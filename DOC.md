# Introduction
This model uses XGBOOST to predict whether an employee would quit a company using features like estimated salary,tenure etc. and obtains mean accuracy of using K-Fold Cross Validation

XGBoost is one of the most popular machine learning algorithm these days. Regardless of the type of prediction task at hand; regression or classification.
XGBoost is well known to provide better solutions than other machine learning algorithms. In fact, since its inception, it has become the "state-of-the-art” machine learning algorithm to deal with structured data.

## Boosting

Boosting is a sequential technique which works on the principle of an ensemble. It combines a set of weak learners and delivers improved prediction accuracy. At any instant t, the model outcomes are weighed based on the outcomes of previous instant t-1. The outcomes predicted correctly are given a lower weight and the ones miss-classified are weighted higher.

## Dataset and features
The dataset is a compilation of records of various employees and their following features:

'CustomerId', 'Surname', 'CreditScore', 'Geography','Gender', 'Age', 'Tenure', 'Balance', 'NumOfProducts', 'HasCrCard','IsActiveMember', 'EstimatedSalary', 'Exited'

The last of them is the target variable for us while the rest comprise the feature-set X

## XGBoost's hyperparameters


    learning_rate: step size shrinkage used to prevent overfitting. Range is [0,1]
    max_depth: determines how deeply each tree is allowed to grow during any boosting round.
    subsample: percentage of samples used per tree. Low value can lead to underfitting.
    colsample_bytree: percentage of features used per tree. High value can lead to overfitting.
    n_estimators: number of trees you want to build.
    objective: determines the loss function to be used like reg:linear for regression problems, reg:logistic for classification problems with only decision, binary:logistic for classification problems with probability.

XGBoost also supports regularization parameters to penalize models as they become more complex and reduce them to simple (parsimonious) models.

    gamma: controls whether a given node will split based on the expected reduction in loss after the split. A higher value leads to fewer splits. Supported only for tree-based learners.
    alpha: L1 regularization on leaf weights. A large value leads to more regularization.
    lambda: L2 regularization on leaf weights and is smoother than L1 regularization.



## References:
https://www.datacamp.com/community/tutorials/xgboost-in-python
