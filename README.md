# Superstore Sales Performance Analysis

End-to-end business analysis project using **PostgreSQL, Python, and Power BI** to evaluate revenue growth, profitability trends, customer concentration, and the impact of discounting.

This project demonstrates a full analytical workflow:

Raw Data → SQL Validation → Python Analysis → Business Insights → Executive Dashboard

---

# Tools & Technologies

- PostgreSQL
    
- pgAdmin 4
    
- Python (Pandas, Matplotlib, Seaborn)
    
- Power BI
    

---

# Data Preparation

The raw CSV dataset was imported into PostgreSQL and cleaned before analysis.

Data preparation steps:

- Imported dataset into PostgreSQL
    
- Resolved encoding issues during import
    
- Converted date fields to proper DATE format
    
- Converted Sales, Profit, Discount, and Quantity to numeric types
    
- Validated totals after transformation
    
- Ensured correct data types inside Power BI
    

Proper data typing ensured accurate aggregations, calculations, and reporting consistency across SQL, Python, and Power BI.

---

# SQL Analysis

SQL was used to validate the dataset and answer core business questions through aggregation and grouping.

## 1. What are total sales, total profit, and total quantity sold?

![Total Sales, Profit and Quantity](screenshots/01_total_performance.png)

This query validated overall business performance and confirmed data integrity after import.

---

## 2. Which Region Performs Best?

![Region Performance](screenshots/02_region_analysis.png)

Identified the highest-performing geographic region based on total sales.

---

## 3. Which Category Makes the Most Money?

![Category Profit](screenshots/03_category_profit.png)

Determined which product category generates the highest total profit.

---

## 4. Are Discounts Hurting Profit?

![Discount Impact](screenshots/04_discount_impact.png)

Analyzed the relationship between discount levels and profitability.

---

## 5. Who Are the Top 10 Customers?

![Top Customers](screenshots/05_top_customers.png)

Identified the highest revenue-generating customers.

---

# Python Analysis & Visualization

Python was used for trend analysis, growth comparison, efficiency measurement, and exploratory data analysis.

---

## 6. Is the Business Growing Over Time?

![Monthly Sales and Profit Trend](screenshots/image1.png)

Sales show a consistent upward trend over time. Profit follows revenue growth but displays higher volatility.

---

## 7. Is Profit Growing at the Same Rate as Sales?

![Sales vs Profit Growth](screenshots/image2.png)

Profit growth generally aligns with sales growth, though certain periods indicate margin compression.

---

## 8. Which Categories Are Most Efficient?

![Profit Margin by Category](screenshots/image5.png)

Technology demonstrates the strongest profitability relative to revenue, indicating higher operational efficiency.

---

## 9. Does Discounting Hurt Profit?

![Discount vs Profit](screenshots/image3.png)

Higher discount levels correlate with reduced profit and increased probability of losses.

---

## 10. Is Revenue Concentrated Among Few Customers?

![Customer Revenue Concentration](screenshots/image4.png)

A small group of customers contributes a significant share of total revenue, indicating partial revenue concentration.

---

# Power BI Dashboard

The dataset was imported into Power BI to create an interactive executive dashboard.

Data types were validated and corrected inside the Power BI model.

Key DAX Measures created:

- Total Sales = SUM(Sales)
    
- Total Profit = SUM(Profit)
    
- Total Quantity = SUM(Quantity)
    
- Average Order Value = DIVIDE([Total Sales], DISTINCTCOUNT(Order ID))
    

---

## Sales Performance Dashboard

![Sales Dashboard](screenshots/dashboard1.png)

This dashboard includes:

- KPI cards (Total Sales, Total Profit, Orders, Average Order Value)
    
- Monthly sales trend
    
- Top 10 products by sales
    
- Sales by region
    
- Interactive slicers (Region, Category, Year)
    

---

## Product & Profit Analysis

![Product and Profit Dashboard](screenshots/dashboard2.png)

This dashboard includes:

- Sales vs Profit by category
    
- Impact of discount on profitability
    
- Geographic sales distribution
    

---

# Key Insights

- Revenue demonstrates consistent year-over-year growth.
    
- Profit growth follows revenue but is sensitive to discount levels.
    
- Technology is the most profitable category.
    
- High discount levels significantly reduce margin performance.
    
- Revenue is partially concentrated among top customers.