# Data Dictionary

## Project: Credit Risk & Loan Default Analytics

### Overview

This document describes the fields available in the Silver layer of the credit risk dataset.

The dataset contains customer demographic information, financial indicators, loan characteristics, and default-related variables used to analyze credit risk and loan portfolio performance.

**Source Table:** `default.credit_risk_silver`

### Dataset Schema

| Column | Data Type | Description |
|---|---|---|
| `loan_id` | STRING | Unique identifier for each loan record. |
| `age` | INT | Customer's age in years. |
| `annual_income` | INT | Customer's annual income. |
| `credit_score` | INT | Customer's credit score, representing creditworthiness. |
| `loan_amount` | DOUBLE | Total amount borrowed by the customer. |
| `loan_purpose` | STRING | Purpose or reason for the loan. |
| `employment_type` | STRING | Customer's employment category or employment status. |
| `debt_to_income` | DOUBLE | Debt-to-income ratio, indicating the relationship between debt and annual income. |
| `interest_rate` | DOUBLE | Interest rate applied to the loan. |
| `default_flag` | INT | Default indicator (1 = Default, 0 = No Default). |
| `loan_status` | STRING | Current or recorded status of the loan. |
| `credit_score_category` | STRING | Credit score classification (Low, Medium, or High). |
| `income_category` | STRING | Customer income classification. |
| `loan_amount_category` | STRING | Loan amount classification based on predefined ranges. |

### Key Business Metrics

| Metric | Description | Calculation |
|---|---|---|
| Total Loans | Total number of loans analyzed. | COUNT(*) |
| Default Loans | Number of loans classified as defaults. | SUM(default_flag) |
| Default Rate | Percentage of loans that resulted in default. | (Default Loans / Total Loans) × 100 |
| Total Loan Amount | Total financial value of the loan portfolio. | SUM(loan_amount) |
| Default Exposure | Total loan amount associated with defaulted loans. | SUM(loan_amount WHERE default_flag = 1) |

### Credit Risk Segmentation

The dataset includes three classification fields used for segmentation:

- **Credit Score Category:** Groups customers according to their credit scores.
- **Income Category:** Groups customers according to their annual income.
- **Loan Amount Category:** Groups loans according to their respective amounts.

These categories support comparative analysis and help identify patterns across different risk profiles.

### Data Quality Considerations

The Silver layer is used as the curated dataset for analytical queries and dashboard development.

Relevant data quality checks include:

- Missing or null values.
- Duplicate loan identifiers.
- Invalid financial values.
- Consistency of default indicators.
- Validity of categorical classifications.
- Consistency between loan status and default indicators.

### Notes

All field names and data types listed in this document reflect the schema of the Silver table in Databricks.

The business definitions describe the analytical purpose of each field and may be refined according to the original dataset documentation.
