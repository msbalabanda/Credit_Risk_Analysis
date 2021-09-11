# Credit_Risk_Analysis

## Overview of the analysis
The purpose of this analysis is to use the unbalanced classification method to predict credit card risk. We use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

The procedure involves:-
* Oversampling the data using the RandomOverSampler and SMOTE algorithms.
* Undersampling the data using the ClusterCentroids algorithm.
* Then, we use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm
* Lastly, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk

## Results

### Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports

## Naive Random Oversampler Model

<img width="552" alt="Screen Shot 2021-09-11 at 2 04 21 PM" src="https://user-images.githubusercontent.com/39747985/132957128-f9f37968-5ea7-4b4e-b8f2-dc055c8679e0.png">


<img width="742" alt="Screen Shot 2021-09-11 at 12 19 27 PM" src="https://user-images.githubusercontent.com/39747985/132954454-a942149f-d2ec-46eb-a4c9-ff9ce6b49b28.png">

The accuracy score of this model is approximately 65%.
The precision for the high risk clients is 1% with a sensitivity rate of 61% and an F1 score of 2%
Whereas the precision for the low risk clients is 100% with a sensitivity rate of 68% and an F1 score of 81%

## SMOTE Model
<img width="455" alt="Screen Shot 2021-09-11 at 2 02 57 PM" src="https://user-images.githubusercontent.com/39747985/132957087-80717dfc-84c0-44a4-9b4b-7d8ef3c23fd7.png">

<img width="772" alt="Screen Shot 2021-09-11 at 1 53 47 PM" src="https://user-images.githubusercontent.com/39747985/132956858-73640b1d-bcb5-4e12-94b4-54ee1bb78fac.png">

Similar to the Naive Random Oversampler Model
The accuracy score of this model is approximately 62%.
The precision for the high risk clients is 1% with a sensitivity rate of 61% and an F1 score of 2%
Whereas the precision for the low risk clients is 100% with a sensitivity rate of 64% and an F1 score of 78%

## ClusterCentroids Model

<img width="398" alt="Screen Shot 2021-09-11 at 2 01 08 PM" src="https://user-images.githubusercontent.com/39747985/132957037-59662d2d-fdf7-48bf-b40f-49b86db25169.png">

<img width="741" alt="Screen Shot 2021-09-11 at 2 01 16 PM" src="https://user-images.githubusercontent.com/39747985/132957044-ab36dac5-5382-48bc-b1e2-963a3ff6a1a8.png">

In this model the accuracy score of 52% is lower than the previous models.
The precision for the high risk clients is 1% with a sensitivity rate of 61% and an F1 score of 1%
Whereas the precision for the low risk clients is 100% with a sensitivity rate of 64% and an F1 score of 78%

## SMOTEENN Model

<img width="368" alt="Screen Shot 2021-09-11 at 2 16 22 PM" src="https://user-images.githubusercontent.com/39747985/132957397-f5d8ddc2-4429-434f-8ee9-d82471d18a83.png">

<img width="763" alt="Screen Shot 2021-09-11 at 2 16 30 PM" src="https://user-images.githubusercontent.com/39747985/132957420-6c3a463d-5118-47ef-a487-d4f31959ff05.png">

In this model the accuracy score of 62%.
The precision for the high risk clients is 1% with a sensitivity rate of 69% and an F1 score of 2%
Whereas the precision for the low risk clients is 100% with a sensitivity rate of 44% and an F1 70%

## BalancedRandomForestClassifier model

<img width="409" alt="Screen Shot 2021-09-11 at 2 22 58 PM" src="https://user-images.githubusercontent.com/39747985/132957578-9ec37022-c492-4c03-8b62-3d0160d7d6f4.png">

<img width="781" alt="Screen Shot 2021-09-11 at 2 23 18 PM" src="https://user-images.githubusercontent.com/39747985/132957586-4627949f-7fb2-4751-a4eb-25bce013265f.png">## Summary

Cmpared to the other models the balanced accuracy score improved to about 79%.
The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion and F1 score of 95%.

## EasyEnsembleClassifier model

<img width="373" alt="Screen Shot 2021-09-11 at 2 27 17 PM" src="https://user-images.githubusercontent.com/39747985/132957710-f754669b-3044-4bcc-8638-fc8e4f33a969.png">

<img width="749" alt="Screen Shot 2021-09-11 at 2 27 25 PM" src="https://user-images.githubusercontent.com/39747985/132957726-646b3dd4-be4d-4b59-8dd4-35f58640fe4f.png">

Lastly in this model the balanced accuracy score is high to about 93%.
The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion and an F1 score of 97%

## Summary

Considering the precision score of all these models, we can conclude that none of these models are good predicors in determining if credit risk is high becasue the precision scores range from 1%-7%. However we can note that the Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 93% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit analysis strategy and limit opportunities to offer credit to credible clients.
Therefore I would not recommend the bank to use any of these models to predict credit risk.
