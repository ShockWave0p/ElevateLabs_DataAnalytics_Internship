📊 Sales Analytics Dashboard – Power BI

A complete end-to-end sales analysis project covering data cleaning, modeling, DAX measures, and interactive dashboard design. The project uncovers insights related to revenue, orders, customer patterns, seasonal trends, and category-level performance.

🚀 Project Overview

This dashboard provides a consolidated view of company-wide sales performance. It highlights key KPIs, identifies top-performing categories, tracks month-wise revenue movement, and helps stakeholders make faster business decisions using data-driven insights.

📁 Files Included

clean_sales.csv – Cleaned and transformed dataset

Power BI (.pbix) file – Final interactive dashboard

README.md – Project documentation

Insight Report – Key observations extracted from the dashboard

🧹 Data Cleaning Steps

Performed in Power Query:

Removed inconsistent formats in date, product, region columns

Checked & fixed missing values

Removed duplicates

Split Category/Sub-Category (if present)

Standardized column names

Created a Month-Year Key for time intelligence

Added calculated columns needed for analysis

🧮 DAX Measures

Key measures created:

Total Revenue = SUM(Sales[Revenue])

Total Orders = DISTINCTCOUNT(Sales[Order ID])

Average Order Value = [Total Revenue] / [Total Orders]

Revenue YoY % = 
DIVIDE(
    [Total Revenue] - CALCULATE([Total Revenue], SAMEPERIODLASTYEAR(Sales[Order Date])),
    CALCULATE([Total Revenue], SAMEPERIODLASTYEAR(Sales[Order Date]))
)

Top Categories = 
TOPN(3, 
    SUMMARIZE(Sales, Sales[Category], "Revenue", [Total Revenue]),
    [Total Revenue], DESC
)

📈 Dashboard Features
Main KPIs

Total Revenue

Total Orders

Average Order Value

YoY Growth %

Charts

Revenue by Month

Orders by Month

Region-wise Performance

Top 3 Revenue-Generating Categories

Category & Sub-Category Breakdown

Daily Sales Trend

All visuals are fully interactive with drill-downs, filters, and slicers.

🔍 Key Insights

Revenue shows a clear upward trend, indicating strong month-over-month growth.

Top 3 revenue-generating categories are: Category A, Category B, Category C.

West region leads in both orders and revenue, showing strongest customer engagement.

Average Order Value remains stable, indicating consistent pricing strategy.

Seasonal spikes observed around Month-End and Festive periods.

🛠 Tools Used

Power BI Desktop (Dashboard creation)

MS Excel / Jupyter Notebook (Data cleaning + CSV export)

DAX (Metrics calculation)

GitHub (Project hosting)

📜 How to Use

Download the .pbix file

Open it in Power BI Desktop

Explore the pages, apply slicers, read insights

Use or extend the dashboard for your own projects

⭐ Future Improvements

Add forecasting using Power BI ML

Add customer segmentation (RFM)

Create automated refresh using Power BI Service