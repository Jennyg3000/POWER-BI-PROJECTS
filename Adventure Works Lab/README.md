
# Reseller Sales Analysis Dashboard 

This repository contains the source data and the Power BI solution for analyzing reseller sales performance. The dashboard provides a detailed look at transactional data, costs, and sales revenue, designed to track key performance indicators (KPIs) in the reseller channel.

---

## 💾 Data Sources

The analysis leverages a single fact table containing all transactional details and the final Power BI report file:

1.  **`ResellerSales_202006.csv`**: A CSV file containing all line-item sales transactions for June 2020. This data is part of a larger data warehouse structure.
2.  **`12-Solution-Sales Analysis.pbix`**: The Power BI report file, which includes the data model, measures (like **Profit**), and visualizations built upon this data.

---

## 📋 Table Details

The primary data file, **`ResellerSales_202006.csv`**, is a fact table containing 3,004 records. It is structured using surrogate keys, allowing it to be joined to various dimension tables (which are implicitly handled within the Power BI data model).

| Column Name | Data Type | Description |
|:---|:---|:---|
| **SalesOrderNumber** | Text | Unique identifier for the customer order. |
| **SalesOrderLineNumber** | Integer | Line item sequence within the order. |
| **OrderDate, DueDate, ShipDate** | Date | Key dates for the order lifecycle. |
| **ProductKey** | Integer | Identifier to link to Product details. |
| **ResellerKey** | Integer | Identifier to link to Reseller details. |
| **PromotionKey** | Integer | Identifier to link to Promotion details. |
| **EmployeeKey** | Integer | Identifier to link to Sales Employee details. |
| **SalesTerritoryKey** | Integer | Identifier to link to Sales Territory details. |
| **OrderQuantity** | Integer | The number of units sold in the line item. |
| **UnitPrice** | Float | The selling price per unit. |
| **TotalProductCost** | Float | The total cost of goods sold (COGS) for the units. |
| **SalesAmount** | Float | The total revenue generated for the line item. |
| *Calculated Measure* | Float | **Profit** = `SalesAmount` - `TotalProductCost`. |

---

## 📊 Visualization Overview (Power BI)

The `12-Solution-Sales Analysis.pbix` file is structured to answer critical business questions using the following types of visualizations:

[![Power BI Dashboard](https://github.com/user-attachments/assets/458ea196-494f-46ca-a202-7bca3c56b842)](https://app.powerbi.com/view?r=eyJrIjoiNzhhMGE1OTQtNzUwYi00MjU5LWE3MDUtZDIwNzFjZWE0MmEyIiwidCI6IjNlYTdjMTI4LWM2MDEtNDQ3OS1hMDAzLWUxNGQwMGMwYjVjYiJ9)

### 1. Sales Trend over Time (Line Chart)

* **Focus:** Tracking the **Sales Amount** and **Profit** by **OrderDate**.
* **Purpose:** To monitor daily and weekly sales performance, spot trends, and identify any anomalies or dips in profitability during the month of June 2020.

### 2. Reseller Performance (Bar Chart)

* **Focus:** Ranking **Total Sales** or **Total Profit** by **ResellerKey**.
* **Purpose:** To identify the top-performing resellers and understand their contribution to the overall sales channel.

### 3. Product Performance (Bar Chart)

* **Focus:** Analyzing **Sales Amount** and **Profit** by **ProductKey**.
* **Purpose:** To determine which products are the most popular or most profitable, which is crucial for inventory and marketing decisions.

### 4. Territory Analysis (Map/Table)

* **Focus:** Breaking down **Sales Amount** by **SalesTerritoryKey**.
* **Purpose:** Provides a high-level view of which sales regions are driving the highest revenue and profit.

  <img width="1223" height="529" alt="image" src="https://github.com/user-attachments/assets/7f297e99-f3a8-4a8f-bc63-5d32d0eed445" />

  <img width="1793" height="971" alt="image" src="https://github.com/user-attachments/assets/fd1921dc-ff2e-49c5-a979-223d06c55923" />


 

