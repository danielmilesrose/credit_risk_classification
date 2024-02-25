# Module 12 Report Template

## Overview of the Analysis
We completed this analysis with the purpose of identifying and predicting loan risk.  The data we looked at included the loan size, the interest
rate, the income of the borrower, the borrower's debt to income ratio, the number of accounts the borrower has, derogatory marks on the borrower's
account, and the total debt of the borrower.  

We analyzed 77536 loans which we split into training and testing sets, using the training set to fit the Logistic Regression Model to predict the
testing set.  We used two models, one based on the original data provided in the csv, and the second based on oversampled data that we got from using 
RandomOverSampler from imblearn.

The first model had 75036 entries in the `0` category (which signifies healthy loans) and 2500 entries in the `1` category, or high risk loans.  After 
we used the RandomOverSampler on the second model, this produced 56271 entries in each category, giving us a more balanaced view.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced Accuracy Score: 96.72%
  * Precision:
    * loan_status `0` (Healthy Loans) - 100%
    * loan_status `1` (High-Risk Loans) - 84%
  * Recall:
    * loan_status `0` (Healthy Loans) - 99%
    * loan_status `1` (High-Risk Loans) - 94%


* Machine Learning Model 2:
  * Balanced Accuracy Score: 99.36%
  * Precision:
    * loan_status `0` (Healthy Loans) - 100%
    * loan_status `1` (High-Risk Loans) - 84%
  * Recall:
    * loan_status `0` (Healthy Loans) - 99%
    * loan_status `1` (High-Risk Loans) - 99%

## Summary

After reviewing the data produced by the two models, the second, oversampled model performs the best of the two.  
  * The balanced accuracy score for Model 2 is higher than that from Model 1.
  * The Precision across both categories is the same for Model 1 and Model 2.
  * The recall for Healthy Loans `0` is the same for both models, but the Recall for the High-Risk Loans `1` is 5% higher on Model 2 than Model 1, making it the more accurate model.
  * Because it's much more important to predict the `1`'s, as it's less risky to accidentally characterize Healthy loans as High Risk than it would be to accidentally label a High-Risk loan as Healthy, I would recommend using Model 2, the Oversampled model.
