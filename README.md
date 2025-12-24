# Telco Customer Churn – Data Cleaning & EDA

## Problem Statement
Customer churn is a major business challenge for telecom companies.  
Before building any predictive model, it is critical to ensure data quality and understand underlying patterns.

This project focuses on cleaning and exploring a real-world telecom dataset to make it suitable for downstream machine learning tasks.

---

## Structure
```
├── telco-customer-churn/
│   ├── data/
│   │   └── Telco-Customer-Churn.csv
│   ├── notebooks/
│   │   └── 01_data_cleaning_and_eda.ipynb
│   ├── README.md

```
---

## Dataset
- Source: Kaggle – Telco Customer Churn
- Rows: 7,043
- Columns: 21
- Target Variable: `Churn`

---

## Data Quality Issues Identified
- `TotalCharges` was stored as an object instead of a numeric type
- Hidden missing values caused by empty strings
- Skewed distributions and extreme values in billing-related features

---

## Cleaning & Preprocessing Decisions
- Converted `TotalCharges` to numeric using coercion to expose invalid entries
- Filled missing `TotalCharges` with `0` based on business logic (new customers with zero tenure)
- Detected outliers using the Interquartile Range (IQR) method
- Retained outliers as high charges represent valid premium customers, not data errors

---

## Key Insights
- Customers with shorter tenure and higher monthly charges show higher churn tendency
- Billing-related features appear to be strong indicators of customer churn
- Naive handling of missing values can introduce false revenue and bias analysis

---

## Tools & Technologies
- Python
- Pandas
- NumPy
- Jupyter Notebook

---

## Next Steps
- Feature engineering
- Build and evaluate churn prediction models
- Model interpretation and business recommendations
