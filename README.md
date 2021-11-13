## Overview 
The purpose of this project was to use Python and SciKit-Learn to build and evaluate several machine learning models to predict credit risk with unbalanced classes. Using the credit card credit dataset from LendingClub, the data was oversampled using the RandomOverSampler and SMOTE algorithms, and undersampled using the ClusterCentroids algorithm. Then, a combinatorial approach of over- and undersampling using the SMOTEENN algorithm was used. Next, the two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, were compared to predict credit risk


## Results 

The following list describes the balanced accuracy score and the precision and recall scores for the high risk case of all six machine learning models built in this project 

**RandomOverSampler:** 
The balanced accuracy score is 0.64, precision 0.01, and recall 0.66 
<img width="464" alt="Screen Shot 2021-11-13 at 4 29 19 PM" src="https://user-images.githubusercontent.com/85901073/141660017-817ed7c7-32b8-425d-a6de-e305fc51c689.png">

**SMOTE Ovesampling:**
The balanced accuracy score is 0.65, precision 0.01, and recall 0.61
<img width="462" alt="Screen Shot 2021-11-13 at 4 52 53 PM" src="https://user-images.githubusercontent.com/85901073/141660052-d3a45522-77fc-43b3-b99e-175aaa701cc4.png">

**ClusterCentroids:**
The balanced accuracy score is 0.54, precision 0.01, and recall 0.69
<img width="455" alt="Screen Shot 2021-11-13 at 4 54 35 PM" src="https://user-images.githubusercontent.com/85901073/141660097-c2bc7ec7-96db-47cf-a0db-1f74a1aec904.png">

**SMOTEENN:**
The balanced accuracy score is 0.64, precision 0.01, and recall 0.71
<img width="457" alt="Screen Shot 2021-11-13 at 4 57 00 PM" src="https://user-images.githubusercontent.com/85901073/141660148-117c85af-edb2-4ebf-bcc3-5ff1fc80c8ca.png">

**RandomForestClassifier:**
The balanced accuracy score is 0.64, precision 0.71, and recall 0.21
<img width="710" alt="Screen Shot 2021-11-13 at 5 04 21 PM" src="https://user-images.githubusercontent.com/85901073/141660301-03ebe79c-b299-4a3b-ad42-55c71af166dd.png">

**EasyEnsembleClassifier:**
The balanced accuracy score is 0.87, precision 0.07, and recall 0.80
<img width="704" alt="Screen Shot 2021-11-13 at 5 02 36 PM" src="https://user-images.githubusercontent.com/85901073/141660257-cf169b32-7141-4c58-8a1a-d3757b3eb654.png">


## Summary 
Given that the classes low risk and high risk were unbalanced, despite re-balancing techniques being applied, all of the models were better at predicting the low risk cases better than the high risk cases given that high risk occurs less in the dataset. Of all the models, the precision for the high risk cases was highest in the random forest classifier with a precision of 0.71 whereas all the other models were below 0.10. The accuracy score for five out of six models are around the same except for the easy ensemble classifier which has a balanced accuracy score of 0.87 and is the highest out of all the models. However, precision in this case is more significant evaluation metric to the problem being address (flagging high credit risk). The random forest classifier performed the best in this regard although the model would not be incredibly effective since it only catches approximately 71% of high risk cases. 
