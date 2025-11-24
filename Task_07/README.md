📌 Task 7 — Basic Sales Summary using SQLite + Python

This project demonstrates how to use SQLite inside Python to extract basic sales insights, load data into pandas, and create simple visualizations.

🔧 Tools Used

Python

sqlite3

pandas

matplotlib

Jupyter Notebook

| File                      | Description                                                          |
| ------------------------- | -------------------------------------------------------------------- |
| **task7.ipynb**           | Jupyter notebook with all steps (DB creation, SQL, analysis, charts) |
| **sales_data.db**         | SQLite database containing sample sales data                         |
| **sales_chart.png**       | Bar chart showing revenue by product                                 |
| **revenue_pie_chart.png** | Pie chart showing revenue share                                      |
| **sales_summary.csv**     | Exported summary of total quantity and revenue                       |
| **README.md**             | Project explanation and documentation                                |

🗃️ Steps Performed
1. Database Creation

Created sales_data.db

Added a table named sales with columns:

product

quantity

price

Inserted 5 sample product sales records.

2. SQL Query Execution

Executed an SQL GROUP BY query to calculate:

Total Quantity Sold

Total Revenue (quantity × price)

Loaded the output into a pandas DataFrame and printed it.

3. Visualization

Created a bar chart to show revenue for each product.

Saved the chart as:

sales_chart.png

🔥 Additional Insights (Bonus Work)
⭐ 1. Top Selling Product

Identified the product with the highest revenue.

⭐ 2. Revenue Share Pie Chart

Created a pie chart showing each product’s contribution to overall revenue.

Saved as:
revenue_pie_chart.png

⭐ 3. Exported Summary to CSV

Exported the aggregated sales summary as:

sales_summary.csv

This makes it easy to reuse for reporting or dashboards.

📝 What I Learned

How to connect SQLite with Python

Executing SQL queries inside Python

Aggregations using SQL (SUM, GROUP BY)

Loading SQL results into pandas

Creating bar charts and pie charts with matplotlib

Exporting data for further analysis

🔗 Final Submission

This repository contains:

Notebook

Database

Visualizations

Summary CSV

Full documentation