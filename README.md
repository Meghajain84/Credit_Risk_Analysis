# Credit_Risk_Analysis

## Overview of the analysis: 
The purpose of analysis is to apply supervised machine learning to analyze credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we were required to use the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, we used the combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we used two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

The summary describes the recommendation of model to use to predict credit card risk.

## Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

### Naive Random Oversampling
![date_search](https://github.com/Meghajain84/UFOs/blob/main/static/images/date_search.PNG)

para

### SMOTE Oversampling
![date_search](https://github.com/Meghajain84/UFOs/blob/main/static/images/date_search.PNG)

para

### Cluster Centroid Undersampling
![date_search](https://github.com/Meghajain84/UFOs/blob/main/static/images/date_search.PNG)

para

### SMOTEEN Combination (Over and Under) Sampling
![date_search](https://github.com/Meghajain84/UFOs/blob/main/static/images/date_search.PNG)

para

### Balanced Random Forest Classifier
![date_search](https://github.com/Meghajain84/UFOs/blob/main/static/images/date_search.PNG)

para

### Easy Ensemble AdaBoost Classifier
![date_search](https://github.com/Meghajain84/UFOs/blob/main/static/images/date_search.PNG)

para

## Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.