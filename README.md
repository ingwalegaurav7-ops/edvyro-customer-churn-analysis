# edvyro-customer-churn-analysis
EdVyro Data Analytics Task 1 — Customer Churn Data Quality and Exploratory Analysis
# EdVyro Data Analytics — Task 1

## Customer Churn Data Quality & Exploratory Analysis

### Project Overview

This project analyzes a synthetic customer churn dataset as part of the EdVyro Data Analytics internship.

The objective is to audit and clean the dataset, perform exploratory analysis, identify initial churn patterns, and recommend which customer group a fictional subscription team should contact first to reduce avoidable churn.

### Decision Question

**Which customer groups should a fictional subscription team contact first to reduce avoidable churn?**

---

## Dataset

The dataset contains synthetic customer records with information about:

* Customer ID
* Tenure in months
* Monthly charge
* Support tickets in the previous 90 days
* Contract type
* Churn status

The dataset contains **15 customer records and 11 fields**.

---

## Data Quality Audit

The dataset was checked for:

* Missing values
* Duplicate rows
* Duplicate customer IDs
* Impossible or negative values
* Extreme/outlier values
* Invalid churn values
* Internal consistency of calculated fields

### Audit Results

| Check                           | Result |
| ------------------------------- | -----: |
| Records                         |     15 |
| Fields                          |     11 |
| Missing values                  |      0 |
| Duplicate rows                  |      0 |
| Duplicate customer IDs          |      0 |
| Negative/impossible values      |      0 |
| IQR outliers                    |      0 |
| Invalid churn values            |      0 |
| Total charge consistency issues |      0 |

The dataset did not require deletion or imputation of any customer records.

---

## Cleaning Decisions

No customer rows were removed because there were no duplicate, missing, or invalid records.

The main transformation was standardizing column names into **snake_case** for consistency and easier analysis.

The cleaning process was documented in the workbook's **Cleaning Log** and verified using validation checks.

---

## Exploratory Analysis

The overall observed churn rate was:

**46.7% (7 of 15 customers)**

### Churn by Contract Type

| Contract Type  | Observed Churn |
| -------------- | -------------: |
| Month-to-Month |         100.0% |
| One Year       |           0.0% |
| Two Year       |           0.0% |

In this sample, all Month-to-Month customers churned, while no One Year or Two Year customers churned.

### Churn by Subscription Type

| Subscription Type | Observed Churn |
| ----------------- | -------------: |
| Basic             |          71.4% |
| Pro               |          50.0% |
| Enterprise        |           0.0% |

### Support Tickets

Customers with higher recent support-ticket counts showed a stronger association with churn in this sample.

Customers with **3–6 support tickets had 100% observed churn**, while customers with **0–2 tickets had 0% observed churn**.

This is an observed pattern only and should not be interpreted as proof that support tickets cause churn.

---

## Key Recommendation

### Audience

Prioritize **Month-to-Month customers**, particularly those showing higher recent support-ticket activity.

### Decision

The fictional subscription team should consider contacting this group first with proactive retention or support follow-up.

### Supporting Metric

Month-to-Month customers had an observed **100% churn rate** in this sample.

Customers with 3–6 support tickets also had **100% observed churn**.

### Uncertainty

The dataset contains only **15 synthetic customer records**. Therefore, these findings are descriptive and should not be treated as predictive, causal, or representative of a larger customer population.

The observed patterns may change significantly when more customer records are analyzed.

### Next Measurement

Collect a larger dataset and track:

* Churn rate by contract type
* Churn rate by support-ticket volume
* Retention after proactive outreach
* Churn before vs. after intervention
* Results from a comparable non-contacted customer group

This would help determine whether the recommended outreach is actually associated with improved retention.

---

## Important Analytical Note

This analysis focuses on **descriptive findings** rather than predictions.

Correlation or association between variables and churn does not establish causation. In particular, the support-ticket pattern should not be interpreted as evidence that support tickets directly cause customers to leave.

---

## Files

### `EdVyro_Task1_Final_Submission.xlsx`

Contains:

* Raw data
* Data quality audit
* Cleaning log
* Cleaned data
* Validation checks
* Summary statistics
* Exploratory analysis
* Churn comparisons
* Key findings
* Data dictionary

### `customer_churn_cleaned.csv`

Cleaned dataset with standardized column names.

### `EdVyro_Task01_Customer_Churn_Analysis`

Short written summary of the data-quality checks, cleaning decisions, findings, and recommendation.

---

## Tools Used

* Microsoft Excel
* Python / Pandas
* Exploratory Data Analysis
* Data Cleaning
* Data Quality Validation
* Descriptive Statistics

---

## Project Limitation

This is a small synthetic dataset intended for beginner-level data-quality and exploratory-analysis practice.

The findings should therefore be treated as initial observations rather than business predictions or causal conclusions.
