# Executive Summary: Financial Performance Dashboard

This repository contains the source data and documentation for a financial performance dashboard, typically visualized using a tool like Power BI. The analysis provides an executive overview of sales, profit, and cost of goods sold (COGS) across various segments, products, and geographies.

---

## 💾 Data Sources

The primary data source for this project is:
* **`Financial Sample.xlsx - Sheet1.csv`**: A CSV file containing transactional financial data.
* **`Executive Summary – Finance Report.pbix`**: The Power BI file containing the final, interactive dashboard.

---

## 📋 Table Details

The dataset provides granular detail on sales transactions. Below is a summary of the columns:

| Column Name | Data Type | Description |
|:---|:---|:---|
| **Segment** | Text | The customer segment (e.g., Government, Midmarket). |
| **Country** | Text | The country where the sale occurred. |
| **Product** | Text | The specific product sold. |
| **Discount Band** | Text | The level of discount applied (e.g., None, High). |
| **Units Sold** | Float | The quantity of units sold in the transaction. |
| **Manufacturing Price** | Integer | The price to manufacture one unit. |
| **Sale Price** | Integer | The price at which one unit was sold. |
| **Gross Sales** | Float | Total sales value before discounts. |
| **Discounts** | Float | Total monetary value of discounts applied. |
| **Sales** | Float | Net sales revenue (after discounts). |
| **COGS** | Float | Cost of Goods Sold for the transaction. |
| **Profit** | Float | The net profit/loss for the transaction. |
| **Date** | Text | The full transaction date. |
| **Month Number** | Integer | The numerical representation of the month (1-12). |
| **Month Name** | Text | The name of the month (e.g., January). |
| **Year** | Integer | The year of the transaction. |

---

## 📊 Power BI Visualizations

The dashboard is structured into sheets, each featuring crucial visualizations for executive review:

### 1. Profit by Month and Year (Line Chart)

* **Chart Type:** **Line Chart**
* **Dimensions & Measures:** Tracks the **Total Profit** (measure) over a time hierarchy, typically displayed by **Month Name** on the X-axis, with separate lines or filtering for **Year**.
* **Key Insight:** This trend analysis is essential for identifying seasonality, growth trends, and specific periods of high or low profitability over the years.

### 2. Total Profit by Country (Map Chart)

* **Chart Type:** **Map Chart** (e.g., Filled Map or Bubble Map)
* **Dimensions & Measures:** Displays **Total Profit** (measure) geographically, using **Country** (dimension) as the location field.
* **Key Insight:** Provides a powerful visual overview of the top-performing and underperforming markets globally, allowing management to quickly allocate resources or investigate regional strategies.

### 3. Total Sales by Product and Segment (Bar Chart)

* **Chart Type:** **Clustered or Stacked Bar Chart**
* **Dimensions & Measures:** Visualizes **Total Sales** (measure) segmented by **Product** (primary dimension) and further broken down by **Segment** (secondary dimension).
* **Key Insight:** This breakdown helps in understanding the revenue contribution of each product line and how well each product performs across different customer segments (e.g., Government vs. Midmarket), guiding product and sales focus.
