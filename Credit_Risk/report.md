# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of this analysis was to use data to see if a borrower could be entrusted to pay back a loan.  If a borrower could be entrusted, the loan would be considered healthy or a 0.  If a borrower could not be trusted to repay the loan, it was deemed an unhealthy loan, or a 1.
* Explain what financial information the data was on, and what you needed to predict.
The data used to predict was the loan amount, the loan interest rate, the borrower's income, their debt to income ratio, their number of accounts, any derogatory marks, and their total debt.  Based on this data, we needed to predict if the borrower can be entrusted to repay the loan and have their loan be considered healthy.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
We basically needed/wanted to know just how much data we have to work with and how balanced/imbalanced the data is.
* Describe the stages of the machine learning process you went through as part of this analysis.
I split the data using train_test_split.  Then I used the LogisticRegression model and fit it usig the training data.  Then made predictions based on that fit.  I calculated the accuracy score, generated a confusion matrix, and printed the classification report. I repeated those steps using resampled data using RandomOverSampler.  
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:  LogisticRegression
  * Accuracy Score:  0.992
  * Precision Score:  0:  1.00, 1:  0.87
  * Recall Score:  0:  1.00, 1:  0.89


* Machine Learning Model 2:  LogisticRegression w/ resampled data
  * Accuracy Score:  0.995
  * Precision Score:  0:  1.00, 1:  0.87
  * Recall Score:  0:  1.00, 1:  1.00
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
It seems that the second model performed better because it has a higher accuracy score.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
However, the data is very imbalanced and tends to lean more toward healthy '0' loans.  So the model and predictions will follow suite and unfortunately grant more people loans than what the actual data would support.  The lender may then not receive repayment on some of those loans that were probably a 1 but the model predicted as 0.

If you do not recommend any of the models, please justify your reasoning.
I would not recommend either of these models to make these predictions.  I would gather more data and strive for a more balanced data set and rerun the models.
