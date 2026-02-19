# Bank Database SQL Project

A SQL database project for managing bank customers, accounts, and transactions.

## 📌 Overview

This project contains SQL queries for a banking system that handles:
- Customer accounts
- Transactions
- Account relationships
- Balance calculations

## 🗄️ Database Tables

- **BANK_CUSTOMER** - Customer information
- **BANK_ACCOUNT_DETAILS** - Account details
- **BANK_ACCOUNT_TRANSACTION** - Transaction records
- **BANK_ACCOUNT_RELATIONSHIP_DETAILS** - Account linking
- **BANK_INTEREST_RATE** - Interest rates
- **BANK_CUSTOMER_MESSAGES** - Customer notifications

## 🚀 Setup

1. Create database:
```sql
CREATE DATABASE Customer_details;
USE Customer_details;
```

2. Run the schema file to create tables and insert data

3. Execute queries from `queries.sql`

## 📊 Sample Queries

**Customer Average Balance:**
```sql
SELECT customer_id, customer_name, AVG(Balance_amount) AS average_balance
FROM BANK_CUSTOMER bc
JOIN Bank_Account_Details bad ON bc.customer_id = bad.Customer_id
GROUP BY customer_id, customer_name;
```

**Monthly Transactions:**
```sql
SELECT Account_Number, Transaction_amount, Transaction_Date
FROM BANK_ACCOUNT_TRANSACTION
WHERE MONTH(Transaction_Date) = 3 AND YEAR(Transaction_Date) = 2020;
```

## 🛠️ Technologies

- MySQL
- SQL
- Python + Pandas (optional)

## 👤 Author

Md Suhail
