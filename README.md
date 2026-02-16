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

This query aggregates total sales (€2.30M), total profit (€286K), and total quantity sold (37,873 units). These metrics provide a high-level performance overview and serve as baseline KPIs for further regional, category, and customer-level analysis.

---

## 2. Which Region Performs Best?

![Region Performance](screenshots/02_region_analysis.png)

This query aggregates total sales and profit by region to evaluate geographic performance. The West region generated the highest revenue (€725K) and profit (€108K), followed by the East region. The South region showed the lowest overall performance, indicating potential opportunities for growth or operational improvement.

---

## 3. Which Category Makes the Most Money?

![Category Profit](screenshots/03_category_profit.png)

This query aggregates total sales and profit by product category to evaluate profitability performance. Technology generated the highest total profit (€145K) and revenue (€836K), followed by Office Supplies. Furniture produced strong revenue but significantly lower profit (€18K), indicating lower margins and potential pricing or cost structure issues.

---

## 4. Are Discounts Hurting Profit?

![Discount Impact](screenshots/04_discount_impact.png)

This query evaluates the impact of discount levels on average profit per order. Results show that profitability declines significantly as discounts increase. While low discounts (0–10%) maintain positive average profit, discounts above 30% lead to negative average profit, indicating that aggressive discounting directly erodes margins.

---

## 5. Who Are the Top 10 Customers?

![Top Customers](screenshots/05_top_customers.png)

This query identifies the top 10 customers ranked by total revenue contribution. The results highlight a small group of high-value customers who generate a disproportionately large share of total sales, indicating revenue concentration among key accounts.

---

# Python Analysis & Visualization

Python was used for trend analysis, growth comparison, efficiency measurement, and exploratory data analysis.

---

## 6. Is the Business Growing Over Time?

![Monthly Sales and Profit Trend](screenshots/image1.png)

Monthly sales demonstrate a clear upward trend, indicating overall business growth over time. Profit also increases alongside revenue but exhibits greater volatility, suggesting margin sensitivity and cost fluctuations across periods.

---

## 7. Is Profit Growing at the Same Rate as Sales?

![Sales vs Profit Growth](screenshots/image2.png)

While profit growth generally follows revenue growth, the higher volatility in profit suggests that margins are sensitive to operational factors such as discounting and cost structure. This indicates that revenue growth does not consistently translate into proportional profitability gains.

---

## 8. Which Categories Are Most Efficient?

![Profit Margin by Category](screenshots/image5.png)

Technology and Office Supplies maintain strong profit margins, demonstrating efficient revenue conversion. However, Furniture underperforms significantly in margin terms, indicating structural profitability challenges that may require pricing or cost optimization strategies.

---

## 9. Does Discounting Hurt Profit?

![Discount vs Profit](screenshots/image3.png)

There is a strong negative correlation between discount depth and profit. Orders with high discount levels (40%+) consistently generate lower margins and often result in losses, indicating aggressive discounting erodes profitability and may require pricing optimization.

---

## 10. Is Revenue Concentrated Among Few Customers?

![Customer Revenue Concentration](screenshots/image4.png)

The analysis indicates revenue concentration among a limited number of high-value customers. While the business benefits from strong key accounts, reliance on a small customer segment may expose the company to revenue volatility if those relationships decline.

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

- **Revenue Growth:** The business shows a clear upward trend in total sales over time, indicating sustained demand and overall expansion.
    
- **Profit Volatility:** While revenue is growing, profit does not increase at the same rate. Periods of margin compression suggest operational or pricing inefficiencies.
    
- **Regional Performance:** The West region leads in both sales and profitability, while other regions present optimization opportunities.
    
- **Category Efficiency:** Technology delivers the highest profit margin, demonstrating strong operational efficiency. Furniture, despite solid sales, generates significantly lower margins.
    
- **Discount Impact:** Higher discount levels strongly correlate with reduced profitability. Aggressive discounting frequently results in margin erosion and, in some cases, losses.
    
- **Customer Concentration:** A small group of top customers contributes a notable share of revenue, introducing moderate revenue concentration risk.