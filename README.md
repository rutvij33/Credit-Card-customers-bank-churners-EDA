# Bank Credit Card Customer Churn: Exploratory Data Analysis

## Overview
An exploratory analysis of ~10,000 credit card customers to understand **who churns and why**,
and what a bank could do about it. The project goes beyond basic charts: it covers careful
data cleaning (including removing leakage columns), feature engineering, statistical testing,
customer segmentation, interaction analysis, and a business impact assessment.

## Dataset
- **Source:** [Credit Card Customers (BankChurners) on Kaggle](https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers)
- **Size:** 10,127 customers, 23 columns (about 16% churned)
- **File:** `data/BankChurners.csv`

## Key Questions
1. Which customer behaviours and demographics are linked to churn?
2. Is missing information ("Unknown" values) itself related to churn?
3. Which engineered features best separate churners from loyal customers?
4. Can customers be grouped into meaningful segments, and which segments churn most?
5. How much business value is at risk, and who should be targeted for retention?

## Methodology
- **Cleaning:** dropped two pre-computed Naive Bayes columns (data leakage), treated "Unknown" as missing, verified derived columns, reviewed outliers with the IQR method
- **Feature engineering:** average transaction value, active months, transactions per active month, spending-drop flag, age and tenure groups, income ordinal
- **Statistical testing:** chi-square with Cramér's V, Mann-Whitney U with effect sizes, confidence intervals for churn rate
- **Segmentation:** KMeans on scaled behavioural features, visualised with PCA
- **Interaction analysis:** churn-rate heatmaps across feature pairs
- **Business impact:** revenue at risk and a simple churn-risk rule

## Key Findings
> Replace these with your own findings and numbers from the notebook.
- [Finding 1]
- [Finding 2]
- [Finding 3]
- [Finding 4]
- [Finding 5]

![Churn by key feature](images/your_chart_1.png)
![Customer segments](images/your_chart_2.png)

## Business Recommendations
- [Recommendation 1]
- [Recommendation 2]
- [Recommendation 3]

## Limitations
- Imbalanced target (about 16% churn)
- Snapshot data with no full time dimension
- Some demographic fields contain "Unknown" values
- Pre-computed model columns were removed to avoid leakage

## Tools Used
Python, pandas, NumPy, Matplotlib, seaborn, SciPy, scikit-learn, statsmodels

## How to Run
```bash
git clone https://github.com/YOUR-USERNAME/bank-churn-eda.git
cd bank-churn-eda
pip install -r requirements.txt
jupyter notebook notebooks/bank_churn_eda.ipynb
```
**Note:** the notebook was written in Google Colab and reads the data from `/content/BankChurners.csv`.
When running locally, change that line to `pd.read_csv('../data/BankChurners.csv')`.
