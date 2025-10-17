# Analyze Sales Performance Metrics for market expansion – Retail E-commerce | Power BI

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

<img width="1034" height="571" alt="image" src="https://github.com/user-attachments/assets/01233c23-9a74-4a33-82e1-6e4ea89ef3be" />

-Put myself in the stakeholder position to create Empathy map

<img width="976" height="758" alt="image" src="https://github.com/user-attachments/assets/d3a9edd4-4300-42fc-a0d7-3c42ec17403c" />

2️⃣ Define point of view  

-Define Northstar Metric

<img width="1019" height="685" alt="image" src="https://github.com/user-attachments/assets/9948b455-e9b7-4c6f-bc0c-a6ea71acaa94" />

-Define Point of View

<img width="1031" height="778" alt="image" src="https://github.com/user-attachments/assets/90c07b53-7b43-4a84-b5e2-ec1986f61197" />

3️⃣ Ideate

<img width="1034" height="755" alt="image" src="https://github.com/user-attachments/assets/ca5be39c-ccd0-4d6d-b541-ce7df02aaedb" />

4️⃣ & 5️⃣ Prototype - Review

-Build Power BI dashbroad

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

-Observation: The first dashboard shows total sales of $12.6M, total profit of $1.7M, and a low return rate of 0.04%, indicating strong overall performance. However, Japan has the highest return rate at 1.20%, and the return rate by product varies significantly, the trend increase first half of the year but go down immediately in July from $1.3M to $0.7M. EMEA become key region of company but LATAM is at the alarm threshold again
-Recommendation: Need to have more promotional campaigns in the first 7 months of the year to launch more promotional programs to attract customers, continue to invest in sub-category Tables especially in the Africa region. Further consideration of optimal shipping options to the LATAM region

<img width="1432" height="801" alt="image" src="https://github.com/user-attachments/assets/0283d845-b43c-4ef2-a571-c1de51b0bf71" />

#### 2️⃣ Dashboard 2 Preview 

-Observation: The second dashboard highlights return details with a total of 23 returns and a 2.08% return rate, with products like Zebra GX420t Direct Thermal/Thermal Transfer Printer (33.33%) and Holmes Replacement Filter (25.00%) showing the highest return rates. Total return by country peaks in Mexico (10), while North region leads in returns by region (10). Sales returns by person show Chuck Magee with the highest at $4K.

-Recommendation: Need to take care of customer Shirley Daniels returned Hamilton Beach Stove, White office supplies Japan area with the highest return value and also take care customer named Jack leborn asked for feedback on the product if possible give him a voucher to experience more products. Review the carrier especialy second class shipping method has the highest return rate with 13 products returned accounting for $5.1K. 

<img width="1431" height="801" alt="image" src="https://github.com/user-attachments/assets/6defca4a-8044-4765-8d2a-b54ca227e044" />

## 🔎 Final Conclusion & Recommendations  

Through this project, I have gained both technical and business insights:

✅ I learned how to build a business-oriented Power BI dashboard that addresses strategic questions from senior management.

✅ I developed a stronger understanding of key performance metrics such as profit margin, return rate, and regional performance.

✅ I practiced writing DAX measures to calculate complex KPIs (e.g., dynamic profit margin, return rate by product group).

✅ I improved my ability to visualize data effectively, choose the right chart types, and apply meaningful filters and drill-down paths.

✅ I learned how to gather and apply stakeholder feedback to improve usability and actionable insights.

✅ This project also helped me realize the importance of aligning data visualization with business goals.


