# Telco Customer Churn Prediction

## Executive Summary

This project develops predictive models to identify high-risk customers for a telecommunications company facing revenue loss due to churn.

The final selected model, Logistic Regression with class balancing, achieved:

- Test AUC: 0.83  
- Cross-Validation AUC: 0.85  
- Improved recall for churn customers after model adjustment  

The objective was not only to maximize AUC, but to reduce missed churn customers and align the model with business retention goals.

---

## Business Problem

Customer churn directly impacts recurring revenue and customer lifetime value in subscription-based businesses.

The goal of this project is to:

- Predict which customers are likely to churn
- Reduce false negatives (missed churn customers)
- Enable targeted retention campaigns
- Improve revenue protection strategy

---

## Dataset Overview

- 7,043 customers
- 21 features (demographic, service usage, billing information)
- Binary classification (Churn: Yes/No)
- Imbalanced dataset (~26% churn rate)

---

## Modeling Approach

### Data Preparation

- Cleaned missing values in TotalCharges
- Applied one-hot encoding to categorical variables
- Train/Test split (80/20)
- StandardScaler applied through Pipeline for Logistic Regression

### Models Implemented

- Logistic Regression (Pipeline with scaling)
- Random Forest Classifier

### Evaluation Metrics

- ROC-AUC
- Accuracy
- Precision and Recall
- 5-Fold Cross-Validation

---

## Model Performance

| Model | Test AUC | CV AUC | Accuracy |
|-------|----------|--------|----------|
| Logistic Regression | 0.8319 | 0.8452 | 0.7875 |
| Random Forest | 0.8160 | 0.8232 | 0.7854 |

Logistic Regression demonstrated stronger and more stable cross-validation performance.

---

## Model Improvement: Business-Oriented Optimization

Because missing a churn customer (False Negative) is more costly than a False Positive, the model was retrained using class weighting to reduce churn misclassification.

This adjustment significantly improved recall for churn customers, enabling better alignment with retention strategy objectives.

### Confusion Matrix (Baseline)

<img src="images/confusion_matrix.png" width="450">

### Confusion Matrix (Class Balanced)

<img src="images/confusion_matrix 2.png" width="450">

The balanced model reduces missed churn customers and increases actionable retention opportunities.

---

## Key Insights

- Month-to-month contracts exhibit the highest churn risk
- Higher monthly charges correlate with increased churn probability
- Customers in early tenure stages are more likely to churn

---

## Business Recommendations

- Deploy targeted retention campaigns for month-to-month customers
- Offer incentives to encourage long-term contract migration
- Implement early engagement programs within the first six months of subscription

---

## Tech Stack

Python  
Pandas  
NumPy  
Scikit-learn  
Matplotlib  
Seaborn
