# Challenge 17, Supervised Machine Learning and Credit Risk

## Project Overview

In this challenge, we’ll use Python to build and evaluate several machine learning models to predict credit risk. 
The goals of this challenge are to:

1. Implement machine learning models.
2. Use resampling to attempt to address class imbalance.
3. Evaluate the performance of machine learning models.

## Resources
Python 3.7

# Summary
We took some preprocessing steps prior to applying machine learning models to the dataset including:
- dropping nan values
- converting interest rate to numerical values instead of string
- converting/summarizing the traget column to low and high risk (binary)
- dropping columns with only one value (useless in prediction models)
- encoding the categorical features

Several supervised machine learning models were applied on the dataset including, and the results are shown below:

| Logistic Regression Model using Name  | Recall | Precision | f1 score | Support | Balanced Accuracy Score |
| ----------- | ------ | --------- | -------- | ------- | ----------------------- |
| Random Oversampling | 0.68 | 0.01 | 0.02 | 101 | 0.666 |
| SMOTE | 0.65 | 0.01 | 0.02 | 101 | 0.661 |
| Cluster Centroid Undersampling | 0.66 | 0.01 | 0.02 | 101 | 0.535 |
| SMOTEENN | 0.75 | 0.01 | 0.02 | 101 | 0.664 |
| Balanced Random Forest | 0.89 | 0.03 | 0.06 | 101 | 0.772 |
| **Easy Ensemble AdaBoost** | **0.92** | **0.09** | **0.16** | **101** | **0.932** |

Amongst all the models, Easy Ensemble AdaBoost shows a significantly higher Recall and Balanced Accuracy Score. These two parameters are very important in classification problems similar to credit risk. Thus, **Easy Ensemble AdaBoost** will be chosen as the model with the best performance.


