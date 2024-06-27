# Module-20-Supervised-Learning

## Using Supervised Learning techniques to train and evaluate a model based on loan risk. Building a model of historical lending activity from a peer-to-peer lending services company to identify the credit-worthiness of borrowers.

## Overview of the Analysis

* The purpose of this analysis is to use historical lending data from a peer to peer lending services company to build a supervised machine learning model to identify the credit-worthiness of borrowers.
* The data contains variables such as the size of the loan, interest rate, income of the borrower, debt-to-income ratio, number of accounts, derogatory remarks, and total debt size to predict the loan status of the borrower (0 for healthy, 1 for high-risk).
* The original data contained 77536 records.
* Supervised machine learning was used to generate a model for analysis. 

The loan status columns was used as the labels, while the rest of the data was used as the features. 

The data was split into training and testing data; the model was trained on approximately 75% of the data (using LogisticRegression on the training features and training labels).

As for the remaining 25% of the data, the features (test features) were used to test the model, with the results being measured up against the actual values from the test labels.

A confusion matrix was generated with this testing data, as well as a classification report.

## Results

* Machine Learning Model 1:
  * The precision for healthy loans is 1.00.
    * The model identified 18759 of the test data loans as healthy. Of these 18759, 18679 are actually healthy. This indicates that virtually all the healthy loans predicted by the model are actually healthy.
  * The recall for healthy loans is 1.00
   * The model only misidentified 67 of the test data healthy loans as being high-risk. i.e there are actually 18746 healthy loans, and the model was able to classify 18679 of these as healthy.
  * The precision for high-risk loans is 0.87
   * 87% of test data loans identified as high-risk are actually high-risk 
  * The recall for high-risk loans is 0.89
   * The model was able to predict 89% of the test data high-risk loans as being high-risk

## Summary

In conclusion, this model would be a good choice to use when investigating credit-worthiness of borrowers, as it is able to identify healthy loans almost 100% of the time. Even though it is not as good as identifying high-risk borrowers, it is still fairly capable, as the f1-score for high-risk borrowers is close to 90%.

Sources and help:
[Confusion Matrix)](https://www.datacamp.com/tutorial/what-is-a-confusion-matrix-in-machine-learning?dc_referrer=https%3A%2F%2Fwww.google.com%2F)
