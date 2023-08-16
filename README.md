# Module 12 Report: Credit-Risk-Classification
## Overview of the Analysis

The purpose of the Credit Risk Analysis is to predict the health of the loan of borrowers according to the loan size, interest rate, the borrower's debt to income ratio, income, number of accounts, derogatory marks and total debt. The financial information used is the loan status, for which 'y' label was created, comparing to the rest of the mentioned financial information; the loan status shows a value of 0 or 1: 0 meaning the loan is healthy, and 1 meaning that the loan has a high risk of defaulting. The 'y' label takes the "loan status" values, and separates the rest of the columns into an array saved in the 'X' variable label.

To create the machine learning process, the data was split into training and test sets by creating the 'X' and 'y' variables as previously mentioned. Data was split and trained by using the sklearn model to "train_test_split", which reshaped the data by the default ratios of 75% of the data for train, and 25% to test, and a random state equals to 1 to ensure the data splitting is reproducible and consistent across different runs. From there the data was fit into a logistic regression model. 

To evaluate the performance of the model, the balance accuracy score was calculated, as well as the confusion matrix, and the classification report showing the precision, recall, f1-score, and support. The analysis was performed twice, the first time using the original dataset, while the second time considering "random over sampled" resampled data. The following are the results of both of the machine learning models:

## Results
* Machine Learning Model 1 (original dataset):
  * Balanced accuracy score: The score of 0.952 suggests that the model has achieved a high level of accuracy while considering class imbalances.
  * Confusion matrix: the confusion matrix shows a good standing model because the false negative is not higher than the false positive value.
  * Classification: the classification report indicates that the model performs very well, particularly in predicting "Healthy Loan" cases. It has high precision and recall for both classes, which suggests a good balance between minimizing false positives and false negatives. The high F1-scores and accuracy further reinforce the model's strong performance.

* Machine Learning Model 2 (resampled data):
  * Balanced accuracy score: 0.9947 indicates that the model is performing better than the machine learning model 1. The model correctly predicts around 99.47% of cases. 
  * Confusion matrix: the confusion matrix remains a good standing model. It continues to show that the false negative is not higher than the false positive value.
  * Classification: the classification report scores are even higher in the resampled data than the original dataset. This is because the application of random oversampling creates a balanced dataset that provides the model more examples from the minority class, allowing it to learn patterns more effectively.
  
## Summary
The machine learning model number 2 seems to perform best due to its higher accuracy and classification scores, however it is important to consider the context and purpose of the model's use to determine which model to choose for performance purposes. The performance depends on the problem we are trying to solve, in this case is for prediction of the health of loans. For the credit risk classification I would choose model 1 for the realistic distribution reason. However I would consider using model 2 as a hybrid for training and validation purposes. 

## References
Code and analysis developed in support from UCB in class examples and lectures.
