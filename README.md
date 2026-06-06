# UK_online_retail_transaction
# 🛒 Customer Segmentation & CLV Prediction

> RFM + KMeans clustering, BG/NBD & Gamma-Gamma CLV models, cohort retention, and sales-trend analysis on **1M+ real UK e-commerce transactions** — segmenting customers today and predicting their value tomorrow.

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)
![scikit-learn](https://img.shields.io/badge/scikit--learn-KMeans-orange)
![lifetimes](https://img.shields.io/badge/lifetimes-CLV%20Models-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Seaborn-blueviolet)

---

## 📌 Overview
An end-to-end analytics project that goes from raw, messy transaction data to a **predictive view of customer value** — combining customer segmentation, lifetime-value modeling, cohort retention, and sales-trend analysis.

## 📊 Dataset
**Online Retail II** (UCI ML Repository) — a real UK online retailer, ~1.07M transactions (Dec 2009 – Dec 2011), 8 columns.

## 🔧 Workflow
## 🧹 Data Cleaning
Real messy data handled — removed missing Customer IDs, cancelled orders ('C' invoices), and returns/negative values.
**1,048,575 rows → 793,309 clean rows.**

## 📈 Sales Trends (Monthly & Quarterly)
Analysed revenue over time. Sales **build steadily toward the end of the year**, peaking in the run-up to the holiday season (Q4) — a classic pattern for a gift/homeware retailer.

## 🏆 Best-Selling Products
Ranked the top 10 products by units sold and revenue — a small set of popular decorative/gift items drives a large share of volume.

## 🎯 RFM + Segmentation (KMeans, K=4)
5,860 customers grouped into 4 clear segments (K chosen via the Elbow Method):

| Segment | Customers | Profile |
|---|---|---|
| 🏆 Champions | 1,178 | Recent, frequent, high spend (~£10.8K avg) |
| 🆕 New / Promising | 1,267 | Recent but low frequency |
| ⚠️ At-Risk | 1,452 | Were valuable, now slipping away |
| 😴 Lost / Hibernating | 1,963 | One-time, long inactive |

> Note: KMeans is **unsupervised** — no target variable, so no train/test split. Segments were validated by interpreting their RFM profiles.

## 🔮 CLV Prediction
Used **BG/NBD** (predicts future purchase count) and **Gamma-Gamma** (predicts average spend) to estimate each customer's **3-month Customer Lifetime Value**.
> CLV = BG/NBD × Gamma-Gamma

## 🔁 Cohort Retention Analysis
Grouped customers by their first-purchase month and tracked return rates over time. **Retention drops sharply after the first month** — most first-time buyers don't return immediately — but a **loyal core keeps purchasing** across many months.

## 💡 Key Insights
- **Champions are the smallest group (1,178) yet generate ~73% of total revenue** — losing one Champion ≈ losing ~33 Lost customers.
- **Revenue is highly seasonal**, peaking toward Q4 (holiday demand).
- **First-month retention is the biggest leak** — early re-engagement matters most.

## 🎯 Marketing Strategy
- 🏆 Champions → reward & protect (VIP, loyalty)
- 🆕 New → nurture toward 2nd/3rd purchase
- ⚠️ At-Risk → urgent win-back campaigns
- 😴 Lost → low-cost reactivation only

## 🛠️ Tech Stack
Python · Pandas · scikit-learn (KMeans) · lifetimes (BG/NBD, Gamma-Gamma) · Matplotlib · Seaborn
*(Note: `lifetimes` is in maintenance mode; `pymc-marketing` is the modern alternative.)*

## 🎓 Skills Demonstrated
Real data cleaning · Sales-trend analysis · RFM analysis · Unsupervised ML (clustering) · Probabilistic CLV modeling · Cohort/retention analysis · Customer analytics · Business strategy

## 👤 Author
**Talha** — aspiring Data Analyst (Slough, UK)
