# Telco Customer Churn Prediction

## Business Problem

Telecommunication companies face significant revenue risk due to customer churn.  
This project builds predictive models to identify high-risk customers and support targeted retention strategies.

---

## Dataset Overview

- **7,043 customers**
- **21 features**
- Binary classification (Churn: Yes/No)
- Imbalanced dataset (~26% churn rate)

---

## Modeling Approach

### Data Preparation
- Missing value handling (TotalCharges cleaned)
- One-hot encoding for categorical variables
- Train/Test split (80/20)

### Models Implemented
- Logistic Regression (StandardScaler + Pipeline)
- Random Forest Classifier

### Evaluation Metrics
- ROC-AUC
- Accuracy
- 5-Fold Cross-Validation

---

## Model Performance

| Model | Test AUC | CV AUC | Accuracy |
|-------|----------|--------|----------|
| Logistic Regression | 0.8319 | 0.8452 | 0.7875 |
| Random Forest | 0.8160 | 0.8232 | 0.7854 |

**Logistic Regression demonstrated stronger and more stable cross-validation performance.**

---

## Key Insights

- Month-to-month contracts show highest churn risk  
- Higher monthly charges increase churn probability  
- Early-tenure customers are more likely to churn  

---

## Business Recommendations

- Targeted retention campaigns for month-to-month customers  
- Incentives for long-term contract conversion  
- Early engagement programs within first 6 months  

---

## Tech Stack

Python • Pandas • NumPy • Scikit-learn • Matplotlib • Seaborn
