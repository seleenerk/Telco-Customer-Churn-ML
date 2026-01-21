# 📶 Telco Customer Churn Prediction & Model Optimization

This project presents an end-to-end machine learning workflow to predict customer churn for a telecommunications company using **scikit-learn**.

## 📋 Table of Contents
* [Overview](#overview)
* [Data Preprocessing](#data-preprocessing)
* [Machine Learning Pipeline](#machine-learning-pipeline)
* [Hyperparameter Tuning](#hyperparameter-tuning)
* [Evaluation Metrics](#evaluation-metrics)

## 🔍 Overview
In this **classification** challenge, we aim to identify at-risk customers. We analyze demographics, account information, and service usage to predict whether a customer will leave (Churn).

## 🛠 Data Preprocessing
Scikit-learn requires data to be in a specific format:
- **Handling Missing Values:** Used `SimpleImputer` with a "mean" strategy for `TotalCharges`.
- **Categorical Encoding:** Converted text features into numeric values using dummy variables (`pd.get_dummies`).
- **Scaling:** Applied `StandardScaler` to ensure all features are on the same scale.



## 🚀 Machine Learning Pipeline
To prevent **data leakage**, we utilized scikit-learn's `Pipeline`. This ensures that scaling and modeling steps are integrated seamlessly.

## ⚙️ Hyperparameter Tuning
We used `GridSearchCV` to optimize the model:
- **CV Strategy:** 5-fold K-Fold cross-validation.
- **Metric:** Optimized for **ROC AUC** to ensure the model effectively distinguishes between classes.



## 📊 Evaluation Metrics
Since the data is imbalanced, we focused on:
- **Confusion Matrix:** To track True Positives vs. False Negatives.
- **ROC Curve:** Visualizing the trade-off between True Positive Rate and False Positive Rate.



---
