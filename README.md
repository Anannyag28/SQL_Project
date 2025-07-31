# SQL_Project
# Walmart Sales Data Analysis using SQL

This project focuses on performing structured analysis of Walmart sales data using SQL. The goal is to extract useful business insights related to customer behavior, sales performance, product demand, and revenue generation.

## Dataset Overview

The dataset contains transaction-level information from Walmart, including:

- Invoice ID
- Branch and City
- Customer Type and Gender
- Product Line and Unit Price
- Quantity Sold, VAT, Total, and COGS
- Payment Method
- Date, Time, and Customer Rating

## Technologies Used

- MySQL (or any SQL-compliant RDBMS)
- SQL (DDL, DML, Aggregate Functions, Filtering, Joins, Date-Time Functions)

## Database Setup

```sql
CREATE DATABASE IF NOT EXISTS walmart;

CREATE TABLE sales (
  invoice_id VARCHAR(30) NOT NULL PRIMARY KEY,
  branch VARCHAR(5) NOT NULL,
  city VARCHAR(30) NOT NULL,
  customer_type VARCHAR(30) NOT NULL,
  gender VARCHAR(10) NOT NULL,
  product_line VARCHAR(100) NOT NULL,
  unit_price DECIMAL(10,2) NOT NULL,
  quantity INT NOT NULL,
  VAT FLOAT(6,4) NOT NULL,
  total DECIMAL(12,4) NOT NULL,
  date DATETIME NOT NULL,
  time TIME NOT NULL,
  payment_method VARCHAR(15) NOT NULL,
  cogs DECIMAL(10,2) NOT NULL,
  gross_margin_pct FLOAT(11,9),
  gross_income DECIMAL(12,4) NOT NULL,
  rating FLOAT(2,1)
);
