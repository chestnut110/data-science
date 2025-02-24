# Restaurant Sales Dashboard

## Project Overview

This project involves analyzing a restaurant's sales data and building an interactive sales dashboard to derive insights. The analysis was performed using PostgreSQL to query the dataset, and the results were visualized using a dashboard. The goal was to uncover key business metrics such as total revenue, best-selling pizzas, and sales trends over time.

## Data Source

The dataset used for this project consists of restaurant sales data stored in a CSV file. The dataset includes:<br><br>
Order date<br>
Order ID<br>
Pizza name, category, and size<br>
Quantity sold<br>
Total price<br>

## Technologies Used

PostgreSQL – For querying and analyzing the dataset<br>

Power BI – For creating the dashboard<br>


## SQL Queries & Insights

The dataset was analyzed using SQL queries in PostgreSQL to derive insights.<br>

<b>Key Business Metrics:</b><br>

Total Revenue:<br>

SELECT SUM(total_price) AS total_revenue FROM sales_data;<br>

Average Order Value:<br>

SELECT SUM(total_price) / COUNT(DISTINCT order_id) AS avg_order_value FROM sales_data;<br>

Total Pizzas Sold:<br>
SELECT SUM(quantity) AS total_pizza_sold FROM sales_data;<br>

Total Orders:<br>
SELECT COUNT(DISTINCT order_id) AS total_orders FROM sales_data;<br>

Average Pizzas per Order:<br>

SELECT CAST(CAST(SUM(quantity) AS DECIMAL(10,2)) / CAST(COUNT(DISTINCT order_id) AS DECIMAL(10,2)) AS DECIMAL(10,2))
AS avg_pizzas_per_order FROM sales_data;<br>

<b>Sales Trends:</b><br><br>

Orders by Day of the Week:<br>

SELECT TO_CHAR(order_date,'Day') AS order_day, COUNT(DISTINCT order_id) AS total_orders
FROM sales_data GROUP BY TO_CHAR(order_date,'Day');<br>

Orders by Month:<br>

SELECT TO_CHAR(order_date,'Month') AS month_name, COUNT(DISTINCT order_id) AS total_orders
FROM sales_data GROUP BY TO_CHAR(order_date,'Month') ORDER BY total_orders DESC;<br>

<b>Sales Breakdown:</b><br><br>

Sales by Pizza Category:<br><br>

SELECT pizza_category, SUM(total_price) AS total_sales,
SUM(total_price) * 100 / (SELECT SUM(total_price) FROM sales_data) AS PCT
FROM sales_data GROUP BY pizza_category;

Sales by Pizza Size:

SELECT pizza_size, SUM(total_price) AS total_sales,
SUM(total_price) * 100 / (SELECT SUM(total_price) FROM sales_data) AS PCT
FROM sales_data GROUP BY pizza_size;

Best & Worst Performing Pizzas:

Top 5 Pizzas by Revenue: ORDER BY total_revenue DESC LIMIT 5;

Top 5 Pizzas by Quantity Sold: ORDER BY total_quantity DESC LIMIT 5;

Bottom 5 Pizzas by Revenue: ORDER BY total_revenue ASC LIMIT 5;

Bottom 5 Pizzas by Quantity Sold: ORDER BY total_quantity ASC LIMIT 5;

Dashboard Summary

The dashboard includes:

Sales Overview: Total revenue, number of orders, and average order value.

Sales Trends: Sales by day of the week and month.

Top & Bottom Selling Pizzas: Revenue and order count for individual pizzas.

Category & Size Sales Distribution: Breakdown of sales by pizza category and size.

How to Use

Clone this repository: git clone <repo-link>

Import the provided dataset into PostgreSQL.

Run the provided SQL queries to explore the data.

Use Power BI / Tableau to create custom visualizations.

Conclusion & Next Steps

This project provides valuable insights into restaurant sales and customer preferences. Possible next steps include:

Forecasting future sales using time series analysis.

Analyzing customer purchase behavior to optimize promotions.

Enhancing the dashboard with real-time updates.
