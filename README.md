Pizza Sales SQL Project
Project Overview
This project analyzes sales data for a pizza store using SQL. The goal is to provide insights into sales performance, customer preferences, and other key metrics.

Table of Contents
Introduction
Dataset
SQL Queries
Analysis
Results
Conclusion
How to Use
Contributing
Introduction
In this project, we explore a pizza sales dataset to understand various aspects of the business. We perform data cleaning, manipulation, and analysis using SQL to derive meaningful insights.

Dataset
The dataset used in this project includes:

orders: Details of each pizza order including order ID, date, and customer.
order_details: Specifics about each pizza in an order including size, quantity, and price.
pizzas: Information about different types of pizzas offered including name, category, and ingredients.
pizza_types: Details about the pizza types including description and size options.
SQL Queries
We use SQL to perform various queries at different levels of complexity:

Basic Queries
Retrieve the total number of orders placed.
sql
Copy code
SELECT COUNT(*) AS total_orders FROM orders;
Calculate the total revenue generated from pizza sales.
sql
Copy code
SELECT SUM(price * quantity) AS total_revenue FROM order_details;
Identify the highest-priced pizza.
sql
Copy code
SELECT name, MAX(price) AS highest_price FROM pizzas;
Identify the most common pizza size ordered.
sql
Copy code
SELECT size, COUNT(*) AS count FROM order_details GROUP BY size ORDER BY count DESC LIMIT 1;
List the top 5 most ordered pizza types along with their quantities.
sql
Copy code
SELECT pizza_id, SUM(quantity) AS total_quantity FROM order_details GROUP BY pizza_id ORDER BY total_quantity DESC LIMIT 5;


Analysis
Our analysis focuses on identifying trends and patterns in the sales data. This includes:

Determining the best-selling pizzas and categories
Understanding customer preferences
Analyzing sales trends over time
Identifying peak order times
Results
Key findings from our analysis include:

The most popular pizzas and their sales figures
The busiest times for the store
Trends in customer ordering behavior
Sales performance across different periods

Conclusion
The insights derived from this project can help the pizza store improve its operations, marketing strategies, and customer satisfaction.

How to Use
To replicate this analysis:

Clone the repository:https://github.com/reemachanotia/Pizza_Sales_SQL_Project 

Import the dataset into your SQL environment.
Run the SQL queries provided in the queries.sql file.
Analyze the results and modify queries as needed for further insights.
Contributing
Contributions are welcome! If you have any suggestions or improvements, please create a pull request or open an issue.

