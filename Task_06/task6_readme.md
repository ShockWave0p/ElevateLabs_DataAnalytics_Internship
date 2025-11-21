# Task 06: Sales Trend Analysis

## Overview
This task performs monthly sales trend analysis using PostgreSQL, focusing on revenue and order volume using aggregation functions and date extraction techniques.

## Key Objectives
- Extract month and year from the date column.
- Calculate monthly revenue using SUM().
- Calculate monthly order count using COUNT(DISTINCT).
- Group results by year and month.
- Sort results chronologically.
- Limit results for specific time periods.
- Create a reusable SQL view.

## SQL Scripts Used

### 1. Preview the dataset
```sql
SELECT *
FROM sales_data
LIMIT 20;
```

### 2. Extract year and month from the date
```sql
SELECT 
    date,
    EXTRACT(YEAR FROM date) AS year,
    EXTRACT(MONTH FROM date) AS month
FROM sales_data
LIMIT 20;
```

### 3. Monthly revenue and order volume
```sql
SELECT
    EXTRACT(YEAR FROM date)  AS year,
    EXTRACT(MONTH FROM date) AS month,
    SUM(order_value_eur)     AS monthly_revenue,
    COUNT(DISTINCT order_id) AS monthly_order_volume
FROM sales_data
GROUP BY
    EXTRACT(YEAR FROM date),
    EXTRACT(MONTH FROM date)
ORDER BY
    year,
    month;
```

### 4. Sorted by latest months
```sql
SELECT
    EXTRACT(YEAR FROM date)  AS year,
    EXTRACT(MONTH FROM date) AS month,
    SUM(order_value_eur)     AS monthly_revenue,
    COUNT(DISTINCT order_id) AS monthly_order_volume
FROM sales_data
GROUP BY
    EXTRACT(YEAR FROM date),
    EXTRACT(MONTH FROM date)
ORDER BY
    year DESC,
    month DESC;
```

### 5. Last 6 months only
```sql
SELECT
    EXTRACT(YEAR FROM date)  AS year,
    EXTRACT(MONTH FROM date) AS month,
    SUM(order_value_eur)     AS monthly_revenue,
    COUNT(DISTINCT order_id) AS monthly_order_volume
FROM sales_data
GROUP BY
    EXTRACT(YEAR FROM date),
    EXTRACT(MONTH FROM date)
ORDER BY
    year DESC,
    month DESC
LIMIT 6;
```

### 6. Create a monthly trend view
```sql
CREATE VIEW monthly_sales_trend AS
SELECT
    DATE_TRUNC('month', date) AS month_start,
    EXTRACT(YEAR FROM date)   AS year,
    EXTRACT(MONTH FROM date)  AS month,
    SUM(order_value_eur)      AS monthly_revenue,
    COUNT(DISTINCT order_id)  AS monthly_order_volume
FROM sales_data
GROUP BY
    month_start, year, month
ORDER BY
    month_start;
```

## Insights
- Revenue spikes are visible in June and December across both years.
- February 2020 shows the lowest revenue period.
- Order volume shows steady improvement from 2019 to early 2020.

## Deliverables
- SQL script
- Final results table
- PDF summary
