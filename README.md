# 💳 Credit Risk & Loan Default Analytics

![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-3776AB?style=for-the-badge&logo=apachespark&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta_Lake-00ADD8?style=for-the-badge)
![Credit Risk](https://img.shields.io/badge/Credit_Risk-6A1B9A?style=for-the-badge)
![Data Analytics](https://img.shields.io/badge/Data_Analytics-1565C0?style=for-the-badge)

## 📖 Overview

This project analyzes credit risk and loan portfolio performance using a synthetic dataset containing 10,000 loan records.

Developed with PySpark, SQL, and Databricks, the project implements a Medallion Architecture to transform raw loan data into analytical datasets, evaluate default patterns, measure financial exposure, and generate business insights through interactive dashboards.

The main objective is to identify risk patterns across customer profiles and loan characteristics, supporting data-driven credit risk assessment.

---

# 🎯 Business Objectives

- Analyze loan portfolio performance and default behavior.
- Measure default rates and financial exposure.
- Identify credit risk patterns across customer income and credit score categories.
- Evaluate default behavior across different loan purposes.
- Develop analytical KPIs to support credit risk assessment.
- Build an interactive dashboard for business intelligence.

---

# 🏗️ Data Architecture

The project follows the **Medallion Architecture**, organizing data into three layers:

### 🥉 Bronze Layer — Raw Data

- Stores the original synthetic loan dataset.
- Preserves raw records for further processing.
- Uses Delta Lake for structured data storage.
- Table: `credit_risk_bronze`.

### 🥈 Silver Layer — Data Cleaning & Transformation

- Removes duplicate loan records.
- Handles missing critical information.
- Applies data validation rules.
- Creates analytical categories for credit score, income, and loan amount.
- Table: `credit_risk_silver`.

### 🥇 Gold Layer — Business Analytics

Creates aggregated analytical tables to support reporting and dashboard development:

- `credit_risk_gold_kpis`
- `credit_risk_gold_score`
- `credit_risk_gold_income`
- `credit_risk_gold_purpose`

---

# 🚀 Technologies Used

- Databricks
- Apache Spark
- PySpark
- SQL
- Delta Lake
- Databricks AI/BI Dashboards
- Git & GitHub

---

# 📁 Project Structure

```bash
credit-risk-loan-default-analytics/
│
├── notebooks/
│   └── credit_risk_analytics.py
│
├── dashboard/
│   └── credit_risk_dashboard.json
│
├── docs/
│   ├── dashboard_screenshot.png
│   └── data_dictionary.md
│
├── README.md
└── .gitignore
```

---

# 📊 Dataset

The project uses a synthetically generated dataset containing **10,000 loan records**.

The Silver layer contains 14 analytical columns:

| Feature | Description |
|---|---|
| Loan ID | Unique loan identifier |
| Age | Customer age |
| Annual Income | Customer annual income |
| Credit Score | Customer credit score |
| Loan Amount | Total borrowed amount |
| Loan Purpose | Purpose of the loan |
| Employment Type | Customer employment category |
| Debt-to-Income | Debt-to-income ratio |
| Interest Rate | Applied loan interest rate |
| Default Flag | Default indicator |
| Loan Status | Loan default classification |
| Credit Score Category | Credit score segmentation |
| Income Category | Income segmentation |
| Loan Amount Category | Loan amount segmentation |

No real customer or financial records are used.

---

# 📈 Key Performance Indicators

The following KPIs were developed to evaluate portfolio performance and credit risk exposure.

| KPI | Result |
|---|---:|
| Total Loans | 10,000 |
| Default Loans | 2,108 |
| Default Rate | 21.08% |
| Total Loan Amount | BRL 256.50M |
| Default Exposure | BRL 52.73M |
| Default Exposure Rate | 20.56% |

*Financial amounts are presented in BRL.*

---

# 🔍 Exploratory Data Analysis & Business Insights

## 1. Credit Score Analysis

| Credit Score Category | Default Rate |
|---|---:|
| Low Score | 30.42% |
| Medium Score | 18.92% |
| High Score | 7.61% |

Low-score borrowers present approximately **four times the default rate** of high-score borrowers.

This indicates a strong relationship between credit score segmentation and loan default behavior.

---

## 2. Income Analysis

| Income Category | Default Rate |
|---|---:|
| Low Income | 21.71% |
| High Income | 21.21% |
| Medium Income | 20.54% |

Default rates remain relatively similar across income categories, suggesting that income alone does not explain credit default behavior.

---

## 3. Loan Purpose Analysis

| Loan Purpose | Default Rate |
|---|---:|
| Home Improvement | 22.14% |
| Personal | 21.49% |
| Debt Consolidation | 21.30% |
| Education | 19.93% |

Home Improvement loans show the highest default rate, while Education loans show the lowest among the analyzed categories.

---

## 4. Financial Exposure Analysis

Low Score borrowers account for approximately **BRL 39.13 million** in default exposure, representing 29.90% of their total loan volume.

In comparison, High Score borrowers present a default exposure rate of 7.52%.

This highlights the importance of credit score segmentation when evaluating financial risk and potential portfolio losses.

---

# 📊 Databricks Dashboard

An interactive dashboard was developed using Databricks AI/BI Dashboards to monitor loan portfolio performance and visualize key credit risk indicators.

The dashboard includes:

- Total Loans and Default Loans.
- Overall Default Rate.
- Total Loan Amount and Default Exposure.
- Default Rate by Credit Score Category.
- Default Rate by Income Category.
- Default Rate by Loan Purpose.
- Financial Exposure Analysis.

Dashboard metrics were validated against SQL queries to ensure analytical consistency.

### Dashboard Preview

![Credit Risk Dashboard](docs/dashboard_screenshot.png)

---

# 🧪 Data Quality & Validation

The Silver layer applies data quality rules to ensure analytical consistency.

Validation results:

- 10,000 records processed.
- 0 missing critical records.
- 0 duplicate loan IDs.
- 14 columns in the transformed dataset.
- Consistent default classifications between `default_flag` and `loan_status`.

Default distribution:

| Loan Status | Total Loans | Percentage |
|---|---:|---:|
| Non-Default | 7,892 | 78.92% |
| Default | 2,108 | 21.08% |

---

# 💼 Business Value

This analysis demonstrates how data engineering and analytics can support credit risk monitoring by:

- Identifying customer segments with higher default rates.
- Measuring financial exposure across risk categories.
- Comparing default behavior across loan purposes.
- Supporting portfolio monitoring through analytical KPIs.
- Improving visibility into credit risk patterns.

---

# 🎯 Project Goals

This project demonstrates practical skills in:

- Data Engineering
- Medallion Architecture
- Data Cleaning & Transformation
- PySpark
- SQL Analytics
- Delta Lake
- Data Quality & Validation
- Credit Risk Analysis
- Financial Analytics
- Dashboard Development
- Business Intelligence

---

# 📌 Future Improvements

Potential future enhancements:

- Predictive credit default modeling using Machine Learning.
- Advanced customer risk segmentation.
- Model performance evaluation.
- Automated data quality monitoring.
- Integration with external financial datasets.
- Advanced credit portfolio risk indicators.

---

*Created by Brenda Espinosa*
