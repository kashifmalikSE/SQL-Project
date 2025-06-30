# 📚 Online Book Store – SQL-Based Database System

This project is a relational database system developed using **PostgreSQL** to simulate the backend operations of an online book store. It covers full database normalization, efficient data handling, and real-world SQL query implementation for managing books, authors, customers, orders, and payments.

## 🔍 Project Overview

The goal of this project is to design and implement a normalized SQL-based relational database that supports:
- Inventory management for books
- Customer and order tracking
- Sales and billing records
- Query-based insights and reports

## 🛠️ Technologies Used

- **Database**: PostgreSQL
- **Language**: SQL
- **Tools**: pgAdmin, SQL Shell (psql)

## 🗂️ Database Schema

The database includes the following main entities:

- 📘 **Books**  
- 👨‍💼 **Authors**  
- 🧑‍💼 **Customers**  
- 🧾 **Orders**  
- 💳 **Payments**

Each table is properly normalized to **3rd Normal Form (3NF)** with relationships defined using **primary and foreign keys** to ensure referential integrity.

## ⚙️ Key Features

- ✅ Relational schema with normalized tables
- ✅ Advanced **SQL queries** for data analysis:
  - `JOINs` across multiple tables
  - `GROUP BY`, `HAVING`, and `ORDER BY`
  - **Subqueries** for report generation
  - **Aggregate functions** for calculating revenue, total orders, etc.
- ✅ Efficient data retrieval supporting customer tracking and inventory analysis

## 🧠 Sample SQL Queries

```sql
-- Find the best-selling books
SELECT book_id, COUNT(*) AS total_sold
FROM orders
GROUP BY book_id
ORDER BY total_sold DESC;

-- Total revenue per customer
SELECT customer_id, SUM(amount) AS total_spent
FROM payments
GROUP BY customer_id;

👨‍💻 Author
Muhammad Kashif
BS Software Engineering – University of Mianwali
📧 km8305604@gmail.com
🔗 LinkedIn Profile
