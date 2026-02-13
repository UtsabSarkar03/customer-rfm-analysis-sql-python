📊 Customer RFM Analysis using SQL & Python
🚀 Project Overview

This project implements an end-to-end Customer RFM (Recency, Frequency, Monetary) Analysis using:

Python for data processing & visualization

SQLite as a relational database

SQL (with CTEs) for metric calculation

Statistical segmentation techniques

The goal is to identify high-value customers, segment them based on purchasing behavior, and analyze revenue contribution across segments.

🎯 Objective

To transform raw transactional data into actionable customer segments by:

Loading structured CSV data into a relational database

Computing RFM metrics using optimized SQL queries

Scoring customers using quartile-based ranking

Segmenting customers into business-friendly categories

Visualizing behavioral patterns

🏗️ Project Workflow
1️⃣ Database Setup

Created SQLite database

Established SQLAlchemy engine connection

Structured relational tables:

orders

order_items

customers

2️⃣ Data Loading

Imported CSV files into pandas

Converted date columns to datetime format

Loaded tables into SQLite database

Verified row counts and schema consistency

3️⃣ RFM Table Creation (SQL with CTEs)

Used SQL Common Table Expressions (CTEs) to:

Join orders and order_items

Calculate total sales per order

Aggregate customer-level metrics:

Last purchase date

Order frequency

Total revenue (Monetary)

This ensures computation happens efficiently inside the database layer.

4️⃣ RFM Metric Calculation

From SQL output:

Recency → Days since last purchase

Frequency → Number of distinct orders

Monetary → Total customer spending

Dataset size:

2,172 customers analyzed

📈 RFM Statistics Summary
Metric	Min	Max	Mean
Recency	1 day	600 days	207 days
Frequency	1 order	9 orders	2.3 orders
Monetary	$12	$10,533	$2,289

Key observation:

Majority customers purchased only 1–3 times

Small group contributes disproportionately high revenue

🔢 RFM Scoring Methodology

Each metric scored on a quartile-based 1–4 scale:

Recency → Lower is better

Frequency → Higher is better

Monetary → Higher is better

Final RFM Score Range:
3 (Lowest) → 12 (Highest)

Segment identifier example:
R=4, F=4, M=4 → 444

🏷️ Customer Segmentation

Customers were grouped into business categories:

🏆 Champions

🤝 Loyal Customers

🌱 Potential Loyalists

⚠️ Need Attention

❌ Lost

📊 Segment Insights
| Segment             | Customers | Revenue Contribution |
| ------------------- | --------- | -------------------- |
| Champions           | 833       | 61.3%                |
| Loyal Customers     | 527       | 21.2%                |
| Potential Loyalists | 455       | 11.9%                |
| Need Attention      | 229       | 3.7%                 |
| Lost                | 128       | 1.6%                 |


🔎 Insight:

Champions (≈38% of customers) generate over 61% of total revenue.

This highlights strong customer concentration.

📉 Behavioral Distribution Analysis

Additional analysis included:

Recency distribution histogram

Frequency distribution histogram

Monetary distribution histogram

Segment-wise revenue breakdown

Scatter plots:

Recency vs Monetary

Frequency vs Monetary

Recency vs Frequency

Top 20 customers by RFM score

Top 10 customers by revenue

🛠️ Tech Stack

Python

Pandas

NumPy

Matplotlib

Seaborn

SQL (CTEs, Aggregations)

SQLite

SQLAlchemy

📁 Repository Structure
├── data/
│   ├── orders.csv
│   ├── order_items.csv
│   └── customers.csv
│
├── notebooks/
│   └── rfm_analysis.ipynb
│
├── database/
│   └── sales_analysis.db
│
└── README.md

💡 Key Skills Demonstrated

Relational database modeling

SQL aggregation using CTEs

Customer behavioral analytics

Statistical segmentation (quartile scoring)

Revenue concentration analysis

Data visualization

End-to-end analytical workflow

🔮 Potential Improvements

Automate RFM refresh process

Convert to scheduled pipeline

Deploy to cloud database

Build interactive dashboard (Power BI / Tableau)

Implement K-Means clustering for advanced segmentation
