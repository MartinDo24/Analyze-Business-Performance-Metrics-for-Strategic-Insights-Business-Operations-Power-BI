# Analyze Business Performance Metrics for Strategic Insights – Business Operations | Power BI

<img width="2238" height="1259" alt="image" src="https://github.com/user-attachments/assets/86fa79d2-2d51-41ea-99da-b4da470ee2d8" />


Author: ĐỖ HOÀNG MINH

Date: 2025-05-05

Tools Used: Power BI

## 📑 Table of Contents 

1. [📌 Background & Overview](#-background--overview)  

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

<details>
<summary> 1️⃣ Tables Used:</summary>

-Fact table: Orders

-Dim table:
  
  + Date
  
  + Returns
  
  + People

-Measure:
  
  + Measure
</details>

<details>
<summary> 2️⃣ Table Schema & Data Snapshot </summary> 

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

</details>

<details>
<summary> 3️⃣ Data Relationships: </summary> 

| From Table (Column)                       | To Table (Column)                        | Relationship Type |
|------------------------------------------|------------------------------------------|-------------------|
| Orders(Order Code)                       | Returns(Orders Code)                     | Many-to-One       |
| Orders(Order Code)                       | Date(Date)                               | Many-to-One       |
| Orders(Region)                           | People(Region)                           | Many-to-One       |

<img width="803" height="191" alt="image" src="https://github.com/user-attachments/assets/8a3f9428-7128-4a15-8d2e-a6ec024b6ade" />

</details>

## 🧠 Design Thinking Process 

1️⃣ Empathize & EDA

<img width="1576" height="845" alt="image" src="https://github.com/user-attachments/assets/48ceee4d-6910-45e1-8467-8ced5e19a8bb" />

-Answer 5W1H 

<img width="1021" height="617" alt="image" src="https://github.com/user-attachments/assets/22b8563b-0cef-40fd-8d98-2717ff6c48d3" />

-Put myself in the stakeholder position to create Empathy map

<img width="1035" height="770" alt="image" src="https://github.com/user-attachments/assets/3546d7a5-fcaf-43bf-9295-15497cc6194d" />

2️⃣ Define point of view  

-Define Northstar Metric

<img width="1029" height="728" alt="image" src="https://github.com/user-attachments/assets/5149455a-ec93-47fd-b605-fe7a24136b57" />

-Define Point of View

<img width="1038" height="792" alt="image" src="https://github.com/user-attachments/assets/f9dcabd5-ee7c-4552-80fd-67c25a29db4e" />

3️⃣ Ideate

<img width="1027" height="753" alt="image" src="https://github.com/user-attachments/assets/3bf592c8-a5b2-42ec-95f2-ff91d358ad59" />

4️⃣ & 5️⃣ Prototype - Review

<img width="982" height="629" alt="image" src="https://github.com/user-attachments/assets/431ce4d6-eda6-46b7-8418-9bb44282cd60" />

<img width="685" height="212" alt="image" src="https://github.com/user-attachments/assets/8fd6f3c6-7cf5-4a19-ad96-663517924ded" />

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

-Observation: The first dashboard shows total sales of $12.6M, total profit of $1.7M, and a low return rate of 0.04%, indicating strong overall performance. However, Japan has the highest return rate at 1.20%, and the return rate by product varies significantly, with Holmes Replacement Filter for HEPA Air Cleaner (25.00%) and Boston 16801 Nautilus Battery Pencil Sharpener (16.67%) showing high returns.

-Recommendation: Investigate the high return rates in Japan and for specific products like the Holmes Filter and Boston Pencil Sharpener to identify quality or market-specific issues. Consider targeted improvements or marketing adjustments to reduce returns and enhance customer satisfaction.

<img width="1430" height="803" alt="image" src="https://github.com/user-attachments/assets/8f02e04d-52c2-4b65-a4c3-88187d5b6b32" />

#### 2️⃣ Dashboard 2 Preview 

-Observation: The second dashboard highlights return details with a total of 23 returns and a 2.08% return rate, with products like Zebra GX420t Direct Thermal/Thermal Transfer Printer (33.33%) and Holmes Replacement Filter (25.00%) showing the highest return rates. Total return by country peaks in Mexico (10), while North region leads in returns by region (10). Sales returns by person show Chuck Magee with the highest at $4K.

-Recommendation: Focus on analyzing the root causes of high return rates for Zebra GX420t and Holmes Filter, possibly due to product defects or misuse. Address regional issues in Mexico and the North region, and review Chuck Magee’s sales process to identify potential training or support needs to reduce returns.

<img width="1432" height="805" alt="image" src="https://github.com/user-attachments/assets/a3b0938b-1433-40eb-a3cf-88003608c151" />

## 🔎 Final Conclusion & Recommendations  

Through this project, I have gained both technical and business insights:

✅ I learned how to build a business-oriented Power BI dashboard that addresses strategic questions from senior management.

✅ I developed a stronger understanding of key performance metrics such as profit margin, return rate, and regional performance.

✅ I practiced writing DAX measures to calculate complex KPIs (e.g., dynamic profit margin, return rate by product group).

✅ I improved my ability to visualize data effectively, choose the right chart types, and apply meaningful filters and drill-down paths.

✅ I learned how to gather and apply stakeholder feedback to improve usability and actionable insights.

✅ This project also helped me realize the importance of aligning data visualization with business goals.


