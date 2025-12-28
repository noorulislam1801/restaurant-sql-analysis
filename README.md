# Restaurant Orders Analysis (SQL)
📊 Project Overview

This project analyzes a restaurant database using SQL, covering three levels:

Menu-level analysis – insights about dishes, categories, and pricing

Order-level analysis – order volume, item counts, and large orders

Combined analysis – cross-table insights on top-selling items and highest spend orders

The project demonstrates SQL proficiency, analytical thinking, and the ability to extract business insights.

💼 Business Value

Identify popular and profitable dishes

Understand menu composition and pricing trends

Analyze order patterns and high-value transactions

Support menu planning, pricing strategies, and operational decisions

🔍 Key Analysis

1️⃣ Menu-Level

Count total menu items

Identify cheapest and most expensive dishes

Analyze Italian cuisine offerings

Count dishes per category and compute average price by category

2️⃣ Order-Level

Examine order_details table and date range

Count total orders and total items ordered

Identify orders with most items

Count orders with >12 items

3️⃣ Combined Analysis

Join menu_items and order_details tables

Determine least and most ordered items by category

Identify top 5 orders by total spend

Analyze highest spend order for item composition and category distribution

🛠️ Skills Demonstrated

SQL querying (SELECT, WHERE, ORDER BY)

Aggregations and grouping (COUNT, SUM, AVG, GROUP BY, HAVING)

Table joins (LEFT JOIN) for cross-table insights

Translating business questions into actionable SQL queries

Analytical storytelling and business-focused insights

🧰 Tools & Technologies

SQL (MySQL-compatible syntax)

Relational Database: restaurant_db

Optional: CSVs for dataset replication

📂 Example Queries
-- Menu-Level
SELECT category, AVG(price) AS avg_price
FROM menu_items
GROUP BY category;

-- Order-Level
SELECT order_id, COUNT(item_id) AS num_items
FROM order_details
GROUP BY order_id
ORDER BY num_items DESC;

-- Combined Analysis
SELECT item_name, category, COUNT(order_details_id) AS num_purchases
FROM order_details od 
LEFT JOIN menu_items mi ON od.item_id = mi.menu_item_id
GROUP BY item_name, category
ORDER BY num_purchases DESC;

🎯 Portfolio Relevance

Demonstrates foundational to advanced SQL skills

Shows ability to extract business insights from relational databases

Relevant for Data Analyst, BI Analyst, and Junior Data / Reporting roles
