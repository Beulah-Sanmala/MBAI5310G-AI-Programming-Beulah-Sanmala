# Ecommerce Customer Churn Prediction – Machine Learning Pipeline

## Assignment Overview
This assignment builds a complete end-to-end machine learning pipeline to predict customer churn in an ecommerce business using Python and Scikit-learn. The goal of the project is to identify customers who are likely to stop using the ecommerce platform based on customer demographics, purchasing behavior, and engagement information.

This assignment demonstrates the major stages of a machine learning workflow, including data preprocessing, feature engineering, model training, and model evaluation.

---

# Business Problem
Customer churn is a major challenge for ecommerce companies because losing customers directly affects revenue and long-term growth. Predicting churn allows businesses to take preventive actions such as personalized marketing campaigns, loyalty rewards, and improved customer support.

The objective of this project is to build a classification model that predicts whether a customer will churn or remain active.

---

# Dataset Used
The dataset used is the **Ecommerce Customer Churn Dataset**.

The dataset contains:
- Customer demographic information
- Spending behavior
- Purchase history
- Customer engagement information
- Service-related metrics

---

# Features and Target Variable

## Target Variable
```python
Churned
```

- `Yes` → Customer churned
- `No` → Customer remained active

---

## Features Used
The following features were selected for model training:

- Age
- Gender
- Region
- Membership Type
- Monthly Spending
- Number of Orders
- Days Since Last Purchase
- Customer Support Calls
- Average Rating
- Coupon Usage
- Newsletter Subscription
- Device Type

The `Customer_ID` column was removed because it only serves as an identifier and does not contribute meaningful predictive information.

---

# Machine Learning Pipeline

The notebook follows a structured machine learning workflow:

1. Load and inspect the dataset
2. Understand the business problem
3. Identify features and target variable
4. Define X and y
5. Handle missing values
6. Separate numerical and categorical features
7. Apply preprocessing using:
   - `SimpleImputer`
   - `StandardScaler`
   - `OneHotEncoder`
8. Split the data into training and testing sets
9. Build a preprocessing pipeline using `ColumnTransformer`
10. Train a baseline Logistic Regression model
11. Evaluate model performance

---

# Model Used
A **Logistic Regression** model was used as the baseline classification algorithm because:
- The target variable is binary
- Logistic Regression is simple and interpretable
- It provides a strong baseline for classification problems

---

# Results Obtained

The Logistic Regression model achieved the following evaluation results:

- **Accuracy:** 0.8154
- **Precision:** 0.6471
- **Recall:** 0.6471
- **F1-score:** 0.6471

These results show that the model was able to classify customer churn with reasonably good performance using the available customer information.

---

# Limitations

Some limitations of this assignment include:

- Logistic Regression is a linear model and may not capture complex non-linear customer behavior patterns
- The dataset may not contain all factors affecting customer churn
- External variables such as competitor pricing, marketing campaigns, and customer satisfaction history were not included

Future improvements could include:
- Random Forest
- XGBoost
- Neural Networks
- Hyperparameter tuning
- Feature engineering

---

# Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

---

# Files Included

- `Week 2 Ecommerce Assignment.ipynb `
- `ecommerce_customer_churn_dataset.csv`
- `README.md`

---

# Conclusion
This assignment successfully demonstrates a complete machine learning pipeline for customer churn prediction. The notebook includes data preprocessing, feature selection, model training, evaluation, and interpretation of results using industry-standard machine learning practices.
[Week 2 Ecommerce Assignment.ipynb](https://github.com/user-attachments/files/28194576/Week.2.Ecommerce.Assignment.ipynb)
