# Forage TATA Job simulation 
### Project title - Credit Delinquency Prediction Using Gen AI 
This repository contains an exploratory data analysis (EDA) project focused on understanding key behavioral and financial indicators influencing credit delinquency risk using GenAI to increase the accuracy and decrease the time to run that process. The dataset, sourced from Kaggle, includes customer demographic, financial, and transactional attributes that support risk modeling and business decision-making.

## Dataset Overview
**Key Features:**
- Age, Income, Credit_Score, Loan_Balance, Debt_to_Income_Ratio

- Missed_Payments, Credit_Utilization, Employment_Status, Credit_Card_Type

- Month_1 to Month_6 – behavioral tracking of monthly activity

- Delinquent_Account – Target variable (1 = delinquent, 0 = non-delinquent)
### Raw vs. Cleaned Dataset

| Feature                | Raw Dataset Issue                 | Cleaned Dataset Fix                              |
| ---------------------- | --------------------------------- | ------------------------------------------------ |
| `Income`               | 7.8% missing values               | Median imputation (due to skewed distribution)   |
| `Loan_Balance`         | 5.8% missing values               | Median imputation                                |
| `Credit_Score`         | 0.4% missing values               | Mean imputation (data is normally distributed)   |
| `Customer_ID`          | Present (non-informative)         | Dropped (unique identifier, no analytical value) |
| `Credit_Utilization`   | Some values >100%                 | Investigated and flagged as outliers             |
| `Month_1` to `Month_6` | Categorical, sequential data      | Retained for feature engineering                 |
| Numerical Features     | Skewed distributions and outliers | To be transformed (log/capping recommended)      |


## EDA Objectives
- Assess overall data quality and readiness for modeling

- Identify key drivers of delinquency risk

- Visualize feature distributions and uncover patterns

- Evaluate the impact of financial behavior (e.g., missed payments, utilization)

- Prepare the dataset for future machine learning workflows


## Key Insights
- Missed Payments, Credit Utilization, and Debt-to-Income Ratio are the strongest predictors of delinquency
- Customers with credit utilization >50% are more likely to default
- 3+ missed payments in the last 6 months signal elevated risk
- Some high-income customers have low credit scores → flagged for further review
- Temporal behavior in Month_1 to Month_6 can enhance modeling if aggregated into features

## AI & GenAI Use
AI tools were used to:

- Detect and summarize missing values

- Identify high-risk segments using correlation and pattern analysis

- Support early feature selection for model design

- Generate risk-driven insights to guide business strategy

## Tools Used
- Python / Pandas / NumPy – Data manipulation

- Matplotlib / Seaborn – Visualization

- Excel – Dataset review and cleaning

- AI Tools – Prompt-based pattern recognition and risk analysis (ChatGPT, Claude, Gemini)

