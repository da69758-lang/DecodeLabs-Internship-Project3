# 🗄️ SQL Data Analysis — Project 3
### DecodeLabs Internship | Batch 2026

This repository contains the raw dataset and SQL analysis work completed as **Project 3** of my Data Analytics internship at **DecodeLabs**. The goal of this project was to use SQL queries to extract meaningful business insights from a raw e-commerce orders dataset.

---

## 📌 Project Objective

> Use SQL to query, filter, group, and aggregate raw data into actionable business intelligence.

Key tasks completed:
- Writing `SELECT` queries to retrieve targeted data
- Filtering records using `WHERE` with equality, comparison, and pattern matching
- Grouping data by category using `GROUP BY`
- Applying aggregate functions: `COUNT()`, `SUM()`, `AVG()`
- Sorting results with `ORDER BY`
- Handling NULL values using `IS NULL` and `COALESCE`

---

## 📂 Dataset Overview

**File:** `SQL_Data_Analysis_Project3.xlsx`

A raw, unprocessed e-commerce orders dataset spanning **2023–2025**. It intentionally contains missing values and uncleaned entries to simulate real-world data scenarios.

### Columns

| Column | Description |
|---|---|
| `OrderID` | Unique order identifier |
| `Date` | Date the order was placed |
| `CustomerID` | Unique customer identifier |
| `Product` | Product category (Laptop, Phone, Monitor, Tablet, Chair, Desk, Printer) |
| `Quantity` | Number of units ordered |
| `UnitPrice` | Price per unit |
| `ShippingAddress` | Delivery address |
| `PaymentMethod` | Credit Card, Debit Card, Cash, Gift Card, Online |
| `OrderStatus` | Delivered, Shipped, Pending, Cancelled, Returned |
| `TrackingNumber` | Shipment tracking ID |
| `ItemsInCart` | Total items in cart at time of order |
| `CouponCode` | Discount code used (SAVE10, FREESHIP, WINTER15, or NULL) |
| `ReferralSource` | Traffic source (Instagram, Google, Facebook, Email, Referral) |
| `TotalPrice` | Final order value |

---

## 🛠️ SQL Concepts Practiced

- `SELECT`, `FROM`, `WHERE`, `ORDER BY`
- `GROUP BY`, `HAVING`
- `COUNT()`, `SUM()`, `AVG()`
- `IS NULL`, `COALESCE`
- Filtering by category, date range, and numeric thresholds
- Pattern matching with `LIKE`

---

## 🔍 Sample Query Ideas

```sql
-- Total revenue by product category
SELECT Product, SUM(TotalPrice) AS TotalRevenue
FROM orders
GROUP BY Product
ORDER BY TotalRevenue DESC;

-- Orders with missing coupon codes
SELECT * FROM orders
WHERE CouponCode IS NULL;

-- Average order value by payment method
SELECT PaymentMethod, AVG(TotalPrice) AS AvgOrderValue
FROM orders
GROUP BY PaymentMethod;

-- Count of orders by status
SELECT OrderStatus, COUNT(*) AS OrderCount
FROM orders
GROUP BY OrderStatus;
```

---

## 🧰 Tools Used

- **SQL** — querying, filtering, aggregation
- **Microsoft Excel** — raw data storage
- **DB Browser / MySQL / PostgreSQL** — query execution

---

## 🏢 About DecodeLabs

DecodeLabs is a tech training organization based in Greater Lucknow, India, offering hands-on industrial internship programs in Data Analytics, Development, and more.

🌐 [www.decodelabs.tech](http://www.decodelabs.tech) | ✉️ decodelabs.tech@gmail.com
