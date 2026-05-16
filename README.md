# Medical Insurance Cost Prediction Using Machine Learning

This project focuses on predicting medical insurance charges using multiple machine learning regression algorithms on the Medical Insurance Cost Dataset. The project includes complete data preprocessing, feature engineering, exploratory data analysis (EDA), model training, evaluation, and visualization.

The objective is to analyze the factors affecting medical insurance costs and build predictive models capable of estimating insurance charges accurately.

---

# Project Workflow

```text id="4jlwmk"
Data Collection
      ↓
Data Cleaning
      ↓
EDA & Visualization
      ↓
Feature Engineering
      ↓
Data Preprocessing
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Feature Importance Analysis
      ↓
Learning Curve Analysis
```

---

# Dataset Features

| Feature    | Description            |
| ---------- | ---------------------- |
| `age`      | Age of the individual  |
| `sex`      | Gender                 |
| `bmi`      | Body Mass Index        |
| `children` | Number of dependents   |
| `smoker`   | Smoking status         |
| `region`   | Residential region     |
| `charges`  | Medical insurance cost |

---

# Data Preprocessing

The following preprocessing steps were performed:

* Checked missing values
* Encoded categorical variables using `pd.get_dummies()`
* Applied feature scaling where required
* Applied logarithmic transformation to target variable
* Split dataset into training and testing sets

---

# Feature Engineering

Additional features were created to improve model learning and prediction performance.

## Age Squared Feature

```python id="jlwm4u"
df['age_squared'] = df['age'] ** 2
```

This captures non-linear relationships between age and insurance costs.

---

## BMI-Smoker Interaction Feature

```python id="2jlwm3"
df['bmi_smoker'] = df['bmi'] * df['smoker_yes']
```

This feature captures the combined effect of smoking and BMI on insurance charges.

---

## Log Transformation of Target Variable

```python id="9jlwmm"
df['log_charges'] = np.log(df['charges'])
```

This reduced skewness in the target variable and improved regression performance.

---

# Exploratory Data Analysis (EDA)

EDA was performed to analyze:

* Distribution of insurance charges
* Correlation between features
* Impact of smoking on medical costs
* Relationship between BMI and charges
* Age vs insurance expenses

Visualization techniques included:

* Scatter plots
* Heatmaps
* Boxplots
* Distribution plots

---

# Machine Learning Models Used

The following regression models were trained and evaluated:

* Linear Regression
* Ridge Regression
* Decision Tree Regressor
* Random Forest Regressor
* Support Vector Regressor (SVR)
* XGBoost Regressor

---

# Model Performance

| Model             | Train R² | Test R² | Train RMSE | Test RMSE |
| ----------------- | -------- | ------- | ---------- | --------- |
| Linear Regression | 0.774    | 0.816   | 0.432      | 0.406     |
| Ridge Regression  | 0.774    | 0.816   | 0.432      | 0.406     |
| Decision Tree     | 0.844    | 0.832   | 0.359      | 0.388     |
| Random Forest     | 0.967    | 0.847   | 0.163      | 0.370     |
| XGBoost           | 0.873    | 0.866   | 0.324      | 0.346     |
| SVR               | 0.852    | 0.854   | 0.349      | 0.361     |

---

# Best Performing Model

## XGBoost Regressor

XGBoost achieved the best overall performance with:

* Highest testing R² score
* Lowest RMSE
* Strong generalization capability
* Minimal overfitting

### Final Results

```text id="5jlwmf"
Train R² : 87%
Test R²  : 86%
Test RMSE: 0.346
```

---

# Visualizations Included

The project includes several important visualizations:

## EDA Visualizations

* Correlation heatmap
* BMI vs Charges scatter plot
* Smoker vs Charges boxplot
* Distribution plots

## Model Evaluation Visualizations

* Actual vs Predicted scatter plots
* Learning curve analysis
* Random Forest feature importance plot

---

# Learning Curve Analysis

Learning curves were generated for the XGBoost model to analyze:

* model convergence
* generalization capability
* overfitting behavior

The learning curve demonstrated stable convergence between training and validation scores, indicating strong model generalization.

---

# Feature Importance Analysis

Feature importance analysis using Random Forest showed that:

* Smoking status
* BMI-Smoker interaction
* BMI
* Age

were among the most influential predictors of insurance costs.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Jupyter Notebook / Kaggle Notebook

---

# Project Structure
```text id="4jlwmk"
├── data/
│   └── insurance.csv
├── notebooks/
│   └── insurance_eda_v1.ipynb
├── images/
│   ├── feature_importance.png
│   ├── learning_curve.png
│   ├── actual_vs_predicted.png
│   └── correlation_heatmap.png
├── README.md
└── requirements.txt
```

---

# Key Insights

* Smoking significantly increases insurance charges.
* BMI strongly affects healthcare costs.
* Feature engineering substantially improved model performance.
* Tree-based ensemble methods outperformed traditional linear models.
* XGBoost achieved the best balance between bias and variance.

---

# Future Improvements

Potential future enhancements include:

* Hyperparameter tuning using GridSearchCV
* Cross-validation optimization
* SHAP value explainability
* Model deployment using Flask or Streamlit
* Docker containerization

---

# Dataset Source

Dataset obtained from:

[Kaggle](https://www.kaggle.com)

---

# Conclusion

This project demonstrates a complete machine learning regression workflow, including preprocessing, feature engineering, model comparison, evaluation, and visualization. Multiple algorithms were explored, with XGBoost achieving the best predictive performance for estimating medical insurance costs.
