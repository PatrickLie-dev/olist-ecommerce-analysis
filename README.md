# Olist E-Commerce Analysis
**End-to-end data analysis of 100K+ Brazilian e-commerce orders using SQL, Python, and dashboard visualization.**

[![SQL](https://img.shields.io/badge/SQL-MySQL-blue)](https://www.mysql.com/)
[![Python](https://img.shields.io/badge/Python-3.x-green)](https://www.python.org/)
[![Dataset](https://img.shields.io/badge/Dataset-Olist%20Kaggle-orange)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
[![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)]()

---

## Project Overview
This project analyzes the [Olist Brazilian E-Commerce dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) — a real-world dataset of 100,000+ orders from 2016–2018. The goal is to extract actionable business insights across sales, logistics, customer behavior, and seller performance.

**Business Questions Answered:**
- What are the top-selling product categories and revenue drivers?
- How does delivery speed impact customer satisfaction?
- Which customer segments have the highest lifetime value?
- What is the month-over-month revenue growth trend?
- What percentage of orders are delivered late, and what is the impact?

---

## Key Findings
| Insight | Finding |
|---|---|
| Overall late delivery rate | **8.11%** of orders arrive after estimated date |
| Impact of late delivery | Orders 30+ days late receive avg review score of **2.20/5** vs **4.41** for fast delivery |
| Top product category | **Bed, Bath & Table** — 11,115 items sold |
| Customer retention | Only **3.12%** of customers make a repeat purchase |
| Revenue growth | **+20% YoY** from 2017 to 2018 |
| Best reviewed category | **Books (General Interest)** — avg score 4.45/5 |
| Top customer state | **São Paulo (SP)** — 41.9% of all customers |

---

## Tech Stack
| Tool | Purpose |
|---|---|
| MySQL 8.0 | Data storage, querying, transformation |
| MySQL Workbench | SQL development environment |
| Python (Pandas, SQLAlchemy) | Data loading, EDA |
| Power BI / Looker Studio | Dashboard visualization |
| Git & GitHub | Version control |

---

## Repository Structure
```
olist-ecommerce-analysis/
│
├── sql/
│   └── olist_sql_query_bank.sql     # 21 SQL queries (Beginner → Advanced)
│
├── notebooks/
│   └── olist_eda.ipynb              # Python EDA notebook (coming soon)
│
├── dashboard/
│   └── olist_dashboard.pdf          # Dashboard export (coming soon)
│
├── data/
│   └── README.md                    # Dataset source info (data not included)
│
└── README.md
```

---

## SQL Query Bank
The `sql/` folder contains **21 production-ready queries** organized by difficulty:

**Beginner (Q1–Q8)** — Core aggregations and grouping
- Total orders, revenue, and avg review score
- Order status breakdown
- Top 10 product categories by sales
- Payment method preferences

**Intermediate (Q9–Q15)** — Joins, date functions, CASE WHEN
- Monthly revenue trend (2016–2018)
- Average delivery time by state
- Delivery speed vs. review score correlation
- Late delivery rate calculation
- Repeat vs. one-time customer segmentation

**Advanced (Q16–Q21)** — CTEs and Window Functions
- RFM customer segmentation (Champions, Loyal, At Risk, Lost)
- Month-over-month revenue growth with `LAG()`
- Cumulative revenue with `SUM() OVER()`
- Top 3 sellers per state using `RANK() OVER(PARTITION BY)`
- Cohort retention analysis with `FIRST_VALUE()`

---

## Dataset
- **Source:** [Kaggle — Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **Size:** ~100,000 orders, 9 relational tables
- **Period:** September 2016 – October 2018
- **Note:** Raw data files not included in this repository. Download directly from Kaggle.

---

## How to Run

### 1. Setup Database
```bash
# Install dependencies
pip install pandas sqlalchemy pymysql

# Load CSVs into MySQL
python load_olist_to_mysql.py
```

### 2. Run SQL Queries
Open `sql/olist_sql_query_bank.sql` in MySQL Workbench and execute queries individually or in sequence.

### 3. Run EDA Notebook
```bash
jupyter notebook notebooks/olist_eda.ipynb
```

---

## Author
**Patrick Lie** | Fresh IT Graduate — BSc Information Technology (IoT), Asia Pacific University  
Actively seeking Junior Data Analyst roles in Jakarta, Indonesia.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/patrick-lie-315964302/)
[![GitHub](https://img.shields.io/badge/GitHub-PatrickLie--dev-black)](https://github.com/PatrickLie-dev)
