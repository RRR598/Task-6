# Data_Analyst_Task-6
# 📊 Sales Trend Analysis (Task 6)

## Overview
This project analyzes monthly **revenue** and **order volume** using SQLite + Python.  
It demonstrates SQL aggregations (`SUM`, `COUNT`, `GROUP BY`) and visualizes trends with matplotlib.

## Tools
- **SQLite (built-in)**
- **Python 3**
- **Pandas** (for query results)
- **Matplotlib** (for charts)

## Steps
1. Create an `orders` table with columns: `order_id`, `order_date`, `amount`, `product_id`.
2. Insert dummy data for multiple months.
3. Run SQL query:
   ```sql
   SELECT strftime('%Y', order_date) AS order_year,
          strftime('%m', order_date) AS order_month,
          SUM(amount) AS total_revenue,
          COUNT(DISTINCT order_id) AS total_orders
   FROM orders
   GROUP BY order_year, order_month
   ORDER BY order_year, order_month;
