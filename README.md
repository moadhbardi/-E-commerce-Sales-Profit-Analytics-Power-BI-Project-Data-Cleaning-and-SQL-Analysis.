📊 E-Commerce Sales & Profit Analytics — Power BI Project
📌 Project Overview

This project analyzes an e-commerce transaction dataset to uncover trends in revenue, profitability, product performance, and customer behavior.
It includes data cleaning, data modeling, DAX measures, and interactive Power BI dashboards designed for business decision-making.

The goal is to transform messy raw data into actionable insights for sales, operations, and marketing teams.

🧹 Data Cleaning & Preparation

The raw CSV dataset contained inconsistencies, missing values, unreadable date formats, and unused variables.
I performed full preprocessing using Excel and Python, including:

✔ Removed irrelevant columns

Removed fields such as product_class and product_size that added no analytical value.

✔ Renamed technical columns

Standardized column names to make the dataset easier to read (e.g., t_id → transaction_id).

✔ Filtered and validated data

Kept only approved transactions.

Removed duplicated values and irrelevant entries.

Checked for missing values and cleaned the final dataset.

✔ Converted date formats

Parsed the transaction date into proper datetime.

Extracted year, month, day, hour, minute for time-based analysis.

✔ Exported a fully cleaned dataset

Saved as CSV.

Loaded into an SQLite database for SQL exploration and validation.

✔ SQL Exploration

I performed several SQL analyses such as:

Top 10 customers by spending

Profit margin filtering

Average list price by brand

Revenue distribution

🧠 Data Modeling (Power BI)

Inside Power BI, I built a star-schema-ready table with clean fields.
Additional transformations included:

✔ Created new calculated columns

Extracted month names

Created profit column:
Profit = List Price – Standard Cost

✔ Built DAX measures for analysis

Main measures include:

Total Revenue

Total Profit

Profit by Brand

Profit by Product Line

Monthly Revenue

Monthly Profit

These measures allow dynamic filtering and slicing inside the report.

📈 Dashboard Structure
1️⃣ Revenue KPI Dashboard

Focuses on business performance from a revenue perspective.

Included Visuals

✔ Total revenue KPI
✔ Revenue by:

Online vs offline order

Order status

Brand

Product line

Month
✔ Pie charts, donut charts, and time-series line charts
✔ Clean background for storytelling

2️⃣ Profit KPI Dashboard

Highlights financial efficiency and product profitability.

Included Visuals

✔ Total profit KPI
✔ Profit by:

Brand

Product line

Month
✔ Donut charts, pie charts, and trend curves
✔ Helps identify high-margin products and seasonal patterns

🔍 Key Insights

Some insights identified from the dashboards:

Standard product line generates the highest revenue and profit.

Some brands perform extremely well in both sales volume and margins.

Profitability fluctuates by month, indicating seasonal demand.

Online orders represent a strong share of total revenue, confirming digital importance.

Certain products exceed 50% profit margin, making them key targets for promotion.

🧰 Tools & Technologies

Excel — early cleaning, inspection

Python (Pandas) — deep cleaning, renaming, date parsing, exporting

SQLite / SQL Queries — validation and exploratory analysis

Power BI — modelling, DAX, interactive dashboards

DAX — calculations for KPIs and breakdowns

🎯 Project Purpose

This project demonstrates my ability to:

Clean and prepare raw business data

Build analytical data models

Perform SQL exploration

Create advanced KPIs using DAX

Design professional Power BI dashboards

Extract insights that support real-world business decisions
