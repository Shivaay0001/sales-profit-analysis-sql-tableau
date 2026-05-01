# 📊 Sales and Profit Analysis Using SQL and Tableau

## 📌 Project Overview

An end-to-end business intelligence project transforming **150,281 raw sales transactions** (2017–2020) into actionable revenue and profit insights using SQL and Tableau. The project is structured into two independent analytical flows — revenue analysis and profit analysis — each with its own interactive dashboard.

This project covers the full analytics workflow: data backup → cleaning → star schema modeling → SQL analysis → Tableau dashboarding.

**🔗 Live Dashboards:** [View on Tableau Public](https://public.tableau.com/app/profile/atul.dwivedi/vizzes)

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| MySQL / MySQL Workbench | Data import, backup, cleaning, star schema, SQL analysis |
| SQL | Joins, aggregations, window functions, analytical queries |
| Tableau Public | Interactive dashboard creation and visualization |
| CSV Export | Data transfer from MySQL to Tableau |

---

## 📁 Dataset Overview

| Property | Detail |
|----------|--------|
| Total Transactions | 150,281 rows |
| Tables | 5 (1 fact + 4 dimension tables) |
| Time Period | 2017 – 2020 |
| Markets | 17 |
| Customers | 38 |
| Products | 279 |
| Customer Types | Brick & Mortar, E-Commerce |

**Fact Table:** `transactions` — sales_qty, sales_amount, profit, currency  
**Dimension Tables:** `customers`, `products`, `markets`, `date`

---

## ⚙️ Workflow

### 1. Data Backup
- Created backup copies of all raw tables before making any changes
- Ensured raw data could be recovered at any point during transformation

### 2. Data Cleaning & Preprocessing
- Identified and handled zero and negative sales values
- Checked and resolved currency inconsistencies across markets
- Verified null values, duplicate rows in lookup tables
- Standardised text fields for join compatibility

### 3. Data Modeling — Star Schema
- Designed a star schema with `transactions` as the central fact table
- Connected 4 dimension tables: customers, products, markets, date
- Built a final analytical table combining all dimensions and measures for clean Tableau export

### 4. SQL Analysis
Calculated the following business metrics using SQL:
- Total revenue, sales quantity, profit, profit margin %
- Revenue and profit by market
- Revenue by year and monthly trends
- Top 5 customers by revenue
- Top 5 products by revenue
- Customer type contribution (Brick & Mortar vs E-Commerce)

### 5. Tableau Dashboard Creation
- Built 2 separate interactive dashboards with year/month filters
- Added navigation buttons between Revenue and Profit views

---

## 📊 Key Business Metrics

| Metric | Value |
|--------|-------|
| 💰 Total Revenue | ₹986.62M |
| 📦 Total Sales Quantity | 2,431.54K units |
| 📈 Total Profit | ₹24.66M |
| 🏆 Top Market (Revenue) | Delhi NCR — ₹520.77M |
| 🏆 Top Customer | Electricalsara Stores — ₹413.91M |
| ✅ Highest Profit Margin | Surat — 4.86% |
| ❌ Lowest Profit Margin | Bengaluru — **-20.78%** (loss-making) |

---

## 💡 Key Insights

### 🗺️ Market Performance
- **Delhi NCR dominates revenue at ₹520.77M** — more than 3× the second-largest market Mumbai (₹150.18M)
- Delhi NCR also leads in sales volume at 989.90K units sold
- **Revenue and profit margin do not follow the same pattern** — high revenue markets are not always high profit markets

### 📉 Profit vs Revenue Disconnect
- **Bengaluru generates ₹8.81M in revenue but has a -20.78% profit margin** — meaning the company is losing money on every sale in that market
- Surat, despite lower revenue, leads in profit margin at 4.86%
- Total profit of ₹24.66M on ₹986.62M revenue = an overall margin of just ~2.5% — margin management is critical

### 👥 Customer Concentration Risk
- **Electricalsara Stores alone contributes ₹413.91M** — approximately 42% of total revenue
- This creates significant business risk if a single customer relationship weakens
- Top 5 customers account for a disproportionate share of total revenue

### 🛒 Customer Type Split
- **Brick & Mortar: 75.60%** of total revenue
- **E-Commerce: 24.40%** — a growing channel with expansion potential

### 📦 Product Performance
- Top product **Prod065 generates ₹16.26M**, followed by Prod090 (₹13.42M) and Prod239 (₹11.09M)
- Revenue is concentrated in a small number of top-performing products

### 📅 Time Trends
- Sales and profit fluctuate across months and years — time-based monitoring is essential for planning and forecasting

---

## 📸 Dashboard Preview

### Revenue Dashboard
![Revenue Dashboard](revenue_dashboard.png)
*Shows Total Revenue (₹986.62M), Sales Quantity, Revenue by Market, Top 5 Customers & Products, and Revenue by Year*

### Profit Dashboard
![Profit Dashboard](profit_dashboard.png)
*Shows Total Profit (₹24.66M), Profit Margin by Market, Profit Trend over time, and Customer Type split*

---

## 💼 Business Recommendations

1. **Investigate Bengaluru losses** — Review pricing, logistics costs, and operational expenses to address the -20.78% profit margin
2. **Expand in high-margin markets** — Surat, Patna, and Bhubaneswar show stronger profitability efficiency
3. **Reduce customer concentration risk** — Diversify beyond Electricalsara Stores, which alone accounts for ~42% of revenue
4. **Track profit alongside revenue** — Revenue growth without margin tracking can mask loss-making operations
5. **Invest in E-Commerce growth** — Currently at 24.40%, this channel has significant room to scale
6. **Use monthly trend analysis** for inventory planning and sales target setting

---

## 🚀 Future Improvements

- **Sales Forecasting** — Time series models (ARIMA / Prophet) for revenue and profit prediction
- **Customer Segmentation** — RFM (Recency, Frequency, Monetary) analysis for customer lifetime value
- **Live Dashboard** — Automated ETL pipeline with Tableau Server or Power BI for real-time refresh
- **Additional KPIs** — Average order value, customer lifetime value, growth rate by market

---

## 📌 Conclusion

This project demonstrates how raw transactional data can be transformed into a full business intelligence solution. The key finding — that **Bengaluru generates ₹8.81M in revenue but operates at a -20.78% loss** — illustrates why tracking profit margin alongside revenue is critical for sound business decision-making.

The complete workflow covers data backup, cleaning, star schema modeling, SQL-based metric calculation, and interactive Tableau dashboarding across 150,281 transactions and 17 markets.

---

## 📁 Files in This Repository

| File | Description |
|------|-------------|
| `Capstone_project_Queries.sql` | All SQL queries — backup, cleaning, star schema, analysis |
| `MDD_capstone_project.pdf` | Full Model Design Document with methodology and insights |
| `Sales-and-Profit-Analysis-Using-SQL-and-Tableau.pdf` | Project presentation slides |
| `revenue_dashboard.png` | Revenue dashboard screenshot |
| `profit_dashboard.png` | Profit dashboard screenshot |
