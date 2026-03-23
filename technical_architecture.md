# Technical Build Documentation
## Creating a GitHub Pages site - GitHub Docs
This documentation outlines the architectural decisions and developmental phases involved in creating the Logistics & Product Analytics Dashboard.

## Tech Stack & Libraries
### Tool / Library	Purpose	Key Benefit
HTML5 & Tailwind CSS	UI Layout & Styling	Rapid, responsive styling without custom CSS files.
JavaScript (ES6+)	Business Logic & JOINs	Enables heavy data processing entirely in the browser.
Chart.js	Data Visualization	Renders high-performance interactive line and bar charts.
PapaParse	CSV Parsing	Handles large-scale data ingestion and async loading.

## Development Roadmap (Build Steps)
Requirement Engineering: Defined core logistics KPIs: Late Deliveries (calculated via timestamp comparison), Unique Purchase Count, and Unique Customer Count.
Visualization Design: Implemented a 2D Intensity Heatmap (7x24 grid) using custom CSS Grid logic to identify peak ordering times by day and hour.
Relational Logic (Multi-File JOIN):
Designed a browser-side "Relational Engine" to join three disparate CSV datasets.
Linked Orders to Order Items via order_id.
Linked Order Items to Products via product_id.
Financial Integration: Added aggregation logic to sum price and shipping_charges from the items dataset to calculate total revenue at a per-order level.

## Debugging & Normalization:
Implemented Key Normalization (trimming and string conversion) to resolve ID mismatches between datasets.
Added Asynchronous Guardrails to ensure all datasets are parsed before the dashboard generation script executes.
Deployment Configuration: Optimized the entire tool into a single-file index.html
