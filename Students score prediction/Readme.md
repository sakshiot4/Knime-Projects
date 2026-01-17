
# 📊 Student Performance Prediction using KNIME

This project demonstrates an **end-to-end regression workflow in KNIME Analytics Platform** to predict student exam scores based on the number of hours studied. The goal is to understand the relationship between study time and performance using **Linear Regression**, along with proper evaluation and error analysis.

---

## 🔍 Problem Statement

Can a student’s exam score be predicted based on the number of hours they study?

This project uses a simple but effective regression approach to model this relationship and evaluate how well study hours explain score variability.

---

## 🗂️ Dataset Overview

The dataset contains student-level information with the following columns:

* `name` – Student name
* `hours` – Hours studied
* `score` – Exam score (target variable)
* `gender`, `grades`, `class` – Categorical attributes

For modeling, only **hours** (feature) and **score** (target) are used.

---

## 🛠️ Tools & Technologies

* **KNIME Analytics Platform**
* Linear Regression
* Data Visualization (JavaScript views)
* Regression Evaluation Metrics

---

## 🔄 Workflow Steps

1. **Data Loading**

   * Loaded dataset using CSV Reader

2. **Data Understanding & EDA**

   * Summary statistics
   * Categorical distribution checks
   * Histograms, box plots, and scatter plots

3. **Feature Selection**

   * Selected `hours` as predictor
   * Selected `score` as target variable

4. **Train–Test Split**

   * 80% training, 20% testing
   * Fixed random seed for reproducibility

5. **Model Training**

   * Trained a Linear Regression model

6. **Prediction**

   * Generated predictions on test data

7. **Model Evaluation**

   * RMSE
   * R² Score

8. **Error Analysis**

   * Residuals (`Actual − Predicted`)
   * Absolute Error calculation

---

## 📐 Model Interpretation

The trained model learns the following relationship:

```
Score = 6.8 × Hours + 24.6
```

### Interpretation:

* For every additional hour studied, the predicted score increases by **~6.8 marks**
* Even with zero study hours, the model predicts a baseline score of **~25 marks**

---

## 📈 Evaluation Metrics

* **RMSE**: Measures average prediction error in marks
* **R² Score**: Indicates how much variance in scores is explained by study hours

These metrics are appropriate for **regression problems**, where accuracy and confusion matrices do not apply.

---

## 🧠 Key Insights

* Study hours have a strong positive correlation with exam scores
* Linear regression performs well for this simple, interpretable problem
* Residual analysis confirms reasonable model behavior

---

## 📌 Conclusion

This project demonstrates a complete regression pipeline in KNIME, covering data preparation, visualization, modeling, evaluation, and interpretation. It serves as a strong example of applying machine learning fundamentals using a low-code analytics platform.

---

## 📷 Workflow Preview

<img width="1362" height="547" alt="image" src="https://github.com/user-attachments/assets/85806f6c-822b-4b34-8639-ad1d2a322147" />

---




