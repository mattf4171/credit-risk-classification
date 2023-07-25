# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of this analysis is to best guide a company about loaning to prospecitve applicants.
* This data was base on features like loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, and total_debt for the purpose of best classifying a healthy loan vs a high-risk loan. 
* There is a much high sample size of healthy loan examples as opposed to high-risk loans.
* In order to perform machine learning on this data we needed seperate our predictor variables and our target variable. We then needed to ensure we have training data to train on and testing data to test the performance of our LogisticRegression model. Then we upsampled the minority target class, in this case the high-risk loan category and re-trained our model so that it would avoid blindly guessing the majority class. This improved our models overall performance.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * The logistic regression model predicts healthy loan very well with perfect precision and almost perfect recall. For high-risk loan we see that logistic regression has made some false positive results implying that those with a high-risk loan at times are not labeled as such, and for recall we have a few false negatives meaning that this model assumes some credit reports are not high-risk when indeed they are. The accuracy of our model is 95% which is great, but let us attempt to get better results for precision and recall by oversampling traininig data.



* Machine Learning Model 2:
  * Our new logistic regression model after applying oversampling method performs better at improving false negative values for high-risk loan category. This is great because we would prefer to have predicted a high-risk loan scenario when in fact it is not a high risk. We certainly see a trade off as opposed to a non-oversampled model, in this case this model has a larger f-score, indicating a much better performing model.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* The second model performs best, we know this because our f1 score is much higher telling us that our precision and recall on average are higher than our initial Logistic Regression model.
* Yes the performance depends on this binary classification task of healthy vs high-risk loans. In our case we would prefer to predict an instance as a high-risk when in fact it is a healthy loan as opposed to predicting a loan to be healthy when in fact it is a high-risk. This is due to the nature of loaning to those whom would pay forward their loan rather than those who may default on payments. A company would much rather have more False Positive values associated with predicting a high-risk when in fact it is a healthy loan type. It is also in an investors best intrest to have fewer False Negative values meaning the predicted category is Healthy but in fact the actual true category was a high-risk loan.
