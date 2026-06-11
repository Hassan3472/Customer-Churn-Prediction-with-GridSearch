# Customer-Churn-Prediction-with-GridSearch

## Project Overview
This project implements a complete, production-ready machine learning pipeline to predict customer churn using the Telco Customer Churn dataset. It utilizes Scikit-learn Pipelines for clean and reproducible preprocessing and modeling.

## Objective
To build a binary classification model that identifies customers likely to churn, allowing for proactive retention strategies.

## Dataset Source
The dataset is sourced from the [Telco Customer Churn dataset](https://github.com/IBM/telco-customer-churn-on-icp4d).

## Data Validation Performed
- Checked data types and shapes.
- Verified missing values (and handled empty strings in `TotalCharges`).
- Inspected duplicate records.
- Summary statistics for numerical and categorical features.

## Models Used
- **Logistic Regression**: A linear model used as a baseline and strong performer.
- **Random Forest Classifier**: An ensemble tree-based model for capturing non-linear relationships.

## Hyperparameter Tuning
- Used `GridSearchCV` with 5-fold cross-validation.
- Optimized for `roc_auc` score.

## Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

## Best Model
- **Logistic Regression** was selected as the best model based on the highest ROC-AUC score (~0.84).

## Pipeline Export
- The final pipeline (including preprocessing and the best estimator) is saved as `customer_churn_pipeline.joblib`.

## Key Results
- Contract type (specifically Month-to-Month) is a significant predictor of churn.
- The pipeline effectively handles both numerical scaling and categorical encoding in a single object, ensuring no data leakage during inference.
