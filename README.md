# SalesInsight-Dashboard-PBI

<img width="2238" height="1259" alt="image" src="https://github.com/user-attachments/assets/86fa79d2-2d51-41ea-99da-b4da470ee2d8" />


Author: ĐỖ HOÀNG MINH

Date: 2025-05-05

Tools Used: Power BI

## 📑 Table of Contents 

1.[📌 Background & Overview](#-background--overview)  

2. [📂 Dataset Description & Data Structure](#-dataset-description--data-structure)

3. [🧠 Design Thinking Process](#-design-thinking-process)

4. [📊 Key Insights & Visualizations](#-key-insights--visualizations)

5. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)


## 📌 Background & Overview 

### Objective

### 📖 What is this project about?

-It provides key financial metrics such as sales, profits, sales volume, return rates, and trends over time, along with detailed data by country, product, and region.

-This project focuses on building a comprehensive dashboard to analyze business performance

### 👤 Who is this project for? 

-Business managers, Senior managers

-Financial management

## 📂 Dataset Description & Data Structure  

### 📌 Data Source 

- Source: Used the data already in the PBIX file to make reports

- Size:4 table ~ 100K rows

- Format: SalesInsight-Dashboard.pbix

#### 1️⃣ Tables Used:

-Fact table: Orders

-Dim table:
  
  + Date
  
  + Returns
  
  + People

-Measure:
  
  + Measure
  

#### 2️⃣ Table Schema & Data Snapshot  

Table 1: Orders

| Column Name        | Data Type |
|--------------------|-----------|
| Order Date         | DATE      |
| Ship Date          | DATE      |
| Ship Mode          | TEXT      |
| Customer ID        | TEXT      |
| Customer Name      | TEXT      |
| Segment            | TEXT      |
| City               | TEXT      |
| State              | TEXT      |
| Country            | TEXT      |
| Postal Code        | FLOAT     |
| Market             | TEXT      |
| Region             | TEXT      |
| Ship Mode          | TEXT      |
| Product ID         | TEXT      |
| Sales              | FLOAT     |
| Quantity           | INT       |
| Profit             | FLOAT     |
| Order Code         | TEXT      |
| Order Year         | DATE      |
| Order ID           | INT       |
| Returns            | TEXT      |


Table 2: Date 

| Column Name        | Data Type |
|--------------------|-----------|
| Date               | DATE      |
| Quarter            | DATE      |
| Year               | DATE      |
| Month              | DATE      |

Table 3: People 

| Column Name        | Data Type |
|--------------------|-----------|
| Region             | TEXT      |
| Person             | TEXT      |

Table 4: Returns 

| Column Name        | Data Type |
|--------------------|-----------|
| Returned           | TEXT      |
| Order Code         | TEXT      |
| Order Year         | DATE      |
| Order ID           | INT       |

#### 3️⃣ Data Relationships: 

| From Table (Column)                       | To Table (Column)                        | Relationship Type |
|------------------------------------------|------------------------------------------|-------------------|
| Orders(Order Code)                       | Returns(Orders Code)                     | Many-to-One       |
| Orders(Order Code)                       | Date(Date)                               | Many-to-One       |
| Orders(Region)                           | People(Region)                           | Many-to-One       |

<img width="803" height="191" alt="image" src="https://github.com/user-attachments/assets/8a3f9428-7128-4a15-8d2e-a6ec024b6ade" />

## 🧠 Design Thinking Process 

1️⃣ Empathize & EDA

-Answer 5W1H 

<img width="1015" height="358" alt="image" src="https://github.com/user-attachments/assets/ab9d6a8e-35c0-4039-b142-2d8a99f81136" />

-Put myself in the stakeholder position to create Empathy map

<img width="649" height="408" alt="image" src="https://github.com/user-attachments/assets/df3713d2-68ee-48ef-9238-589500173912" />

-EDA 

<img width="270" height="392" alt="image" src="https://github.com/user-attachments/assets/6b83b9b9-fc15-4dac-9960-a19c249152b6" />

2️⃣ Define point of view  

-Define Northstar Metric

<img width="230" height="423" alt="image" src="https://github.com/user-attachments/assets/549ebe8e-cf41-49ad-bc2b-abcc08632715" />

-Define Point of View

<img width="456" height="406" alt="image" src="https://github.com/user-attachments/assets/ad9c3fe0-5236-47e2-a4fa-d4a8527a1ac8" />

-Create some Growth Formula base on Pov 

<img width="646" height="154" alt="image" src="https://github.com/user-attachments/assets/75c2bf27-159b-4767-bc7b-0291ca4d1601" />

3️⃣ Ideate

-BRAINSTORMING: start from Growth Formula

<img width="560" height="395" alt="image" src="https://github.com/user-attachments/assets/35409d45-a772-4c8f-a481-296cdffcb0dc" />

-STRUCTURE IDEA: start from each Pov

<img width="865" height="366" alt="image" src="https://github.com/user-attachments/assets/b6203a0f-a602-4163-87a8-7d120c4a4246" />

## ⚒️ Main Process 

1️⃣ Data Cleaning & Preprocessing

-Delete duplicate, missing value, remove columns that unnecessary,... 

2️⃣ Exploratory Data Analysis (EDA) 

-Find the relationship between each table

-Find where is Dimtable where is Facttable

-Find which formula is necessary 

3️⃣ Create a measure table by DAX 

-Measure about AVG,  Margin, rate/sale growth ,total

4️⃣ Power BI Visualization

-Create a ouline 

-Choose chart or card to show the change or display indicators

## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Preview

#### 1️⃣ Dashboard 1 Preview 

-Observation: Observation: The first dashboard shows total sales of $12.6M, total profit of $1.7M, and a low return rate of 0.04%, indicating strong overall performance. However, Japan has the highest return rate at 1.20%, and the return rate by product varies significantly, with Holmes Replacement Filter for HEPA Air Cleaner (25.00%) and Boston 16801 Nautilus Battery Pencil Sharpener (16.67%) showing high returns.

-Recommendation: Investigate the high return rates in Japan and for specific products like the Holmes Filter and Boston Pencil Sharpener to identify quality or market-specific issues. Consider targeted improvements or marketing adjustments to reduce returns and enhance customer satisfaction.

<img width="1430" height="800" alt="image" src="https://github.com/user-attachments/assets/bb3902da-7e9b-4401-8a4a-bc4bfdeb70f7" />

#### 2️⃣ Dashboard 2 Preview 

-Observation: The second dashboard highlights return details with a total of 23 returns and a 2.08% return rate, with products like Zebra GX420t Direct Thermal/Thermal Transfer Printer (33.33%) and Holmes Replacement Filter (25.00%) showing the highest return rates. Total return by country peaks in Mexico (10), while North region leads in returns by region (10). Sales returns by person show Chuck Magee with the highest at $4K.

-Recommendation: Focus on analyzing the root causes of high return rates for Zebra GX420t and Holmes Filter, possibly due to product defects or misuse. Address regional issues in Mexico and the North region, and review Chuck Magee’s sales process to identify potential training or support needs to reduce returns.

<img width="1429" height="801" alt="image" src="https://github.com/user-attachments/assets/6ecfe7af-bed5-44fa-a92c-a8966b9fe15b" />

## 🔎 Final Conclusion & Recommendations  

📌 Key Takeaways:

✔️ Recommendation 1: Maintain current strategies to sustain growth and explore opportunities to further increase sales and profit.

✔️ Recommendation 2: Investigate quality issues with Zebra GX420t and Holmes Filter, and implement targeted market strategies for Japan, Mexico, and the North region to reduce returns.

✔️ Recommendation 3: Review Chuck Magee’s sales process and provide training or support to minimize returns, while leveraging the low overall return rate as a competitive advantage.







✔️ Recommendation 2: Investigate quality issues with Zebra GX420t and Holmes Filter, and implement targeted market strategies for Japan, Mexico, and the North region to reduce returns

✔️ Recommendation 3: Review Chuck Magee’s sales process and provide training or support to minimize returns, while leveraging the low overall return rate as a competitive advantage.
