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

## ClusterCentroids model

<img width="398" alt="Screen Shot 2021-09-11 at 2 01 08 PM" src="https://user-images.githubusercontent.com/39747985/132957037-59662d2d-fdf7-48bf-b40f-49b86db25169.png">

<img width="741" alt="Screen Shot 2021-09-11 at 2 01 16 PM" src="https://user-images.githubusercontent.com/39747985/132957044-ab36dac5-5382-48bc-b1e2-963a3ff6a1a8.png">

## Summary
