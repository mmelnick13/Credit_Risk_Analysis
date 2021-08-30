# Credit Risk Analysis

## Overview of the analysis
The purpose of this analysis was to evaluate the performance of models and makea  written recommendation on whether they can be used to predict credit this. This was done by using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, oversampling the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, using a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, comparing two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

## Results

### Naive Random Oversampling
- Accuracy Score: 64%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 62%
- Recall Low Risk: 67%

### SMOTE Oversampling
- Accuracy Score: 65%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 66%
- Recall Low Risk: 64%

### Cluster Centroid Undersampling
- Accuracy Score: 51%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 59%
- Recall Low Risk: 43%

### SMOTEENN Sampling
- Accuracy Score: 62%
- Precision High Risk: 1%
- Precision Low Risk: 100%
- Recall High Risk: 70%
- Recall Low Risk: 55%

### Balanced Random Forest Classifying
- Accuracy Score: 79%
- Precision High Risk: 4%
- Precision Low Risk: 100%
- Recall High Risk: 67%
- Recall Low Risk: 91%

### Easy Ensemble Classifying
- Accuracy Score: 93%
- Precision High Risk: 7%
- Precision Low Risk: 100%
- Recall High Risk: 91%
- Recall Low Risk: 94%

## Summary
This analysis is trying to find the best model that can detect if a loan is high risk or not. Becasue of that, we need to find a model that lets the least amount of high risk loans pass through undetected. That correlating statistic for this is the recall rate for high risk. Looking through the different models, the ones that scored the highest were:
- Easy Ensemble Classifying (91%)
- SMOTEENN Sampling (70%)
- Balanced Random Forest Classifying (67%)

While this is the most important statistic that is pulled from this analysis, another important statistic is recall rate for low risk as it shows how many low risk loans are flagged as high risk. Looking through the different models, the ones that scored the highest were:
- All samples had 100% precision low risk

After taking these two statistics over the others, we can look at the accurary score to get a picture of how well the model performs in general. The models with the highest accuracy scores were:
- Easy Ensemble Classify (93%)
- Balanced Random Forest Classifying (79%)
- SMOTEENN Sampling (62%)

After factoring in these three main statistics, the model that I would recommend to use for predicting high risk loans is the Easy Ensemble Classifying model.
