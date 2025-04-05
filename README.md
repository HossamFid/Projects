
# 📊 Sales Data Warehouse Analytics

This project presents a set of SQL scripts designed to generate insightful reports from a star schema-style data warehouse consisting of **customers**, **products**, and **sales**.

Using **Microsoft SQL Server** and a well-structured schema, the reports deliver valuable business intelligence such as sales performance, customer segmentation, and product behavior across time.

## 📁 Project Structure

The data warehouse includes three main tables:

- `gold.fact_sales` – Contains transactional data for product sales.
- `gold.dim_customers` – Stores customer demographic and profile information.
- `gold.dim_products` – Holds product-related metadata like category, cost, and maintenance info.

The scripts in this project generate the following:

---

## 1️⃣ Business Summary Report

**File:** Embedded in comments within the script  
**Purpose:** High-level overview of core metrics for quick business performance insights.

### 📈 Key Metrics Calculated:

- Total Sales
- Total Quantity Sold
- Average Price
- Total Orders
- Total Products
- Total Customers

> ✅ Executed using `UNION ALL` to return a unified view of aggregated KPIs.

---

## 2️⃣ Customer Report

**Script:** `customer_report` view  
**Purpose:** Analyze customer behaviors and segment them for marketing or retention strategies.

### 🧩 Metrics Included:

- Customer Age & Full Name
- Total Orders, Total Sales, Quantity Purchased
- Lifespan (months between first and last order)
- Recency (months since last order)
- Average Order Value (AOV)
- Age Group: `<20`, `<30`, `adult`, `old`
- Segments: `VIP`, `Normal`, `New`

> 🎯 Helps in identifying high-value and newly acquired customers.

---

## 3️⃣ Product Report

**Script:** `product_report` view  
**Purpose:** Evaluate product-level performance, pricing effectiveness, and customer reach.

### 📦 Metrics Included:

- Product Name, Category, Subcategory
- Total Orders, Sales, Quantity Sold
- Unique Customers
- Lifespan (sales activity duration)
- Average Selling Price
- Performance Segmentation: `Top`, `Mid`, `Low`
- Recency & Average Monthly Revenue
- AOV (Average Order Value)

> 🔍 Supports product lifecycle management and promotion strategies.

---

## 🖼️ Schema Reference

![Schema Diagram](./path-to-your-image.png)  
*(Replace with actual image path once uploaded to GitHub)*

---

## 🚀 How to Use

1. **Run the SQL scripts** in your SQL Server Management Studio (SSMS).
2. Ensure the `gold` schema exists or update schema names accordingly.
3. Execute the `SELECT * FROM customer_report` and `product_report` to view outputs.

---

## 🛠️ Tech Stack

- Microsoft SQL Server
- T-SQL
- Star Schema Modeling

---

## 📌 Notes

- This project assumes clean, validated data in the fact and dimension tables.
- Designed for analytics/BI teams for dashboarding or reporting pipelines.
