# Credit Rish Analysis Using Supervised Machine Learning (Module 17 Challenge)

## Overview
To determine if these machine learning models could accurately predict credit risk by analyzing a credit card dataset, this study evaluated their performance.

## Results

Oversampling using SMOTE and naive random oversampling is followed by undersampling using ClusterTest. 

#### Naive Random Oversampling Using RandomOversampler

- A balanced accuracy score of 64% is achieved. 
- In the high_risk segment, the precision is 1% and the sensitivity is 61%. 
- With a precision score of 100% and a sensitivity score of 68%, low_risk scores perfectly. 
- With a precision score of 99%, and a sensitivity score of 68%, overall the performance is excellent. 

#### SMOTE Oversampling

- An accuracy score of 66% is considered balanced.
- With a sensitivity score of 67%, high_risk has a precision score of 1%.
- With a sensitivity score of 66%, low_risk has 100% precision.
- This study has a precision rating of 99% is achieved with a sensitivity of 66%.

#### Undersampling Using ClusterCentroids

- It is 51% accurate on a balanced basis.
- For high_risk, the precision and sensitivity scores are 1% and 59% respectively.
- Low_risk precision score is 100% and its sensitivity score is 43%.
- In general, the precision score is 99%, while the sensitivity score is 44%.

### SMOTEENN Algorithm to Predict Credit Risk
In order to determine whether the later SMOTEENN algorithm works better than the earlier resampling models, I applied a combinatorial approach of over-and under-sampling.

#### Combination (Over and Under) Sampling Using SMOTEENN

- 64% is the balanced basis.
- High_risk has a precision score of 1% and a sensitivity score of 70%.
- Low_risk has a precision score of 100% and a sensitivity score of 57%.
- The precision score overall is 99%, while the sensitivity score is 57%.

### Ensemble Classifiers to Predict Credit Risk
Lastly, I trained and tested two ensemble classifiers to predict credit risk, BalancedRandomForestClassifier and EasyEnsembleClassifier.

#### Balanced Random Forest Classifier

- An accurate balance score of 79% is achieved.
- In the high_risk group, precision is 4%, sensitivity is 67%.
- Low_risk has a precision of 100% and a sensitivity of 91%.
- As a whole, the precision score is 99%, sensitivity is 91%. 

#### Easy Ensemble AdaBoost Classifier

- 93% is the balanced accuracy score.
- High_risk score has a precision of 7% and a sensitivity of 91%.
- Low_risk score has a precision of 100% and a sensitivity of 94%.
- There is an overall precision score of 99% and a sensitivity score of 94%.

## Summary
With the exception of undersampling, where the balanced accuracy score was 51%, the first three resampling models and the combination sampling model all had balanced accuracy scores in the range of 64-66%. As compared to Ensemble Classifier whose balanced accuracy score was 79% and Easy Ensemble Classifier's balanced accuracy score of 93%. To find models that assess credit risk, we should specifically focus on the high_risk variable. Our goal is to achieve high precision scores as precision indicates how reliable a positive classification is, and we also want to achieve high sensitivity scores since sensitivity measures how many loans are correctly classified as high risk. In terms of precision scores, each of the three resampling models and the combination sampling model achieved a precision score of 1%. Only the SMOTEENN model received a sensitivity score higher than 70%, with the scores ranging from 59-67%. Most notably, the EasyEnsembleClassifier scored 7% precision and 91% sensitivity, most impressive among the ensemble classifiers. With 100% precision and 94% sensitivity, EasyEnsembleClassifier also had the highest score for low_risk. Due to its high balanced accuracy score, high precision score, and high sensitivty score among all the models, I would recommend using the EasyEnsembleClassifier.