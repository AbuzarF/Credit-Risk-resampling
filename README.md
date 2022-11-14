# Credit-Risk-resampling

# Analysis of the Machine Learning Model


## Explain the purpose of the analysis: 
#### Logistic Regression is a statistical method fo predicting binary outcomes from data. The purpose of this analysis is to predict if the loan is a high-risk or not by using the given financial information by incorporating the data into the Logistic Regression Model.

## Explain what financial information the data was on, and what you needed to predict:
#### For our purpose of analysis we used Loan size (X features) and the  loan status (y variable). In this analysis we are predicting the loan status, i.e. if the loan is a high-risk or not. The data is imbalanced and contain around 3% high-risk loans.

## Provide basic information about the variables you were trying to predict (e.g., `value_counts`):
#### when we analysed the *balance* of our target values, we found that out of 77536, only 2500 were flagged as high-risk loans. The data is hghly imbalanced and  may caused the data to potentially flag the high-risk loan as non-risky.

##  Describe the stages of the machine learning process you went through as part of this analysis:
#### In predicting the values, we performed the following steps:
* Pulled the data and read it into the data frame
* Dropped the Loan status column from the original data and labeled as y variable
* The remaining columns were labeled as X features
* Calculated the value counts
* Split the data into train and test data sets. By default 75% of data was used to train the model and 25% used to test the model.
* Fit the model on the training data (X_train, y_train)
* Made predictions using the test data and pulled it into a data frame
* Evaluated the model's performance by calculating the balanced_accuracy score, confusion_matrix and classification_report for imbalanced data.
* Given the data was imbalanced, we then resampled the data by using the RandomOverSampler model to account for the imbalance in the data. Calculation was made on over sampled data as mentioned above

## Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method:
#### We used the LogisticRegression model to make predictions on high-risk loans. Since we found that the data was imbalanced, we used the Random Over Sample method to resample the data and account for imbalance in the data.

## Results

## Machine Learning Model 1:
## Description of Model 1 Accuracy, Precision, and Recall scores:

* Balanced Accuracy Score: 0.9520479254722232
* Precision for non-risky loans: 1
* Precision for high risk loans: 0.85 

* Recall for non-risky loans: 0.99
* Recall for high risk loans: 0.91

## Machine Learning Model 2:
## Description of Model 2 Accuracy, Precision, and Recall scores:

* Balanced Accuracy Score: 0.9936781215845847
* Precision for non-risky loans: 1
* Precision for high risk loans: 0.84

* Recall for non-risky loans: 0.99
* Recall for high risk loans: 0.99

## Summary

### Which one seems to perform best? How do you know it performs best?
#### Keeping in view, Model 2 performed better. The balanced accuracy score improved from 0.95204 to 0.99367 and the recall for high risk loans also improved from 0.91 to 0.99. 
#### However, when considering the precision scores, Model 1 performed slightly better(0.85), then 0.84 in Model 2.
The overall performance of Model 2 is better. When considering the pecision score, Model 1 appeared to work better because the precision score is more important.

## Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
#### The answer is Yes. It is important to predict '1's  accurately as it represents hig risk loans. It would be costly to flag a high risk loans as non-risky. The overall performance of the precision score gain importance to  look at.

## If you do not recommend any of the models, please justify your reasoning.
#### Comparing precision scores, non of the models accurately classifying high-risk-loans. It is recommended to test other machine learning models, such as Random Forest or Support Vector Machine. If these models produce better precision scores then LogisticRegression model, it is worth considering looking at it.

 



