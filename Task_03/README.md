# Task 3 – SQL for Data Analysis  
**Dataset:** Online Retail II  
**Tool:** PostgreSQL  
**Author:** Swaraj  

---

## 📌 Overview  
This task focuses on analyzing ecommerce transaction data using SQL.  
The goal is to apply essential SQL concepts for data extraction, transformation, and analysis.

The following SQL components were implemented:

- SELECT  
- WHERE  
- Aggregate Functions (SUM, COUNT, MIN, MAX)  
- GROUP BY  
- ORDER BY  
- Subqueries  
- JOINS (INNER, LEFT, RIGHT)  
- Views  
- Index Optimization  

All executed queries are stored inside **task3_queries.sql**, and output screenshots are placed in the **/screenshots** folder.

---

## 📊 Dataset Description  
The Online Retail II dataset contains one year of ecommerce transactions.

| Column        | Description                          |
|---------------|--------------------------------------|
| invoice       | Transaction code                     |
| stock_code    | Product identifier                   |
| description   | Product description                  |
| quantity      | Number of units sold                 |
| invoice_date  | Date and time of transaction         |
| price         | Unit price                           |
| customer_id   | Unique customer identifier           |
| country       | Customer’s country                   |

**Total Rows:** ~541,910  
**Date Range:** Dec 2010 → Dec 2011  

---

## 🧪 SQL Tasks Completed

### **1. SELECT Statements**
Previewed the dataset and sample rows.

### **2. WHERE Filtering**
Filtered data by:
- Country  
- Quantity  
- Date ranges  

### **3. Aggregate Functions**
- Total number of rows  
- Null value counting  
- Total revenue calculation  
- Date range extraction (MIN/MAX)  

### **4. GROUP BY Analysis**
- Revenue by country  
- Monthly revenue  

### **5. Subquery**
Top 5 highest spending customers.

### **6. JOINS**
Joined the main retail dataset with a product category lookup table.

### **7. Views**
Created:
- `monthly_revenue`
- `revenue_by_country`

### **8. Index Optimization**
Indexes added to speed up filtering & grouping:
- country  
- invoice_date  
- customer_id  

---

## 📁 Repository Structure

```
Task_3/
│── task3_queries.sql
│── Task_3_Report.docx
│── online_retail_II.csv
│── README.md
│── screenshots/
│     ├── select.png
│     ├── where.png
│     ├── aggregates.png
│     ├── groupby.png
│     ├── subquery.png
│     ├── joins.png
│     ├── views.png
│     └── indexes.png
```


## 📌 Conclusion  
The dataset was fully analyzed using essential SQL techniques including filtering, aggregation, joins, subqueries, view creation, and optimization.  
All required components from the Task 3 PDF have been completed.

---

## ✨ Author  
**Swaraj**  
Data Analytics Intern  

