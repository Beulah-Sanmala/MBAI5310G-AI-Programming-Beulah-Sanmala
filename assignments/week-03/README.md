# Assignment 3 – Classification Model Comparison

## Assignment Overview

This assignment compares two machine learning classification models, **Logistic Regression** and **Support Vector Machine (SVM)**, for predicting customer churn in an ecommerce business. The objective is to identify customers who are likely to stop using the platform based on customer demographic information, purchasing behavior, and engagement metrics.

The assignment demonstrates a complete machine learning workflow, including data preprocessing, model training, performance evaluation, and business interpretation of results.

---

## Dataset Used

The dataset used for this assignment is the **Ecommerce Customer Churn Dataset**. The dataset contains customer demographic, spending, engagement, and service-related information that can be used to predict whether a customer will churn.

---

## Target Variable

The target variable selected for prediction is:

```python
Churned
```

Where:

- **Yes** = Customer churned
- **No** = Customer remained active

---

## Features Used

The following features were used for model training:

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

The `Customer_ID` column was excluded because it serves only as a unique identifier and does not provide meaningful predictive information.

---

## Models Compared

Two classification models were trained and evaluated:

### 1. Logistic Regression
A simple and interpretable classification algorithm commonly used as a baseline model for binary classification problems.

### 2. Support Vector Machine (SVM)
A more advanced classification algorithm capable of identifying complex decision boundaries between classes.

---

## Evaluation Metrics

Both models were evaluated using:

- Confusion Matrix
- Accuracy
- Precision
- Recall
- F1-score

These metrics provide a comprehensive assessment of classification performance.

---

## Model Comparison

The performance of Logistic Regression and SVM was compared using the evaluation metrics calculated on the testing dataset.

The model with the higher overall performance, particularly in terms of Recall and F1-score, was considered the stronger model for customer churn prediction.

---

## Business Interpretation

For customer churn prediction, **Recall** is one of the most important evaluation metrics because it measures how effectively the model identifies customers who are actually likely to leave.

A higher recall helps the business identify more at-risk customers and implement retention strategies before those customers churn.

---

## False Positives and False Negatives

### False Positive
A false positive occurs when the model predicts that a customer will churn, but the customer actually remains active.

This may result in unnecessary retention efforts and marketing costs.

### False Negative
A false negative occurs when the model predicts that a customer will remain active, but the customer actually churns.

This is generally more costly because the business loses a customer without taking any preventative action.

---

## Limitations

One limitation of this project is that the dataset may not include every factor influencing customer churn. External factors such as competitor pricing, customer satisfaction, product quality, and economic conditions are not captured in the dataset.

In addition, both models rely on historical data and may not fully reflect future customer behavior patterns.

---

## Importance of Human Judgment

Machine learning models provide valuable predictions but should not replace human decision-making. Business managers and analysts should use model predictions together with domain knowledge, customer feedback, and business strategy when making retention decisions.

Human judgment remains important for interpreting predictions and determining appropriate actions.

---

## Conclusion

This assignment successfully trained and compared two classification models, Logistic Regression and SVM, for ecommerce customer churn prediction. Both models were evaluated using confusion matrix, accuracy, precision, recall, and F1-score.

The project demonstrates a complete classification workflow, from data preprocessing and model training to evaluation and business interpretation, using Python and Scikit-learn.
