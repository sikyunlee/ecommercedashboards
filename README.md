# 📦 Logistics & E-commerce Analytics Dashboard

An interactive, browser-side data visualization tool designed to analyze logistics performance, shipping efficiency, and product category trends across multiple relational datasets.

## 🚀 Live Demo
You can access the live, interactive dashboard here:
sikyunlee.github.io

## 📊 Key Features & KPIs
This dashboard provides a comprehensive view of e-commerce operations by joining three distinct datasets (Orders, Items, and Products) directly in the browser.
### Logistics Performance
Late Delivery Tracking: Automatically calculates late shipments by comparing order_delivered_timestamp against order_estimated_delivery_date.
Ordering Heatmap: A 24/7 density matrix identifying peak ordering hours and days of the week to help spot logistics bottlenecks.
Time-Series Analysis: Toggle between Weekly and Monthly granularities to track performance trends over time.

### Business Metrics
Revenue Analytics: Aggregates price + shipping_charges to show total gross revenue.
Customer Insights: Tracks unique customer_id counts and total purchase volume.
Category Popularity: Visual breakdown of which product categories drive the most sales volume.

## 📁 Data Preparation
To use this dashboard, you must upload three CSV files from your local machine. No data is ever uploaded to a server; all processing happens locally in your browser.
Orders File (orders_rev_df.csv): Should contain order_id, customer_id, and delivery timestamps.
Order Items File: Should contain order_id, product_id, price, and shipping_charges.
Product Info File: Should contain product_id and product_category_name.
**Note: The tool uses a relational join engine to connect these files using order_id and product_id as primary keys.**

## 🛠️ Technical Implementation
Tailwind CSS: For a modern, responsive user interface.
Chart.js: Powering the trend lines and categorical bar charts.
PapaParse: Used for fast, asynchronous CSV parsing.
GitHub Pages: Hosting the static application with an automated deployment workflow.

## 📝 How to Run Locally
If you'd like to run this project on your own machine:
Clone this repository: git clone https://github.com/sikyunlee/ecommercedashboards.git
Open index.html in any modern web browser (Chrome, Firefox, or Edge).
Upload your logistics CSV files and click Generate Analytics Dashboard.

## 🤝 Contact
Developed by sikyunlee. Feel free to reach out for questions regarding the logistics logic or data structure!
