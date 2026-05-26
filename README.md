# 🛒 Retail Sales Analysis using SQL

## 📌 Project Overview

This project analyzes a Superstore retail dataset using SQL to uncover business insights related to sales, customers, products, and profitability.

The project demonstrates:
- SQL data analysis
- Joins and relationships
- Window functions
- Subqueries
- Business reporting queries

---

# 📊 Project Highlights

| Feature | Description |
|---|---|
| 📈 Sales Analysis | Analyze total and category-wise sales |
| 👥 Customer Insights | Identify top customers and buying patterns |
| 📦 Product Analysis | Find top-performing products |
| 💰 Profitability Analysis | Detect loss-making orders |
| 🧠 Advanced SQL | Window Functions, CASE, Subqueries |

---

# 🗂 Dataset Structure

## Customers Table

| Column Name | Description |
|---|---|
| customer_id | Unique customer ID |
| customer_name | Customer name |
| city | Customer city |
| segment | Customer segment |

---

## Orders Table

| Column Name | Description |
|---|---|
| order_id | Unique order ID |
| order_date | Order date |
| sales | Sales amount |
| profit | Profit amount |
| customer_id | Customer reference |
| product_id | Product reference |

---

## Products Table

| Column Name | Description |
|---|---|
| product_id | Unique product ID |
| product_name | Product name |
| category | Product category |
| sub_category | Product subcategory |

---

# 🔗 Database Relationship Diagram

```text
Customers
   │
   │ customer_id
   ▼
Orders_Clean
   ▲
   │ product_id
   │
Products
```

---

# 🛠 SQL Concepts Used

| SQL Concept | Used |
|---|---|
| SELECT Statements | ✅ |
| Filtering (WHERE) | ✅ |
| Aggregate Functions | ✅ |
| GROUP BY & HAVING | ✅ |
| INNER JOIN | ✅ |
| SELF JOIN | ✅ |
| Subqueries | ✅ |
| Window Functions | ✅ |
| CASE Statements | ✅ |
| Ranking Functions | ✅ |

---

# 📌 Key Business Questions Solved

### ✅ Sales Analysis
- Total sales by category
- Running sales totals
- Orders above average sales

### ✅ Customer Analysis
- Top customers by sales
- Customers with multiple orders
- Customers from same city

### ✅ Profit Analysis
- Negative profit orders
- Profit status classification

### ✅ Product Analysis
- Top 3 products in each category
- Best-selling categories

---

# 💻 Sample SQL Queries

## 🔹 Rank Customers Based on Sales

```sql
SELECT customer_id,
SUM(sales) AS total_sales,
RANK() OVER (ORDER BY SUM(sales) DESC) AS customer_rank
FROM orders_clean
GROUP BY customer_id;
```

---

## 🔹 Running Total of Sales

```sql
SELECT order_date,
sales,
SUM(sales) OVER (ORDER BY order_date) AS running_total
FROM orders_clean;
```

---

# 🚀 Tools Used

- MySQL
- SQL
- GitHub
- VS Code / MySQL Workbench

---

# 📈 Project Outcome

This project improved my understanding of:
- SQL query writing
- Data analysis techniques
- Business insight generation
- Advanced SQL concepts

-  📸 Project Screenshots

## SQL Query Example

![SQL Query](Query1.png)
![SQL Query](Query2.png)
![SQL Query](Query3.png)

---

# 👨‍💻 Author

## Viji
Aspiring Data Analyst
