# 📊 Sales Report - Power BI Dashboard

## 🧾 Project Overview
This Power BI report provides a comprehensive analysis of **sales performance**, aiming to uncover trends, monitor KPIs, and support data-driven business decisions.  
It helps stakeholders track revenue growth, profit margins, customer performance, and product-level insights across various regions and time periods.

---

## 🎯 Objectives
- Analyze total sales, profit, and quantity across time, regions, and product categories.
- Identify top-performing products and customers.
- Understand sales trends and forecast potential growth areas.
- Compare regional and segment-wise performance.
- Provide an interactive dashboard for management-level reporting.

---

## 🧩 Dataset Details
**Dataset Source:** `<e.g., Sales_Data.csv / Excel / SQL Database>`  
**Data Period:** `<e.g., Jan 2019 – Dec 2023>`  
**No. of Records:** `<e.g., 50,000+ transactions>`  
**Key Columns:**
- `Order ID`
- `Order Date`
- `Customer Name`
- `Product Category`
- `Sub-Category`
- `Region`
- `Sales`
- `Profit`
- `Quantity`
- `Discount`

---

## 🧮 Data Cleaning & Transformation
Performed within **Power Query Editor**:
- Removed null and duplicate records.
- Split and merged columns for standardization.
- Changed data types for date and currency columns.
- Created calculated columns like *Year*, *Month*, *Profit Margin (%)*, and *Sales per Customer*.
- Established relationships between fact and dimension tables (Star Schema Model).

---

## 🧠 DAX Measures Used
Some key DAX measures implemented:
```DAX
Total Sales = SUM(Sales[Sales])
Total Profit = SUM(Sales[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales])
Total Quantity = SUM(Sales[Quantity])
Sales Growth % = DIVIDE(([Total Sales] - [Previous Year Sales]), [Previous Year Sales])
Average Discount = AVERAGE(Sales[Discount])
