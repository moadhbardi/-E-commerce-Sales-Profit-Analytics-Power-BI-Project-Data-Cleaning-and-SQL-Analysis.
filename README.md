E-Commerce Revenue & Profit Analysis – Power BI Project

A complete end-to-end data analytics project using Excel, Python, Power BI, and DAX

🚀 Project Overview

This project presents a full Business Intelligence workflow built on a real-world E-commerce dataset.
It covers everything from data collection, cleaning, feature engineering, exploratory analysis, DAX measures, and interactive dashboards.

The objective is to deliver an easy-to-read and actionable Revenue & Profit Performance Dashboard for business decision-makers.

🎯 Key Objectives

Analyze total revenue, profit, and order performance

Identify top performing brands & product lines

Compare online vs offline orders

Understand monthly sales trends

Build interactive dashboards with drill-down & filters

Demonstrate a complete BI workflow for employers

📁 Dataset Information

The dataset contains transaction-level E-commerce data, including:

Column	Description
order_id	Unique order identifier
order_date	Date of purchase
brand	Product brand
product_line	Category (Standard, Road, Mountain…)
list_price	Product price before discount
disount_percent	% discount applied
profit	Profit earned per item
online_order	If order was made online
order_status	Approved / Cancelled / Returned…

Data was originally provided in Excel and cleaned using Python.

🧹 Data Cleaning & Preparation
✔ Excel Pre-cleaning

Fixed inconsistent brand names

Checked missing / null values

Removed duplicate records

Standardized date formats

Verified discount formula consistency

🐍 Python Data Cleaning Workflow

Performed using Pandas:

✔ Major steps

Loaded the raw Excel file with pandas.read_excel()

Converted order_date to datetime

Extracted Month column

Replaced incorrect product line categories

Handled negative or impossible values in list_price

Verified profit calculations

Exported a cleaned version used in Power BI

df['order_date'] = pd.to_datetime(df['order_date'])
df['month'] = df['order_date'].dt.month_name()
df['profit'] = df['list_price'] - df['list_price'] * df['discount_percent']

📐 DAX Measures Used in Power BI

Below are the key DAX measures powering the dashboard:

Total Revenue
total_revenue = SUM(dataset[list_price])

Total Profit
Sum of profits = SUM(dataset[profit])

Monthly Revenue
Revenue by Month = CALCULATE(
    SUM(dataset[list_price]),
    ALLEXCEPT(dataset, dataset[month])
)

Online vs Offline Revenue
Revenue Online = CALCULATE(
    SUM(dataset[list_price]),
    dataset[online_order] = TRUE()
)

Profit Margin
Profit Margin = DIVIDE([Sum of profits], [total_revenue])

📊 Power BI Dashboard

Your dashboard consists of two interactive pages:

📍 Page 1 — Revenue KPI Dashboard

Includes the following visuals:

Main KPI Card → Total Revenue

Donut Chart → Revenue by Online vs Offline

Donut Chart → Revenue by Order Status

Pie Chart → Revenue by Brand

Bar Chart → Revenue by Product Line

Line Chart → Monthly Revenue Trend

✔ Insights

Standard product line dominates revenue.

Online orders represent ~50% of total revenue.

Best performing brands generate over 4M each.

Consistent sales peaks in July–August.

📍 Page 2 — Profit KPI Dashboard

Includes:

Main KPI Card → Total Profit

Line Chart → Monthly Profit Trend

Pie Chart → Profit by Brand

Donut Chart → Profit by Product Line

✔ Insights

Standard line drives 74% of total profit

WearzA2B is the most profitable brand (~25%)

Profit seasonality similar to revenue with peaks in Q3

🎨 Design & UX

Improvements applied:

Unified color theme

Transparent card backgrounds

Clean fonts & modern icons

Minimal and centered KPI cards

Drill-down enabled on charts

Filters: Month, Brand, Product Line, Order Status

This makes the dashboard clean, modern, and recruiter-friendly.

📂 Repository Structure
📁 ecommerce-bi-project/
│
├── data/
│   ├── raw_dataset.xlsx
│   └── cleaned_dataset.xlsx
│
├── python-cleaning/
│   └── data_cleaning.ipynb
│
├── powerbi/
│   └── ecommerce_dashboard.pbix
│
├── images/
│   ├── revenue_dashboard.png
│   ├── profit_dashboard.png
│   └── sample_visuals.png
│
└── README.md   ← (this file)

🧪 How to Reproduce

1️⃣ Clone this repository

git clone https://github.com/USERNAME/ecommerce-bi-project.git


2️⃣ Install Python requirements

pip install pandas numpy matplotlib


3️⃣ Open the Power BI file

powerbi/ecommerce_dashboard.pbix


4️⃣ Connect it to cleaned_dataset.xlsx


This project demonstrates:

✔ Data cleaning (Excel + Python)
✔ ETL pipeline understanding
✔ DAX proficiency
✔ KPI design thinking
✔ Business storytelling
✔ Dashboard UX & layout
✔ End-to-end BI execution
