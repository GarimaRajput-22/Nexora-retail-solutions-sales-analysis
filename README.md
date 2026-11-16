Nexora Retail Solutions: Sales Analysis Dashboard (2020-2026)

An interactive Excel dashboard that analyzes six years of retail sales, profit, returns, and target performance for Nexora Retail Solutions. Built with Power Query, Power Pivot (star schema), and DAX.

Dashboard Preview

Table of Contents
Project Overview
Business Questions
Tools and Skills
Data Model
Key DAX Measures
Dashboard Features
Key Insights
Recommendations
Repository Structure
How to Use
Author
Project Overview

Nexora Retail Solutions sells Furniture, Electronics, and Office Supplies across five regions. This project turns raw transactional data into a single-page dashboard so decision-makers can track performance, spot problems, and filter results by category, sub-category, region, and time.

Dataset scope: 500,000 orders | 10,000 customers | 2.75M units sold | 2020-2026

Business Questions
How are sales and profit performing overall, and is profit growing year over year?
Which regions, categories, and products drive the most revenue?
Which payment methods do customers prefer?
How large is the return problem?
Is the business meeting its sales targets?
Tools and Skills
Tool	Used for
Power Query	Data cleaning, transformation, and loading
Power Pivot	Data modeling (star schema) and relationships
DAX	KPI and time-intelligence measures
Excel	PivotTables, charts, slicers, timeline, dashboard layout
Data Model

The data is modeled as a star schema: one central sales fact table linked to dimension tables.

            Product
               |
Region ---- Sales (Fact) ---- Date
               |
          (other dimensions)

Update this diagram to match your Power Pivot diagram view (for example, add Customer or Payment Method if you modeled them as separate tables).

Key DAX Measures
DAX
Total Sales    = SUM ( Sales[Sales_Amount] )
Total Profit   = SUM ( Sales[Profit] )
Profit Margin  = DIVIDE ( [Total Profit], [Total Sales] )
Avg Order Value = DIVIDE ( [Total Sales], [Total Orders] )
Total Orders   = DISTINCTCOUNT ( Sales[Order_ID] )
Return Rate    = DIVIDE ( [Total Returns], [Total Orders] )

Replace table and column names with the ones in your model, and add your Sales vs Target and YoY Profit measures here.

Dashboard Features
8 KPI cards: Total Sales, Total Profit, Average Order Value, Profit Margin, Return Rate, Total Returns, Total Orders, Total Customers, Total Quantity
YoY Growth in Profit: line chart of profit trend across 2020-2026
Sales by Region: Central, East, North, South, West
Sales by Payment Method: UPI, Net Banking, Cash, Card
Top Products: Chair, Desk, Laptop, Notebook, Pen
Sales vs Target: yearly actual sales against target
Category Performance: Electronics, Furniture, Office Supplies
Interactive filters: slicers for Category, Sub-Category, and Region, plus a Date timeline. All charts update together.
Key Insights
Metric	Finding
Total Sales	₹74.48 billion
Total Profit	₹14.44 billion (profit margin 19.38%)
Average Order Value	₹33,955
Return Rate	33.28% (166,385 returns out of 500,000 orders), which is high
Regional Sales	Evenly spread at about ₹14.8B-₹14.9B per region; gap between best and worst is under 1%
Top Products	Desk (~₹12.9B), Pen and Notebook (~₹12.6B); Laptop is weakest at ~₹6.75B
Category Mix	Balanced: Electronics, Furniture, and Office Supplies each contribute roughly one third
Payment Methods	Nearly equal at about ₹18.6B each (UPI, Net Banking, Cash, Card); cash is still significant
Profit Trend	Flat year over year at about ₹2.04B-₹2.08B per year, with no clear upward trend
Sales vs Target	Actual sales of ~₹10.5B-₹10.7B per year against a ~₹13.99B target, missing targets by roughly 24%
Recommendations
Reduce the return rate. At 33%, returns are the biggest risk to profit. Investigate returns by product, category, and region.
Close the sales-target gap. Targets are consistently missed by about 24%, so either improve execution or revisit target setting.
Push Laptop sales. Laptop is the weakest product and offers the most room to grow.
Find levers to break the flat profit trend. Look at pricing, discounts, and product mix.
