# EdVyro Task 02 — Data Quality and Exploratory Analysis

## Dataset
Synthetic customer churn sample supplied by EdVyro. The dataset contains **15 records and 11 columns**.

## Quality audit
- Missing values: **0**
- Duplicate rows: **0**
- Duplicate customer IDs: **0**
- IQR outliers in numeric fields: **0**
- Negative age/tenure/monthly charges/support tickets: **0**
- Churn categories: **Yes / No**
- Total charges validation exceptions: **0**

## Cleaning decisions
1. Column names were standardized to snake_case for reproducible analysis.
2. No missing-value imputation was necessary.
3. No duplicate records were removed.
4. No numeric outliers were removed or capped because none fell outside the 1.5×IQR bounds.
5. Total charges were validated against `tenure_months × monthly_charge`; all records reconciled.

## Initial descriptive patterns
- Observed churn rate: **46.7%** (7 of 15 customers).
- Contract-level churn rates:
  - Month-to-Month: 100.0%
  - One Year: 0.0%
  - Two Year: 0.0%
- Subscription-level churn rates:
  - Basic: 71.4%
  - Enterprise: 0.0%
  - Pro: 50.0%

## Interpretation caution
These are descriptive patterns in a very small synthetic dataset. They should not be treated as causal relationships or generalised to real customers.

## Files
- `EdVyro_Task02_Customer_Churn_Analysis.xlsx`
- `customer_churn_cleaned.csv`
