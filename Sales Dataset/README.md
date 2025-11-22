# Sales Analysis and Performance Dashboard 🚀

This repository contains the source data and documentation for a comprehensive sales analysis dashboard, developed using **Power BI**, that monitors **Key Performance Indicators (KPIs)** and trends across various regions, products, and customer segments. 🎯

---

## 💾 Data Sources 📂

The analysis is based on two related CSV files derived from the original Excel workbook, **`Sales Dataset.xlsx`**. The full interactive dashboard is contained within the Power BI file.

| File Name | Description | Type |
| :--- | :--- | :--- |
| **`Sales Dataset.xlsx - ListOfOrders.csv`** | Contains high-level order, customer, and geographic details. 📋 | Data Source |
| **`Sales Dataset.xlsx - OrderBreakdown.csv`** | Contains product-level sales figures, profit, and quantity data. 📈 | Data Source |
| **`Sales.pbix`** | The complete interactive Power BI report file. 📊 | Dashboard |

---
## 📋 Table Structure and Linking ✨

The two data tables are linked via the **`Order ID`** column, establishing a standard **One-to-Many** relationship for comprehensive reporting across all dimensions. 🔗

### 1. `ListOfOrders` Table (Order and Customer Details) 🛍️

| Column Name | Data Type | Description |
|:---|:---|:---|
| **Order ID** | Text | Unique identifier for each order. (**Primary Key**) 🔑 |
| **Order Date** | Text | The date the order was placed. 🗓️ |
| **Customer Name** | Text | The name of the customer. 👤 |
| **City, Country, Region, State** | Text | Geographical details of the destination. 🌍 |
| **Segment** | Text | The customer group (e.g., Consumer, Corporate). 👥 |
| **Ship Date, Ship Mode** | Text | Logistics details. 🚚 |
| **lon, lat** | Float | Geographic coordinates for mapping. 📍 |

### 2. `OrderBreakdown` Table (Product and Transaction Details) 📦

| Column Name | Data Type | Description |
|:---|:---|:---|
| **Order ID** | Text | Foreign key linking to the `ListOfOrders` table. 🔑 |
| **Product Name** | Text | The specific item sold. 🏷️ |
| **Discount** | Float | The discount rate applied to the line item. 📉 |
| **Sales** | Integer | The revenue generated. 💰 |
| **Profit** | Integer | The profit or loss generated. 💲 |
| **Quantity** | Integer | The number of units sold. 🔢 |
| **Category** | Text | The top-level product category (e.g., Furniture, Technology). 💻 |
| **Sub-Category** | Text | The detailed product sub-category (e.g., Chairs, Phones). 🛋️ |


---

## 📊 Power BI Visualizations

The dashboard features several key charts to analyze sales performance across different dimensions:

👉 
[![Power BI Dashboard](https://github.com/user-attachments/assets/210f9ed5-d6ea-4f05-bf61-ce1d9b13b39e)](https://app.powerbi.com/view?r=eyJrIjoiOTE1ODUyNTItOWZjZi00NmQ4LTg2MWQtOWRkMWQ5YWViN2U0IiwidCI6IjNlYTdjMTI4LWM2MDEtNDQ3OS1hMDAzLWUxNGQwMGMwYjVjYiJ9)


### 1. Top Sales by Category and Segments (Bar Chart)🔬

* **Chart Type:** **Clustered/Stacked Bar Chart** 📊
* **Dimensions & Measures:** Visualizes **Total Sales** (measure) segmented by **Category** (primary dimension) and then further broken down by **Segment** (secondary dimension).#️⃣
* **Key Insight:** Identifies which product categories are the largest revenue drivers and shows how sales performance varies across customer segments (Consumer, Corporate, Home Office) within those categories.✅

  <img width="643" height="334" alt="image" src="https://github.com/user-attachments/assets/8430e408-bdf3-4149-8527-e9e186128c10" />


### 2. 📅Total Sales Profit by Year (Line Chart)💵

* **Chart Type:** **Line Chart**📈
* **Dimensions & Measures:** Tracks the **Total Profit** (measure) over **Year** (derived from `Order Date`).
* **Key Insight:** Illustrates the overall financial trend of the business over time. This helps in spotting periods of growth, decline, or seasonality in profitability.💡

<img width="656" height="334" alt="image" src="https://github.com/user-attachments/assets/865f2794-57a2-48db-a19b-ee51c02aa12b" />


### 3.🗺️ Country and Profit (Map Chart)🌍

* **Chart Type:** **Filled Map / Bubble Map**📍
* **Dimensions & Measures:** Displays **Total Profit** (measure) geographically, usually using **Country** (dimension) to shade the map or size bubbles.
* **Key Insight:** Provides a visual representation of performance across the global market, easily highlighting countries that are major profit centers versus those generating losses.💡

<img width="607" height="379" alt="image" src="https://github.com/user-attachments/assets/306d1ce4-de90-4520-b5eb-866651b44b2e" />


### 4.🥇 Top 10 Profit Products (Bar/Line Chart)📈

* **Chart Type:** **Bar Chart or Line Chart** (Ranked by Profit)
* **Dimensions & Measures:** Shows the **Total Profit** (measure) for the **Top 10 Product Names** (dimension).💲
* **Key Insight:** Pinpoints the individual products that contribute the most significantly to the company's overall profitability, aiding in inventory, marketing, and sales strategy planning.💡

<img width="699" height="407" alt="image" src="https://github.com/user-attachments/assets/6ff5fb62-6ebc-475a-a9e3-1b962d24bcc6" />

