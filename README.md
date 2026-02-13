Customer Churn Prediction & Retention Strategy Modeling
Business Problem

Telecom providers face significant revenue risk due to customer churn. This project builds predictive models to identify high-risk customers and inform targeted retention strategies.

Dataset

7,043 customers

21 features

Binary classification (Churn: Yes/No)

Imbalanced dataset (~26% churn rate)

Modeling Approach

Data cleaning and preprocessing

One-hot encoding for categorical features

Train/test split (80/20)

Logistic Regression (with StandardScaler Pipeline)

Random Forest Classifier

ROC-AUC evaluation

5-fold cross-validation

Results
Model	Test AUC	CV AUC	Accuracy
Logistic Regression	0.8319	0.8452	0.7875
Random Forest	0.8160	0.8232	0.7854

Logistic Regression demonstrated stronger and more stable performance across validation folds.

Key Insights

Month-to-month contracts show highest churn risk

Higher monthly charges increase churn probability

Early tenure customers are more likely to churn

Business Recommendations

Targeted retention campaigns for month-to-month customers

Incentives for long-term contract conversion

Early engagement programs within first 6 months
