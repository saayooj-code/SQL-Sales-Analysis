# SQL-Sales-Analysis
SQL Sales Analysis is a MySQL-based data analysis project created to demonstrate practical SQL and database management skills. The project focuses on creating a structured sales database, storing sales transaction data, and analyzing monthly sales performance using SQL queries and window functions.
# SQL Sales Analysis

A beginner-friendly SQL data analysis project using MySQL to store, analyze, and compare sales data.

## 📌 Project Overview

This project demonstrates how SQL can be used to analyze sales data and identify monthly sales trends.

The project creates a sales database, stores product sales information, calculates total monthly sales, and compares each month's sales with the previous month using the `LAG()` window function.

## 🎯 Objectives

- Create a MySQL database and sales table
- Store product sales information
- Retrieve sales records
- Calculate monthly total sales
- Compare current-month sales with previous-month sales
- Practice SQL aggregation and window functions

## 🛠️ Technologies Used

- MySQL
- SQL
- Aggregate Functions
- Window Functions

## 📂 Dataset / Table Structure

The project uses a `SALES` table containing:

| Column | Description |
|---|---|
| `salesid` | Unique sales record ID |
| `productid` | Product identifier |
| `salesdate` | Date of sale |
| `quantity` | Quantity sold |
| `amount` | Sales amount |

## 🔍 SQL Concepts Used

### Database & Table Creation
- `CREATE DATABASE`
- `USE`
- `CREATE TABLE`

### Data Insertion
- `INSERT INTO`

### Data Retrieval
- `SELECT`

### Data Aggregation
- `SUM()`
- `GROUP BY`
- `MONTH()`

### Window Function
- `LAG()`

## 📊 Analysis Performed

The project calculates the total sales for each month using:

```sql
SELECT
    MONTH(SalesDate) AS MonthNo,
    SUM(Amount) AS TotalSales
FROM SALES
GROUP BY MONTH(SalesDate);
