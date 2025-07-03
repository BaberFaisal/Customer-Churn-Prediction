#  Customer Churn Prediction

This project implements a complete machine learning pipeline to predict **customer churn**. It includes **synthetic data generation**, **EDA**, **feature engineering**, **model training**, and **evaluation using multiple metrics**. The project mimics a real-world telecom use case to identify customers likely to leave the service.

---

##  Table of Contents

1. [Project Overview](#project-overview)
2. [Libraries Used](#libraries-used)
3. [Data Generation](#data-generation)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Data Preprocessing](#data-preprocessing)
6. [Feature Engineering](#feature-engineering)
7. [Modeling](#modeling)
8. [Model Evaluation](#model-evaluation)
9. [Conclusion](#conclusion)
10. [Future Work](#future-work)

---

##  Project Overview

The aim of this notebook is to build a supervised learning pipeline for **binary classification** to determine whether a customer will churn or not. Key business implications include improved customer retention and reduced revenue loss.

---

##  Libraries Used

The project uses the following Python libraries:

- `pandas`, `numpy`: For data manipulation  
- `matplotlib`, `seaborn`: For visualization  
- `scikit-learn`: For modeling, preprocessing, and evaluation  
- `xgboost`: For advanced gradient boosting modeling  
- `warnings`: To suppress unnecessary output  

---

##  Data Generation

Synthetic data is generated with fields resembling real customer demographics and telecom service usage, such as:

- Gender, SeniorCitizen, Partner, Dependents  
- Tenure, MonthlyCharges, TotalCharges  
- Services used: InternetService, TechSupport, StreamingTV, etc.  
- Target variable: `Churn` (Yes/No)

This enables testing the ML pipeline without needing proprietary data.

---

##  Exploratory Data Analysis (EDA)

Key steps include:

- Checking data types and distributions  
- Visualizing target balance (churn vs. non-churn)  
- Analyzing correlations between features  
- Using plots to understand patterns (boxplots, histograms, etc.)  

---

##  Data Preprocessing

-  **Missing Data Handling**: Replaced or imputed as needed  
-  **Categorical Encoding**: Applied one-hot encoding and label encoding  
-  **Normalization**: Continuous variables scaled using `StandardScaler`

This ensures clean and model-ready data.

---

##  Feature Engineering

-  **Tenure Buckets**: Grouped tenure into categorical bins  
-  **Customer Value Metrics**: Combined features like charges and services  
-  **Interaction Terms**: Optionally tested interaction of categorical features  
-  Feature selection based on correlation and importance scores

---

##  Modeling

Multiple machine learning algorithms are trained:

- `Logistic Regression`  
- `Random Forest Classifier`  
- `XGBoost Classifier`  

Each model is trained with 5-fold cross-validation and hyperparameter tuning using `GridSearchCV`.

---

##  Model Evaluation

Each model is evaluated using:

-  Accuracy  
-  Precision, Recall, F1-score  
-  ROC-AUC Score  
-  Confusion Matrix  
-  Precision-Recall Curve, ROC Curve  

These metrics ensure the model balances true positives and false positives effectively.

---

##  Best Performing Model

The **XGBoost Classifier** performs best based on validation metrics:

- Excellent balance of precision and recall  
- High ROC-AUC score  
- Consistent performance across different churn rates

---

##  Conclusion

This notebook successfully demonstrates:

- A full customer churn prediction pipeline  
- Synthetic but realistic customer data  
- EDA, preprocessing, modeling, and evaluation steps  
- Use of interpretable metrics to assess model quality

---

## Future Work

- Train on **real-world telecom datasets**  
- Deploy the model with **Flask or FastAPI** for live predictions  
- Use **SHAP** for model explainability  
- Continuously retrain model with fresh data  
- Explore **AutoML frameworks** for faster prototyping
