# Telecom Churn

## Problem Statement

In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition. For many incumbent operators, retaining high profitable customers is the number one business goal. To reduce customer churn, telecom companies need to predict which customers are at high risk of churn.

## Goals and Objective
Define high-value customers and predict churn only on high-value customers
Build models to predict churn. The predictive model will serve two purposes:
It will be used to predict whether a high-value customer will churn or not, in near future
identify important variables that are strong predictors of churn

## Solution Overview
I created a Telecom Churn Prediction Model using Logistic Regression, a supervised learning algorithm.

### Data
- The dataset comprises 99,999 entries across 226 attributes.
- Customer data spans four months: June, July, August, and September (coded as 6, 7, 8, and 9).
- There was no pre-existing target or churn column. The objective was to predict churn in the ninth month using data from the first three months.
- The churn column was created based on criteria: customers who had zero calls (incoming and outgoing) and no mobile internet usage in the fourth month.

### High-Value Customer Identification
- High-value customers were defined as those who recharged with an amount equal to or more than the 70th percentile of the average recharge amount in the first two months.
- The resulting dataset consisted of 30,011 entries and 138 attributes, focusing on high-value customers.

### Data Preprocessing
- Techniques applied included:
  - Importing and understanding data.
  - Missing value check.
  - Data reduction, cleaning, and wrangling.
  - Feature engineering.
  - Univariate analysis.

### Handling Class Imbalance
- The churn column exhibited imbalance, addressed by using the SMOTE technique to obtain balanced churn data.

### Model Building and Evaluation
- Key steps included:
  - Splitting data into training and testing sets.
  - Feature scaling and selection.
  - Applying SMOTE for balanced data.
  - Building and training the model.
  - Evaluating model performance.
    - Accuracy score: 80.07%
    - Precision score: 26.52%
    - Recall score: 81.96%
    - ROC and AUC curve: 80.94%

### Conclusion
- The model achieved a precision score of 81.96%, indicating accuracy on test data.
- An AUC score of 80.94% signifies satisfactory discrimination between classes.
