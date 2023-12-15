# Telecom Churn Prediction

## Problem Statement
In the telecommunications industry, customer retention is crucial due to the high rate of churn. Identifying and retaining high-value customers has become a primary business goal, considering the substantial cost difference between acquiring new customers and retaining existing ones.

## Goals and Objectives
- Define high-value customers and predict churn specifically among this segment.
- Develop models to forecast churn, serving the dual purpose of predicting potential churn and identifying key predictors of churn.

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
