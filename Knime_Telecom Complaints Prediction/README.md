# Telecom Complaint Prediction (Logistic Regression)

## 📌 Project Overview
This project aims to build a binary classification model in **KNIME** to predict whether a telecom customer will raise a complaint. By identifying unhappy customers early, telecom providers can improve proactive support and reduce call center congestion.

## 🛠️ Tech Stack & Tools
* **Tool:** KNIME Analytics Platform
* **Model:** Logistic Regression (with L2 Regularization)
* **Data Handling:** SMOTE (Synthetic Minority Over-sampling Technique)
* **Preprocessing:** One-Hot Encoding, Z-Score Normalization

## 📊 Dataset Information
* **Source:** `telecom_data_clean.csv`
* **Target Variable:** `complaint_flag_num` (1 = Complaint, 0 = No Complaint)
* **Key Features:** Usage patterns, network/outage behavior, recharge/payment history, and plan details.

## 🚀 Workflow Highlights
1.  **Leakage-Safe Filtering:** Removed identifiers and complaint-specific resolution fields to ensure real-world model validity.
2.  **Imbalance Correction:** Applied SMOTE only on the training branch (preserving the real-world distribution of the test set).
3.  **Standardization:** Used Z-score scaling to help the Logistic Regression model train effectively.
4.  **Convergence Fix:** Implemented L2 (Uniform Gauss/Ridge) regularization to handle multicollinearity from one-hot encoded variables.

## 📈 Model Performance
| Metric | Score |
| :--- | :--- |
| **Accuracy** | 0.867 |
| **Precision (Class 1)** | 0.957 |
| **Recall (Class 1)** | 0.880 |
| **F1 Score (Class 1)** | 0.917 |
| **Cohen’s Kappa** | 0.586 |

## 📁 Repository Structure
* `data/`: Contains the cleaned telecom dataset.
* `knime_workflow/`: Exported KNIME workflow file (.knwf).
* `outputs/`: Final predictions, confusion matrix, and model metrics in CSV format.

## 🏁 Conclusion
The pipeline successfully built a leakage-safe and balanced model capable of predicting customer complaints with high precision. Future improvements could include testing Random Forest or XGBoost for comparative analysis.

