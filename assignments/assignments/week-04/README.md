# Assignment 4 – Decision Tree Model and Business Interpretation

## Business Problem

FreshBasket is a subscription-based grocery delivery service operating in the Greater Toronto Area. The business depends on recurring customers, so customer churn is a serious problem. When customers cancel or do not renew their subscriptions, FreshBasket loses recurring revenue and may need to spend more money acquiring new customers.

The goal of this assignment is to build a Decision Tree classification model that predicts whether a customer is likely to churn. The model is used as a decision-support tool to help FreshBasket identify at-risk customers and take proactive retention actions.

## Dataset

The dataset used in this assignment is `freshbasket_customer_churn_dataset.xlsx`.

The dataset contains customer demographic, subscription, spending, service-quality, and engagement information. The target variable is `Churned`, which shows whether a customer cancelled or did not renew the subscription.

## Target Variable

`Churned`

- `Yes` = customer churned
- `No` = customer did not churn

## Machine Learning Model

The model used is a Decision Tree Classifier.

The model was selected because Decision Trees are easy to interpret and can show which features are most important in predicting churn. The model used controlled settings to reduce overfitting:

- `max_depth = 5`
- `min_samples_leaf = 8`
- `class_weight = balanced`

## Data Preparation

The following steps were completed:

- Loaded the Excel dataset
- Checked rows and columns
- Checked column names and data types
- Checked missing values
- Checked duplicate rows
- Removed duplicate records
- Removed the Customer_ID column from model training
- Converted the target variable into binary form
- Handled missing numerical and categorical values
- Encoded categorical variables using one-hot encoding
- Split the dataset into training and testing sets

## Class Imbalance

The dataset is somewhat imbalanced. About 72% of customers are non-churned customers and about 28% are churned customers.

This is important because a model can appear accurate by predicting the majority class more often. For a churn prediction problem, recall and F1-score are important because the business needs to identify customers who are actually likely to leave.

## Model Results

| Metric | Result |
|---|---:|
| Training Accuracy | 66.4% |
| Testing Accuracy | 60.7% |
| Precision | 39.1% |
| Recall | 78.3% |
| F1-score | 52.2% |

## Confusion Matrix Interpretation

The model produced the following results on the testing dataset:

- 33 customers were correctly predicted as No Churn
- 18 customers were correctly predicted as Churn
- 28 customers were incorrectly predicted as Churn even though they stayed
- 5 customers were incorrectly predicted as No Churn even though they churned

In simple words, the model was strong at finding actual churned customers. It correctly identified 18 out of 23 churned customers. This is useful for FreshBasket because recall is important in churn prediction. However, the model also produced several false positives, meaning some customers may receive retention attention even though they would have stayed.

## Key Business Insights

The most important features were:

1. Satisfaction_Score
2. Monthly_Spend
3. Orders_Last_3_Months
4. App_Engagement_Score
5. Average_Order_Value
6. Region_Toronto
7. Customer_Service_Tickets

These features suggest that customer satisfaction, spending behaviour, order activity, app engagement, and service interactions are important signals for churn risk.

## Business Recommendation

FreshBasket should use the model as an early warning tool for customer churn. Customers predicted as high risk should be reviewed by managers or customer support staff. The business can then decide whether to provide a retention offer, improve service, investigate delivery issues, or recommend a better subscription plan.

Because recall is high, the model is useful for finding many at-risk customers. However, because precision is lower, the business should not automatically send expensive discounts to every predicted churn customer. Human review should be used before taking costly action.

## Limitation

One limitation is that the dataset is synthetic and simplified for educational purposes. It may not fully represent real customer behaviour, seasonal grocery demand, competitor promotions, or unexpected delivery problems.

Another limitation is class imbalance. There are more non-churned customers than churned customers, which may affect model performance.

## Responsible AI Reflection

The Decision Tree model should support business decisions, not replace human judgment. Managers should review customer context, avoid unfair treatment, protect privacy, and make sure that retention actions are helpful rather than intrusive.
