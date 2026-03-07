# ☕ Coffee Shop Sales Analysis (SQL Project)

## 📌 Project Overview

This project analyzes a Coffee Shop Sales dataset using SQL to extract meaningful business insights from transactional data. The analysis focuses on understanding sales performance, identifying top-selling products, evaluating store performance, and discovering time-based sales trends.

The goal of this project is to demonstrate practical SQL data analysis skills such as filtering, aggregation, grouping, and time-based analysis to support data-driven decision making.

---

## 🎯 Project Objectives

* Analyze overall **sales and revenue performance**
* Identify **top-selling products**
* Compare **sales across different store locations**
* Analyze **customer purchasing patterns by time**
* Generate **business insights from sales data**

---

## 🗂 Dataset Information

The dataset contains transactional sales data with the following columns:

| Column Name      | Description                    |
| ---------------- | ------------------------------ |
| transaction_id   | Unique transaction identifier  |
| transaction_date | Date of transaction            |
| transaction_time | Time of transaction            |
| transaction_qty  | Quantity of products purchased |
| store_id         | Store identifier               |
| store_location   | Store location                 |
| product_id       | Product identifier             |
| unit_price       | Price per product              |
| product_category | Category of product            |
| product_type     | Type of product                |
| product_detail   | Specific product name          |

---

## 🛠 Tools & Technologies

* SQL (MySQL / BigQuery)
* Data Analysis
* GitHub for version control

---

## 📊 Key SQL Analysis

### Total Revenue

```sql
SELECT SUM(transaction_qty * unit_price) AS total_revenue
FROM coffee_sales;
```

### Revenue by Product Category

```sql
SELECT 
product_category,
SUM(transaction_qty * unit_price) AS revenue
FROM coffee_sales
GROUP BY product_category
ORDER BY revenue DESC;
```

### Top Selling Products

```sql
SELECT 
product_detail,
SUM(transaction_qty) AS total_sales
FROM coffee_sales
GROUP BY product_detail
ORDER BY total_sales DESC
LIMIT 10;
```

### Store Performance

```sql
SELECT 
store_location,
SUM(transaction_qty * unit_price) AS revenue
FROM coffee_sales
GROUP BY store_location;
```

### Sales by Hour

```sql
SELECT 
HOUR(transaction_time) AS hour,
SUM(transaction_qty) AS total_sales
FROM coffee_sales
GROUP BY hour
ORDER BY hour;
```

---

## 📈 Key Insights

* Coffee products generate the **highest sales volume**.
* **Morning hours** show the highest number of transactions.
* Some store locations generate **higher revenue than others**.
* A small number of products contribute to a **large portion of sales**.

---

## 📁 Project Structure

```
coffee-shop-sales-sql-project
│
├── dataset.csv
├── create_table.sql
├── analysis_queries.sql
└── README.md
```

---

## 🚀 How to Use This Project

1. Import the dataset into your SQL database.
2. Create the table using the provided SQL schema.
3. Run the analysis queries to generate insights.

---

FILE : https://1drv.ms/b/c/DEDAF65BEE0BCD3E/IQBKcyVi9bH5Tpi8_XDU33jhATdKyawKgZvsiUADphI12OU?e=ATIqHH
