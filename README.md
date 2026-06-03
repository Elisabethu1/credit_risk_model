# credit_risk_model
Credit Risk Modeling Project
Probability of Default (PD) & Expected Loss (EL) Estimation
🚀 Overview

This project builds a credit risk scoring model to estimate:

📉 Probability of Default (PD) — likelihood a borrower will default
💰 Expected Loss (EL) — estimated financial loss given default

Using borrower financial data, we apply Logistic Regression with feature engineering to create an interpretable and industry-aligned credit risk model.

🎯 Objective

To develop a predictive framework that:

Identifies high-risk borrowers
Estimates default probability
Computes expected financial exposure
Provides interpretable risk drivers for decision-making
📂 Dataset Description

The dataset contains borrower-level financial attributes:

credit_lines_outstanding
total_debt_outstanding
loan_amt_outstanding
income
years_employed
fico_score
target: default (0/1)
🧠 Feature Engineering

To improve model performance and interpretability, we construct:

📌 Debt-to-Income Ratio
DTI=
Income
Total Debt
	​

📌 Payment-to-Income Ratio
PTI=
Income
Loan Amount
	​


These features better capture repayment pressure and leverage risk.

⚙️ Model Pipeline
Model: Logistic Regression
Scaling: StandardScaler
Missing values: Median Imputation
Evaluation: ROC-AUC

Why Logistic Regression?

✔ Highly interpretable
✔ Industry standard for credit scoring
✔ Strong baseline for separable datasets

📈 Model Performance
ROC-AUC Score: 1.0
📌 Interpretation

The model achieves near-perfect separability between default and non-default classes, indicating strong predictive structure in financial variables.

📊 Probability of Default (PD)

Example borrower output:

PD = 0.0248 (2.48%)

📌 Interpretation:
The borrower is classified as low risk, with a low likelihood of default.

💰 Expected Loss (EL)
EL=PD×(1−Recovery Rate)×Exposure
Recovery Rate: 10%
Exposure: Loan Amount
Example Result:
Expected Loss = 445.92

📌 Interpretation:
This represents the expected monetary loss adjusted for recovery assumptions.

📊 Model Evaluation Visualizations
📉 ROC Curve
<p align="center"> <img src="C:/Users/elisabethung/Pictures/Screenshots/ROC Curve.png" width="500"/> </p>
Measures classification performance across thresholds
Model shows near-perfect separation
📊 Confusion Matrix
<p align="center"> <img src="C:/Users/elisabethung/Pictures/Screenshots/confusion_matrix.png" width="450"/> </p>
Very few misclassifications
High predictive accuracy
🔥 Feature Importance
<p align="center"> <img src="C:/Users/elisabethung/Pictures/Screenshots/feature_importance.png" width="500"/> </p>

Key drivers of default risk:

Credit lines outstanding (+ risk)
Debt-to-income ratio (+ risk)
FICO score (– risk)
Years employed (– risk)
📦 Default Distribution
<p align="center"> <img src="C:/Users/elisabethung/Pictures/Screenshots/default_graph.png" width="450"/> </p>
Balanced dataset improves model stability
Clear separation between classes
🔍 Key Insights
Credit exposure and debt ratios are strongest predictors of default
Credit score (FICO) strongly reduces risk probability
Logistic regression provides both accuracy and interpretability
Feature engineering significantly improves model clarity
🏁 Conclusion

This project demonstrates a complete credit risk modeling pipeline, including:

✔ Data preprocessing
✔ Feature engineering
✔ Logistic regression modeling
✔ Risk estimation (PD & EL)
✔ Model evaluation and visualization

The model is suitable for credit underwriting and risk assessment use cases.
