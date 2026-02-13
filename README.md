📊 Customer RFM Analysis with SQL & Python
🚀 Overview

This project performs an end-to-end **Customer RFM (Recency, Frequency, Monetary) Analysis** using Python and SQL.

The goal is to move from raw transactional data to actionable customer segments by:

• Loading CSV data into a relational database

• Writing optimized SQL queries using CTEs

• Calculating RFM metrics

• Scoring customers using quartile ranking

• Segmenting customers into business categories

• Visualizing behavioral patterns and revenue concentration

This project demonstrates database handling, SQL aggregation, and analytical storytelling.

🏗️ **Project Architecture**
CSV Files → SQLite Database → SQL (CTEs) → RFM Metrics → Scoring → Segmentation → Visualization

📂 **Dataset**

The project uses three structured tables:

• orders

• order_items

• customers

Total customers analyzed: **2,172**

🧮 Step 1: ** Database Setup**

• Created SQLite database using SQLAlchemy

• Loaded CSV files into relational tables

• Converted date columns to proper datetime format

• Ensured referential joins between orders and order_items

This ensures computations happen efficiently inside the database.

🧠 **Step 2: RFM Calculation (Using SQL CTEs)**

Customer metrics were calculated directly inside SQL using:

• Order joins

• Aggregations

• Grouping

• CTE structure for readability and performance

Metrics computed:

• Recency → Days since last purchase

• Frequency → Total distinct orders

• Monetary → Total revenue generated

**📊 RFM Statistics Summary**
| Metric    | Min | Max     | Mean   |
| --------- | --- | ------- | ------ |
| Recency   | 1   | 600     | 207    |
| Frequency | 1   | 9       | 2.3    |
| Monetary  | $12 | $10,533 | $2,289 |


**🔢 Step 3: RFM Scoring**

Each metric was scored using quartiles (1–4 scale):

• Lower Recency → Higher Score

• Higher Frequency → Higher Score

• Higher Monetary → Higher Score

Final RFM Score Range:
**3 → 12**

**🏷️ Step 4: Customer Segmentation**

Customers were grouped into meaningful business segments:

• 🏆 Champions

• 🤝 Loyal Customers

• 🌱 Potential Loyalists

• ⚠️ Need Attention

• ❌ Lost

**📈 Segment Distribution
Customer Distribution by Segment**
<img width="1188" height="583" alt="image" src="https://github.com/user-attachments/assets/e3f0edeb-36f0-4cf6-9154-ffbf325ff552" />

**Revenue Contribution by Segment**
<img width="1162" height="587" alt="image" src="https://github.com/user-attachments/assets/f6772cb6-6855-4ba4-b905-c44768678f51" />

**🔎 Key Insight**

Champions represent a minority of customers but generate the majority of revenue.

Revenue Contribution:
| Segment         | Revenue % |
| --------------- | --------- |
| Champions       | 61%       |
| Loyal Customers | 21%       |
| Others Combined | 18%       |


**📉 Behavioral Analysis
Recency Distribution**
<img width="1155" height="691" alt="image" src="https://github.com/user-attachments/assets/b873af2d-5047-4d9e-b504-3b27e950482f" />
**Frequency Distribution**
<img width="1155" height="686" alt="image" src="https://github.com/user-attachments/assets/9dc55bce-300b-474e-9b37-0fc9f824d3e1" />
**Monetary Distribution**
<img width="1162" height="698" alt="image" src="https://github.com/user-attachments/assets/5e0887a8-36a3-4ba6-a18b-a2ec2071576b" />

**📊 Relationship Analysis**
**Recency vs Monetary**
<img width="1172" height="699" alt="image" src="https://github.com/user-attachments/assets/2e15c95f-5b20-4991-849c-4f42ab30a859" />
**Frequency vs Monetary**
<img width="1167" height="697" alt="image" src="https://github.com/user-attachments/assets/91b751ed-ae14-4bc3-a860-cb07bfcc977f" />

**🏆 Top Customer Analysis**
• Identified Top 20 customers by RFM score

• Identified Top 10 customers by total revenue

• Measured revenue concentration percentage

Top 10 customers contribute ~2% of total revenue.

**🛠️ Tech Stack**

• Python

• Pandas

• NumPy

• Matplotlib

• Seaborn

• SQL (CTEs, Aggregations)

• SQLite

• SQLAlchemy




