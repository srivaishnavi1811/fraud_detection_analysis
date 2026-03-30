**Credit Card Fraud Detection Pipeline**


**Project Overview:**

This project addresses the challenge of detecting fraudulent credit card transactions using a highly imbalanced dataset (284,807 transactions with only 492 frauds). The goal was to move beyond simple accuracy and build a model that maximizes Recall to catch as much fraud as possible while maintaining a high Precision-Recall AUC.

**The Problem:**

In financial data, fraud is a "needle in a haystack." A standard model might achieve 99% accuracy just by predicting "Not Fraud" every time, but it would miss 100% of the actual theft. This project uses SMOTE and Random Forest to solve this imbalance.

**Key Features:**

Imbalance Handling: Utilized SMOTE (Synthetic Minority Over-sampling Technique) to balance the training set (from 398 fraud cases to 227,447).

Advanced Modeling: Implemented a Random Forest Classifier optimized for multi-core processing (n_jobs=-1).

Explainable AI: Extracted Feature Importances (Digital Fingerprints) to identify the top 10 indicators of fraudulent activity.

Deployment Ready: Includes a pre-trained model and scaler "packaged" via joblib for instant integration into web applications.


**Tech Stack:**

Language: Python

Libraries: Scikit-Learn, Imbalanced-Learn (SMOTE), Pandas, NumPy

Visualization: Matplotlib, Seaborn

Model Persistence: Joblib

**Project Structure:**

fraud_detection.ipynb: The complete end-to-end analysis and training notebook.

data/: Source dataset (CSV format).

fraud_model_final.pkl: The final trained Random Forest model.

scaler.pkl: The fitted StandardScaler for normalizing new transaction data.