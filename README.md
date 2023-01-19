# Credit Risk Analysis

## Overview: 

### There are many factors that go into the decision to approve of loans. Lending organizations use many variables to predict credit risk and determine the likelihood that a borrower may default on a loan. 

### Predicting credit risk can easily become complicated, as it is something that may vary widely depending on individual circumstances of each borrower; there are several known predictors of risk however, many of which have strong associations.

### Supervised machine learning may be utilized to evaluate credit risk, given data sets with known information about risk factors and predictors. This project was performed on behalf of Lending Club, a peer to peer lending service, in order to evaluate the performance of several supervised machine learning algorithms in predicting credit risk. 

## Results: 

#### Oversampling RandomOverSampler algorithm: Naive oversampling randomly takes observations from the minority class and adds them to the training data set, replacing them as it goes.
#### The balanced accuracy score of 0.64 suggests that this model is better than random chance, but still mediocre. The precision of 0.99 does suggest that this model has a high sensitivity, but the lower recall of 0.65reveals that it is not as good at identifying all positives, misclassifying a signifiant number as negatives.  
![Image 1](https://github.com/elissewright/Credit_Risk_Analysis/blob/main/Images/1.png)

#### Oversampling SMOTE algorithm: SMOTE generates synthetic samples for the minority class, and is a popular machine learning approach for sets with imbalanced data. 
#### This model is a similar performer to Random Oversampling, with a balanced accuracy score of 0.63, precision of 0.99, and recall of 0.64.
![Image 2](https://github.com/elissewright/Credit_Risk_Analysis/blob/main/Images/2.png)

#### Undersampling ClusterCentroids algorithm: This algorithm uses K-means to cluster similar data based on proximity to a central point. 
#### While the balanced accuracy score and precision for this model follow the trends of the previous models at 0.63 and 0.99, respectively, the recall of 0.45 suggests this might be the weakest performing model so far.  
![Image 3](https://github.com/elissewright/Credit_Risk_Analysis/blob/main/Images/3.png)

#### Over and Undersampling SMOTEEN algorithms: SMOTEEN is also used for imbalanced data sets, and combines SMOTE methods with K-means to look for nearest neighbors of each observation. 
#### The combination approach has the worst balanced accuracy score yet at 0.53, suggesting this model is no better than randomly guessing. The precision remains at 0.99, with recall of 0.45. 
![Image 4](https://github.com/elissewright/Credit_Risk_Analysis/blob/main/Images/4.png)

#### BalancedRandomForestCLassifier: This model takes trees and contructs bootstrap samples of each, then randomly under-samples each one to balance it. 
#### This model exceeds the performance of the previous ones on all metrics, with a balanced accuracy score of 0.79, precision of 0.99, and recall of 0.91. 
![Image 5](https://github.com/elissewright/Credit_Risk_Analysis/blob/main/Images/5.png)

#### EasyEnsembleClassifier: This algorithm is used to create ensemble sets with random undersampling, selecting random subsets to make ensembles of them. It combines several weaker machine learning techniques in one in order to make an overall strong algorithm. 
#### Out of all models, this was the strongest performer by far, with a balanced accuracy score of 0.93, a precision of 0.99, and a recall of 0.94. 
![Image 6](https://github.com/elissewright/Credit_Risk_Analysis/blob/main/Images/6.png)

## Summary: 

### Based on these results, I do not recommend the combined SMOTEEN approach or the Cluster Centroids algorithm, both of which were the worst performers out of the bunch. 

### The best performing, highly recommended models are the Balanced Random Forest Classifier and the Easy Ensemble Classifier, both of which consistently had high scores across all metrics.

