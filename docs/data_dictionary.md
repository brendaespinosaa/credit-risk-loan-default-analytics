# Data Dictionary

## Project: Credit Risk & Loan Default Analytics

### Overview

This document describes the main fields used in the credit risk analysis dataset, including customer information, loan characteristics, credit scores, and loan default indicators.

### Dataset Fields

| Column | Description | Data Type |
|---|---|---|
| `loan_id` | Unique identifier for each loan record. | Integer |
| `customer_id` | Unique identifier for each customer. | Integer |
| `loan_amount` | Total amount borrowed by the customer. | Decimal |
| `credit_score` | Customer's credit score, representing their creditworthiness. | Integer |
| `credit_score_category` | Credit score classification (Low, Medium, or High). | String |
| `loan_term` | Loan repayment period. | Integer |
| `interest_rate` | Interest rate applied to the loan. | Decimal |
| `income` | Customer's annual income. | Decimal |
| `debt_to_income_ratio` | Ratio between the customer's debt and income. | Decimal |
| `employment_status` | Customer's employment status. | String |
| `default` | Indicates whether the loan resulted in default (1 = Yes, 0 = No). | Integer |

### Key Business Metrics

| Metric | Description | Calculation |
|---|---|---|
| Total Loans | Total number of loan records analyzed. | COUNT(*) |
| Default Loans | Number of loans classified as defaults. | SUM(default) |
| Default Rate | Percentage of loans that resulted in default. | (Default Loans / Total Loans) × 100 |
| Total Loan Amount | Total financial value of all loans. | SUM(loan_amount) |
| Default Exposure | Total loan amount associated with defaulted loans. | SUM(loan_amount WHERE default = 1) |

### Credit Risk Categories

| Category | Description |
|---|---|
| Low Score | Customers with lower credit scores and potentially higher credit risk. |
| Medium Score | Customers with intermediate credit scores and moderate credit risk. |
| High Score | Customers with higher credit scores and potentially lower credit risk. |

### Data Quality Considerations

The analysis considers the following data quality aspects:

- Missing or null values.
- Duplicate loan records.
- Invalid or inconsistent values.
- Consistency of default indicators.
- Accuracy of financial calculations.

### Notes

The data dictionary describes the expected analytical fields and business definitions used in the project. Actual column names and data types should match the source dataset and Databricks implementation.
