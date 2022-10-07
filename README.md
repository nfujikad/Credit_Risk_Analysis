# Credit_Risk_Analysis

## Overview

The project utilized machine learning techniques to solve credit card risk. The task required different techniques to train and evaluate models with unbalanced classes.

1. 'imbalanced-learn'
2. 'scikit-learn'

These libraries build and evaluate models using resampling. 

The following steps:
1.	`RandomOverSampler` and `SMOTE` algorithms to oversample the data
2.	`ClusterCentroids` algrithom to undersample the data. 
3.	Combination of over- and undersampling using the `SMOTEENN` algorithm.
4.  `BalancedRandomForestClassifier` and `EasyEnsembleClassifier` to predict credit risk.
5.	Provide recommendation on whether these models should be used to predict credit risk

## Purpose

The goal is too:
1.	Use Resampling Models to Predict Credit Risk
2.	Use the SMOTEENN Algorithm to Predict Credit Risk
3.	Use Ensemble Classifiers to Predict Credit Risk
4.	Provide written report on the Credit Risk Analysis

## Results


### 1. RandomOverSampler

![01](https://github.com/nfujikad/Credit_Risk_Analysis/blob/main/Resources/1_Oversample.png)

- The balanced accuracy score is 65%.
- For high-risk, the precision score is 1%, recall score is 61%. Only 1% of predicted high-risk are true high-risk and 68% high-risk cases are correctly identified by this model with a F1 score of 2%. 
- For low-risk, the precision score is 100%, recall score is 68%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 61% low-risk are correctly identified with a F1 score of 81%.


### 2. SMOTE 

![02](https://github.com/nfujikad/Credit_Risk_Analysis/blob/main/Resources/2_SMOTE.png)

- The balanced accuracy score is 62%.
- For high-risk, the precision score is 1%, recall score is 61%. Only 1% of predicted high-risk are true high-risk and 61% high-risk cases are correctly identified by this model with a F1 score of 2%. 
- For low-risk, the precision score is 100%, recall score is 64%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 64% low-risk are correctly identified with a F1 score of 77%.

### 3. ClusterCentroids

![3](https://github.com/nfujikad/Credit_Risk_Analysis/blob/main/Resources/3_CLuster.png)

- The balanced accuracy score is 53%.
- For high-risk, the precision score is 1%, recall score is 61%. Only 1% of predicted high-risk are true high-risk and 61% high-risk cases are correctly identified by this model with a F1 score of 1%. 
- For low-risk, the precision score is 100%, recall score is 45%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 45% low-risk are correctly identified with a F1 score of 62%.

### 4. SMITEENN

![4](https://github.com/nfujikad/Credit_Risk_Analysis/blob/main/Resources/4_SMITEEN.png)

- The balanced accuracy score is 64%.
- For high-risk, the precision score is 1%, recall score is 70%. Only 1% of predicted high-risk are true high-risk and 70% high-risk cases are correctly identified by this model with a F1 score of 2%. 
- For low-risk, the precision score is 100%, recall score is 58%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 58% low-risk are correctly identified with a F1 score of 73%.

### 5. BalancedRandomForestClassifier

![5](https://github.com/nfujikad/Credit_Risk_Analysis/blob/main/Resources/5_BRFC.png)

- The balanced accuracy score is 79%.
- For high-risk, the precision score is 4%, recall score is 67%. 4% of predicted high-risk are true high-risk and 67% high-risk cases are correctly identified by this model with a F1 score of 7%. 
- For low-risk, the precision score is 100%, recall score is 91%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 91% low-risk are correctly identified with a F1 score of 95%.

### 6. EasyEnsembleClassifier

![6](https://github.com/nfujikad/Credit_Risk_Analysis/blob/main/Resources/6_Easy.png)

- The balanced accuracy score is 93%.
- For high-risk, the precision score is 7%, recall score is 91%. 7% of predicted high-risk are true high-risk and 91% high-risk cases are correctly identified by this model with a F1 score of 14%. 
- For low-risk, the precision score is 100%, recall score is 94%. Due to the small population of high-risk and large population of low-risk, almost 100% predicted low-risk are true low-risk, and 94% low-risk are correctly identified with a F1 score of 97%.

## Summary

In summary, `ClusterCentroids` has the lowest accuracy score, precision score, recall score and the F1 score. The best performing is `EasyEnsembleClassifier` with the highest accuracy score, precision score, recall score and F1 score. 


### Recommendation
With a small high-risk population, the precision scores of high-risk are extremely low for each model, and low-risk precision scores are almost 100% for all of the models. Regarding credit risk, it is of greater important to catch high-risk profiles vs. low-risk. In the anlysis the recall score for high-risk is influential, it states how many high-risk profiles can be identified among all real high-risk profiles. 

The comparisons show `EasyEnsembleClassifier` has the best performance specifically for high-risk profiles, identifying 92% of real high-risk profiles. At the same time, all of the models also falsely classified a large number of high-risk that are actually low-risk profiles (low precision scores of low-risk), so that many applicants will be falsely rejected.

In conclusion, if the bank just aims to catch as many high-risk as possible, `EasyEnsembleClassifier` would be the best choice. However, if the bank aims to accurately determine both low- and high-risk profiles, they should consider additional models not included in this analysis. 

