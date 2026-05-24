# 📊 ApexPlanet Internship – Task 2: EDA & Business Intelligence

---

## 📌 Objective

To uncover patterns, trends, and relationships within the Delinquency Prediction Dataset using statistical analysis, SQL queries, and advanced visualizations — and to propose a key metrics dashboard for business stakeholders.

---

## 📂 Repository Structure

```
ApexPlanet-DataAnalytics-Task2/
│
├── ApexPlanet_Task2_EDA.ipynb        # Main Jupyter Notebook (all steps)
├── delinquency.db                    # SQLite database with SQL query results
├── eda_final_dataset.csv             # Dataset with engineered features
│
├── plots/
│   ├── hist_age.png
│   ├── hist_credit_score.png
│   ├── bar_delinquent.png
│   ├── bar_employment.png
│   ├── bar_card_type.png
│   ├── heatmap_correlation.png
│   ├── scatter_credit_missed.png
│   ├── boxplot_income.png
│   ├── boxplot_utilization.png
│   ├── pairplot.png
│   ├── stacked_employment_delinquency.png
│   └── bar_payment_reliability.png
│
└── README.md
```

---

## 🗂️ Dataset Overview

| Property | Details |
|---|---|
| **Dataset** | Delinquency Prediction Dataset |
| **Records** | 500 customers |
| **Features** | 19 columns |
| **Target** | `Delinquent_Account` (0 = Not Delinquent, 1 = Delinquent) |
| **Domain** | Banking / Financial Risk Analytics |

---

## 📈 Step 1 — Descriptive Statistics & Univariate Analysis

Key statistics computed for all 19 columns:

| Metric | Value |
|---|---|
| Total Customers | 500 |
| Delinquent Accounts | 80 (16%) |
| Not Delinquent | 420 (84%) |
| Avg Credit Score | ~490 |
| Avg Missed Payments | ~2.5 |
| Avg Annual Income | ~$95,000 |
| Avg Debt-to-Income Ratio | ~0.48 |

**Charts Created:**
- Age Distribution Histogram
- Credit Score Distribution Histogram
- Delinquent vs Not Delinquent Bar Chart
- Employment Status Breakdown
- Credit Card Type Distribution

---

## 🗄️ Step 2 — SQL Business Questions

The dataset was loaded into a **SQLite database** (`delinquency.db`) and 5 business questions were answered using SQL:

| # | Business Question |
|---|---|
| Q1 | What is the delinquency rate by Employment Status? |
| Q2 | What is the avg Credit Score & Income of delinquent vs non-delinquent customers? |
| Q3 | Which city has the highest number of delinquent accounts? |
| Q4 | Which credit card types are most associated with delinquency? |
| Q5 | Do customers with high Debt-to-Income ratio miss more payments? |

**SQL techniques used:** `GROUP BY`, `CASE WHEN`, `AVG()`, `SUM()`, `COUNT()`, `ORDER BY`

---

## 🔥 Step 3 — Multivariate Analysis & Correlation

Advanced visualizations to explore relationships between variables:

| Chart | Variables | Key Finding |
|---|---|---|
| Correlation Heatmap | All numeric features | `Missed_Payments` strongest predictor |
| Scatter Plot | Credit Score vs Missed Payments | Lower score + more misses = delinquent |
| Pair Plot | Credit Score, Income, Missed Payments, DTI | Clear delinquent clusters |
| Box Plot | Income by Delinquency | Delinquents have lower median income |
| Stacked Bar | Employment Status by Delinquency | Unemployed highest risk group |

**Feature Engineering:**
- `Total_Late_Missed` — total Late + Missed months across Month_1 to Month_6
- `OnTime_Count` — number of On-time payments across 6 months
- `Payment_Reliability_Score` — ratio of on-time payments (0 to 1)
|
---

## 🔍 Top 5 Key Insights

1. **Class Imbalance** — Only 16% of customers are delinquent; future models must address this.
2. **Missed Payments = Top Risk Factor** — The single strongest predictor of delinquency.
3. **Credit Score is Protective** — Higher credit scores strongly correlate with lower delinquency.
4. **Unemployment Drives Risk** — Unemployed customers show the highest delinquency rate.
5. **Payment History Matters** — Customers with low Payment Reliability Score are far more likely to default.

---

## ⚙️ How to Run

```bash
# Install dependencies
pip install pandas matplotlib seaborn

# Open notebook in VS Code or Jupyter
jupyter notebook ApexPlanet_Task2_EDA.ipynb
```

Place `Delinquency_prediction_dataset.csv` in the same folder before running.

---

## 🛠️ Tools & Technologies

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-EDA-green?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Charts-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-9cf)
![SQLite](https://img.shields.io/badge/SQLite-SQL%20Queries-lightblue?logo=sqlite)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

---

## 🎥 LinkedIn Video Walkthrough

> 📹 *[https://www.linkedin.com/posts/upputhollakeerthisaikumar_dataanalytics-eda-sql-activity-7464136642266808320-yxcH?utm_source=share&utm_medium=member_desktop&rcm=ACoAAERiNqUBFwhaq-h8hxYboSpaMhxsFz0hk6I]*

---

## 🏢 About ApexPlanet

[ApexPlanet Software Pvt. Ltd.](https://www.apexplanet.in) is dedicated to driving innovation in digital solutions and nurturing the next generation of tech talent through hands-on internship programs.
