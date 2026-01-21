Telco Customer Churn Prediction and Model Optimization
This project aims to predict customer churn for a telecommunications company using supervised learning techniques in Python with scikit-learn. By analyzing customer demographics, account information, and service usage, we built a model to identify customers at risk of leaving.
+3

📋 Table of Contents
Overview

Data Preprocessing

Machine Learning Pipeline

Hyperparameter Tuning

Evaluation Metrics

🔍 Overview
Machine learning is the process where computers learn to make decisions from data without being explicitly programmed. In this classification challenge, the target variable consists of categories: "Churn" or "No Churn".


🛠 Data Preprocessing
Scikit-learn requires data to be in a specific format before modeling:

Handling Missing Values: Missing data in the TotalCharges column was handled using SimpleImputer with a "mean" strategy.

Categorical Encoding: Categorical features (like Contract and InternetService) were converted into numeric values using dummy variables to be compatible with scikit-learn.

Scaling: We used StandardScaler to center and scale features, ensuring that variables with larger scales (e.g., TotalCharges) do not disproportionately influence the model.


🚀 Machine Learning Pipeline
To prevent data leakage and streamline the workflow, we utilized scikit-learn's Pipeline. The pipeline integrates:

Imputation: Filling missing values.

Scaling: Standardizing features.

Classification: Logistic Regression model for binary classification.


⚙️ Hyperparameter Tuning
We used GridSearchCV to optimize the model's performance by trying different hyperparameter values and using cross-validation to avoid overfitting.

CV Strategy: 5-fold K-Fold cross-validation.

Metric: We optimized for ROC AUC to ensure the model effectively distinguishes between classes.


📊 Evaluation Metrics
Since accuracy is not always a useful metric for imbalanced data, we evaluated the model using:

Confusion Matrix: To see True Positives and False Negatives.

Precision and Recall: Crucial for understanding how many actual churners were identified.

ROC Curve: Visualizing the trade-off between the True Positive Rate and False Positive Rate.