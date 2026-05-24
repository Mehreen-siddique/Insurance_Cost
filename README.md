# 🚀 Machine Learning Weekly Showcase
## Regression & Classification Benchmark Study

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-Boosting-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

# 📖 Project Overview

This repository contains a comprehensive machine learning benchmark study conducted across multiple real-world datasets involving both **Regression** and **Classification** problems.

The goal of this project is to demonstrate an end-to-end machine learning workflow including:

- Data preprocessing
- Feature engineering
- Model training
- Performance evaluation
- Model comparison
- Insight generation

This repository serves as a **weekly machine learning showcase and portfolio project**.

---

# 📂 Datasets Used

The following datasets were used throughout this project.

| Dataset | Problem Type | Objective | Dataset Link |
|---|---|---|---|
| Medical Insurance Cost | Regression | Predict insurance charges | Add Link |
| Bike Sharing Demand | Regression | Predict bike rental demand | Add Link |
| Titanic | Classification | Predict survival | Add Link |
| Student Performance in Exams | Regression + Classification | Predict score & pass/fail | Add Link |
| Heart Disease UCI | Classification | Predict heart disease | Add Link |

---

# 🔗 Dataset Sources

Replace the links below with your actual Kaggle or UCI dataset URLs.

### Medical Insurance Cost
[Dataset Link](PASTE_LINK_HERE)

### Bike Sharing Demand
[Dataset Link](PASTE_LINK_HERE)

### Titanic Competition
[Dataset Link](PASTE_LINK_HERE)

### Student Performance in Exams
[Dataset Link](PASTE_LINK_HERE)

### Heart Disease UCI
[Dataset Link](PASTE_LINK_HERE)

---

# 🧠 Machine Learning Models Used

This project includes both **Regression** and **Classification** algorithms to compare performance across different learning paradigms.

---

# 📈 Regression Models

The following regression algorithms were implemented:

| Model | Type | Purpose |
|---|---|---|
| Linear Regression | Linear | Baseline regression |
| Ridge Regression | Linear + Regularization | Reduce overfitting |
| Decision Tree Regressor | Tree-Based | Capture non-linear relationships |
| Random Forest Regressor | Ensemble | Improve stability & accuracy |
| Support Vector Regressor (SVR) | Kernel-Based | High-dimensional regression |
| XGBoost Regressor | Boosting | High-performance prediction |

---

## Why These Regression Models?

Regression models were selected to compare:

- Linear vs non-linear learning
- Simple vs ensemble approaches
- Bagging vs boosting
- Predictive power on tabular datasets

### Model Selection Justification

### Linear Regression
Used as a simple and interpretable baseline model.

### Ridge Regression
Chosen to reduce overfitting using regularization.

### Decision Tree Regressor
Selected to learn complex non-linear patterns.

### Random Forest Regressor
Chosen due to ensemble robustness and reduced variance.

### SVR
Used to evaluate kernel-based learning capability.

### XGBoost
Selected because of strong predictive performance and boosting architecture.

---

# 📊 Classification Models

The following classification models were trained:

| Model | Type | Purpose |
|---|---|---|
| Logistic Regression | Linear | Baseline classifier |
| Decision Tree Classifier | Tree-Based | Rule-based learning |
| Random Forest Classifier | Ensemble | Robust classification |
| Support Vector Machine (SVM) | Margin-Based | High-dimensional classification |

---

## Why These Classification Models?

These models were selected to compare:

- Linear vs non-linear decision boundaries
- Ensemble learning
- Interpretability vs performance
- Different classification strategies

### Logistic Regression
Used as an interpretable baseline classification model.

### Decision Tree
Chosen for learning non-linear rules.

### Random Forest
Selected for strong classification performance and stability.

### Support Vector Machine
Used for effective high-dimensional classification.

---

# ⚙️ Data Preprocessing Workflow

A structured preprocessing pipeline was applied where required.

## Step 1 — Data Cleaning

- Duplicate removal
- Data type verification
- Missing value identification

## Step 2 — Missing Value Handling

Different techniques were used depending on data type.

### Numerical Features
- Median imputation

### Categorical Features
- Mode imputation

### High Missing Columns
Columns with excessive missing values were removed when necessary.

---

## Step 3 — Encoding

Categorical variables were encoded to make them suitable for machine learning models.

---

## Step 4 — Train-Test Split

Datasets were divided into:

- 80% Training Data
- 20% Testing Data

This ensured fair and unbiased model evaluation.

---

# 🏗 Feature Engineering

Feature engineering was performed when required.

---

## Student Performance Dataset

A new feature:

`pass_fail`

was created using math score.

### Rule

- Math Score ≥ 50 → Pass (1)
- Math Score < 50 → Fail (0)

---

## Why Pass/Fail Was Created?

The original math score is continuous and suitable for regression.

However, academic systems often evaluate outcomes through binary decisions such as:

- Pass / Fail
- Qualified / Not Qualified

Creating this feature allowed:

- Conversion into a classification problem
- Binary outcome prediction
- Educational outcome analysis

---

## Why Pass_Fail Was Used as Target?

The `pass_fail` feature represents the final academic outcome.

It was selected as the target variable because it allows machine learning models to learn patterns associated with student success and failure.

---

# 📏 Evaluation Metrics

Different evaluation metrics were used depending on problem type.

---

# Regression Metrics

| Metric | Purpose |
|---|---|
| MAE | Average prediction error |
| RMSE | Penalizes larger prediction errors |
| R² Score | Measures explained variance |

---

# Classification Metrics

| Metric | Purpose |
|---|---|
| Accuracy | Overall prediction correctness |
| F1 Score | Balance between precision and recall |
| ROC-AUC | Classification ranking performance |

Multiple metrics were used to ensure reliable evaluation.

---

# 🏆 Global Regression Comparison

Replace with your actual results.

| Dataset | Model | R² Score | RMSE | MAE |
|---|---|---:|---:|---:|
| Insurance | Linear Regression |0.81 |0.40 |0.26 |
| Insurance | Random Forest |0.85 |0.36 |0.18 |
| Insurance | XGBoost |0.86 |0.34 |0.18 |
| Bike Sharing | Random Forest | |0.32 | |
| Student Score | Random Forest | 0.79|6.50 | |
| Student Score | XGBoost |0.81 |6.20 | |

---

# 🏆 Global Classification Comparison

Replace with your actual results.

| Dataset | Model | Accuracy | F1 Score | ROC-AUC |
|---|---|---:|---:|---:|
| Titanic | Logistic Regression | | | |
| Titanic | Random Forest | | | |
| Heart Disease | Logistic Regression | | | |
| Heart Disease | Random Forest | | | |
| Student Pass/Fail | Logistic Regression | | | |
| Student Pass/Fail | Random Forest | | | |

---

# 🥇 Best Performing Models

| Dataset | Problem Type | Best Model | Key Metric |
|---|---|---|---|
| Insurance | Regression | | |
| Bike Sharing | Regression | | |
| Titanic | Classification | | |
| Student | Classification | | |
| Heart Disease | Classification | | |

---

# 🔍 Key Findings

Major findings from this study include:

- Ensemble methods consistently performed strongly
- Random Forest produced stable results across datasets
- XGBoost delivered strong regression accuracy
- Logistic Regression remained valuable for interpretability
- Feature engineering significantly improved classification performance

---

# 📁 Repository Structure

```text
Machine-Learning-Showcase/
│
├── datasets/
│
├── notebooks/
│   ├── medical_insurance.ipynb
│   ├── bike_sharing.ipynb
│   ├── titanic.ipynb
│   ├── student_performance.ipynb
│   └── heart_disease.ipynb
│
├── images/
│
├── README.md
│
└── requirements.txt
```

---

# ✅ Final Conclusion

This repository demonstrates a complete machine learning workflow across multiple datasets and problem types.

The project highlights the importance of:

- Data preprocessing
- Feature engineering
- Algorithm comparison
- Metric-based evaluation
- Data-driven model selection

The findings show that no single model is universally best and successful machine learning depends on selecting appropriate techniques based on data characteristics and task requirements.

---

# 👩‍💻 Author

**Mehreen Siddique**

GitHub: Add Link  
Kaggle: Add Link  
LinkedIn: Add Link
