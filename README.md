# Credit Risk & Loan Default Analytics

## Project Overview

This project explores credit risk and loan portfolio performance using a synthetic dataset of 10,000 loan records.

Developed with PySpark, SQL, and Databricks, the project implements a Medallion Architecture to process loan data, evaluate default patterns, measure financial exposure, and generate actionable business insights through interactive dashboards.

## Business Objectives

- Analyze loan portfolio performance and default behavior.
- Measure default rates and financial exposure.
- Identify credit risk patterns across customer income and credit score categories.
- Evaluate default behavior across different loan purposes.
- Develop analytical KPIs to support data-driven credit risk assessment.

## Data Architecture

The project follows the Medallion Architecture:

**1. Bronze Layer — Raw Data**

- Stores the original synthetic loan dataset.
- Uses Delta Lake for structured data storage.
- Table: `credit_risk_bronze`.

**2. Silver Layer — Data Cleaning and Transformation**

- Removes duplicate loan records.
- Handles missing critical information.
- Applies business validation rules.
- Creates analytical categories for credit score, income, and loan amount.
- Table: `credit_risk_silver`.

**3. Gold Layer — Business Analytics**

Creates aggregated analytical tables to support reporting and dashboard development:

- `credit_risk_gold_kpis`
- `credit_risk_gold_score`
- `credit_risk_gold_income`
- `credit_risk_gold_purpose`

## Technologies

- Databricks
- Apache Spark
- PySpark
- SQL
- Delta Lake
- Databricks Dashboards

## Dataset

The project uses a synthetically generated dataset containing 10,000 loan records.

The dataset includes:

- Loan ID
- Customer age
- Annual income
- Credit score
- Loan amount
- Loan purpose
- Employment type
- Debt-to-income ratio
- Interest rate
- Default indicator
- Loan status

No real customer or financial records are used.

## Key Performance Indicators

| KPI | Result |
|---|---:|
| Total Loans | 10,000 |
| Default Loans | 2,108 |
| Default Rate | 21.08% |
| Total Loan Amount | 256.50M |
| Default Exposure | 52.73M |
| Default Exposure Rate | 20.56% |

*Financial amounts are presented in BRL in the dashboard.*

## Key Business Insights

### 1. Credit Score Analysis

| Credit Score Category | Default Rate |
|---|---:|
| Low Score | 30.42% |
| Medium Score | 18.92% |
| High Score | 7.61% |

Low-score borrowers present approximately four times the default rate of high-score borrowers.

### 2. Income Analysis

| Income Category | Default Rate |
|---|---:|
| Low Income | 21.71% |
| High Income | 21.21% |
| Medium Income | 20.54% |

Default rates remain relatively similar across income categories, suggesting that income alone does not explain credit default behavior.

### 3. Loan Purpose Analysis

| Loan Purpose | Default Rate |
|---|---:|
| Home Improvement | 22.14% |
| Personal | 21.49% |
| Debt Consolidation | 21.30% |
| Education | 19.93% |

Home Improvement loans show the highest default rate, while Education loans show the lowest.

### 4. Financial Exposure Analysis

Low Score borrowers account for approximately BRL 39.13 million in default exposure, representing 29.90% of their total loan volume.

In comparison, High Score borrowers present a default exposure rate of 7.52%.

This highlights the importance of credit score segmentation when evaluating financial risk.

## Data Quality

The Silver layer applies data quality rules to ensure analytical consistency.

Validation results:

- 10,000 records processed.
- 0 missing critical records.
- 0 duplicate loan IDs.
- 14 columns in the transformed dataset.

## Dashboard

An interactive Databricks dashboard was developed to visualize:

- Default Rate by Credit Score Category.
- Default Rate by Income Category.
- Default Rate by Loan Purpose.
- Total Loan Amount vs. Default Exposure (BRL).

All dashboard metrics were validated against SQL queries to ensure consistency.

## Project Structure

```text
credit-risk-loan-default-analytics/
│
├── README.md
│
└── notebooks/
    └── credit_risk_analytics.ipynb
```

## How to Run

1. Open a Databricks workspace.
2. Import `credit_risk_analytics.ipynb`.
3. Run the notebook cells sequentially.
4. Review the Bronze, Silver, and Gold tables.
5. Execute the analytical SQL queries.
6. Explore the Databricks dashboard.

## Project Purpose

This project demonstrates practical skills in data generation, data engineering, data quality, SQL analytics, financial risk analysis, and business intelligence using the Databricks ecosystem.

**Note:** This is an educational analytics project using synthetic data. It does not represent a production credit risk model or real financial portfolio.
