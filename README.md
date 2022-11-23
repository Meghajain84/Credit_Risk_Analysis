# Credit_Risk_Analysis

## Overview of the analysis: 
The purpose of analysis is to apply supervised machine learning to analyze credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we were required to use the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, we used the combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we used two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

The summary describes the recommendation of model to use to predict credit card risk.

## Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

### Naive Random Oversampling
![Naive_Random_Oversampling](https://github.com/Meghajain84/Credit_Risk_Analysis/blob/main/Naive_Random_Oversampling.PNG)

* <font color="blue"> Balanced Accuracy Score: 0.64 </font>
* <font color="blue"> Precision (High/Low risk): .01/1 </font>
* <font color="blue"> Recall (High/Low risk): .62/.65 </font>

<font color="blue"> Both balanced accuracy score and recall for high risk are not looking that great. </font>

### SMOTE Oversampling
![SMOTE_Oversampling](https://github.com/Meghajain84/Credit_Risk_Analysis/blob/main/SMOTE_Oversampling.PNG)

* <font color="blue"> Balanced Accuracy Score: 0.63 </font>
* <font color="blue"> Precision (High/Low risk): .01/1 </font>
* <font color="blue"> Recall (High/Low risk): .62/.64 </font>

<font color="blue"> Both balanced accuracy score and recall for high risk are not looking great. </font>

### Cluster Centroid Undersampling
![ClusterCentroids_Undersampling](https://github.com/Meghajain84/Credit_Risk_Analysis/blob/main/ClusterCentroids_Undersampling.PNG)

* <font color="blue"> Balanced Accuracy Score: 0.53 </font>
* <font color="blue"> Precision (High/Low risk): .01/1 </font>
* <font color="blue"> Recall (High/Low risk): .61/.45 </font>

<font color="blue"> Both balanced accuracy score and recall for high risk are not looking great. </font>

### SMOTEEN Combination (Over and Under) Sampling
![SMOTEEN](https://github.com/Meghajain84/Credit_Risk_Analysis/blob/main/SMOTEEN.PNG)

* <font color="blue"> Balanced Accuracy Score: 0.64 </font>
* <font color="blue"> Precision (High/Low risk): .01/1 </font>
* <font color="blue"> Recall (High/Low risk): .70/.57 </font>

<font color="blue"> Both balanced accuracy score and recall for high risk are not looking great. </font>

### Balanced Random Forest Classifier
![BalanceRandomForest](https://github.com/Meghajain84/Credit_Risk_Analysis/blob/main/BalanceRandomForest.PNG)

* <font color="blue"> Balanced Accuracy Score: 0.79 </font>
* <font color="blue"> Precision (High/Low risk): .04/1 </font>
* <font color="blue"> Recall (High/Low risk): .67/.91 </font>

<font color="blue"> Balanced accuracy score is slightly better than models above, but recall for high risk is still not looking great. </font>

### Easy Ensemble AdaBoost Classifier
![EasyEnsemble](https://github.com/Meghajain84/Credit_Risk_Analysis/blob/main/EasyEnsemble.PNG)

* <font color="blue"> Balanced Accuracy Score: 0.93 </font>
* <font color="blue"> Precision (High/Low risk): .07/1 </font>
* <font color="blue"> Recall (High/Low risk): .91/.94 </font>

<font color="blue"> Bothe balanced accuracy score and recall are looking good. </font>

## Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

Sensitivity is more important in our scenario. A test with high sensitivity means few false negatives, though there may be a high number of false positives. In this context, false positives are preferable to false negatives. It’s better to rule out false positive credit risks than to miss applicants who actually are at credit risk.

Comparing all the six model's results, we can clearly see that **Easy Ensemble AdaBoost Classifier model** has surpassed all other models.
Out of 87 (79+8) actual credit risk applications, it predicted 79 correctly. The recall value of 0.91 is way higher than other models as it is closest to 1. 
In addition, the balanced accuracy score of .93 is highest for this model when compared to other models.

