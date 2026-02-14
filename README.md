# Telco Customer Churn Prediction

## Executive Summary

This project develops predictive models to identify high-risk customers for churn in a telecommunications business.

Best Model: Logistic Regression  
Test ROC-AUC: 0.83  
Cross-Validation ROC-AUC: 0.85  

The model demonstrates stable generalization performance and provides actionable insights for retention strategy optimization.



## Business Context

Customer churn directly impacts recurring revenue and customer lifetime value (CLV).  
Accurate churn prediction enables targeted intervention before revenue loss occurs.

From a business perspective:

- Missing a churn customer (False Negative) results in lost revenue.
- Incorrectly targeting a loyal customer (False Positive) incurs marketing cost.

Therefore, model evaluation must go beyond accuracy and focus on Recall and ROC-AUC.



## Dataset Overview

- 7,043 customers
- 21 features
- Binary classification (Churn: Yes/No)
- Imbalanced dataset (~26% churn rate)



## Modeling Approach

### Data Preparation
- Cleaned missing values in `TotalCharges`
- One-hot encoding for categorical variables
- 80/20 Train/Test split
- StandardScaler applied for Logistic Regression

### Models Implemented
- Logistic Regression (Pipeline)
- Random Forest Classifier

### Evaluation Metrics
- ROC-AUC
- Accuracy
- Confusion Matrix
- 5-Fold Cross-Validation



## Model Performance

| Model | Test AUC | CV AUC | Accuracy |
|-------|----------|--------|----------|
| Logistic Regression | 0.8319 | 0.8452 | 0.7875 |
| Random Forest | 0.8160 | 0.8232 | 0.7854 |

Logistic Regression demonstrated stronger and more stable cross-validation performance, indicating better generalization.



## Confusion Matrix Analysis (Logistic Regression)

<img src="images/confusion_matrix.png" width="450">

Baseline results:

- True Positives (Churn correctly predicted): 193
- False Negatives (Missed churn customers): 181
- False Positives (Incorrect churn alerts): 118

Interpretation:

The model captures a meaningful portion of churn customers, but reducing False Negatives remains critical because missed churn leads directly to revenue loss.

From a retention strategy perspective, threshold tuning or recall optimization may further improve business value.



## ROC Curve

<img src="images/roc_curve.png" width="500">

The ROC curve demonstrates strong separation capability between churn and non-churn customers.



## Key Drivers of Churn

Based on model behavior and feature patterns:

- Month-to-month contracts show the highest churn risk
- Higher monthly charges increase churn probability
- Early-tenure customers are more likely to churn



## Business Recommendations

- Prioritize retention campaigns for month-to-month customers
- Offer incentives for long-term contract conversion
- Implement proactive engagement programs within the first 6 months
- Consider recall-optimized deployment strategy to reduce revenue leakage



## Tech Stack

Python  
Pandas  
NumPy  
Scikit-learn  
Matplotlib  
Seaborn
