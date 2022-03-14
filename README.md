# Credit Risk Analysis

## Analysis Overview
In this analysis, we are using Python to build and evaluate machine learning models to predict credit risk. 
We adopted the following procedure:

* Oversample the data using the RandomOverSampler and SMOTE algorithms.
* Undersample the data using the ClusterCentroids algorithm.
* Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
* Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.
We will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

##Results 

### RandomOverSampler Model
* The balanced accuracy score was about 65%
* The high_risk precision was only about 1% with 62% sensitivity.

### SMOTE Model
* Similar to the randomoversampler model. 
* balance accuracy score of about 64%
* Same high_risk precision, with a 63% sensitivity.

### ClusterCentroids Model 
* The balance accuracy score was a low 52%
* Same high_risk precision of 1% with 63% sensitivity. 

### SMOTEENN Model 
* The balanced accuracy score is about 62%.
* The high_risk precision is still 1% only with 68% sensitivity.

### BalancedRandomForestClassifier Model 
* The balanced accuracy score improved to about 79%.
* The high_risk precision is still low at 4% only with 67% sensitivity.

### EasyEndembleClassifier Model 
* Now, the balanced accuracy score is high to about 93%
* The high_risk precision is still low at 7% only with 91% sensitivity

## Summary 
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high. The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.
