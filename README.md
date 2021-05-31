# Credit_Risk_Analysis

## Overview
There six machines learning models are built in the project to predict credit risk. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we will use imbalanced-learn and scikit-learn libraries to train and evaluate models with unbalanced classes. Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, here are we will apply below:

1. RandomOverSampler (oversampling)
2. SMOTE (oversampling)
3. ClusterCentroids (undersampling)
4. SMOTEENN (over- and undersampling)
5. BalancedRandomForestClassifier (ensemble learning)
6. EasyEnsembleClassifier (ensemble learning)


## Results

**1. RandomOverSampler (oversampling)**

* Balanced accuracy scores is 66%
* Precision and sensitivity (recall) score of predicting high risk is 1% and 66%.
* Precision and sensitivity (recall) score of predicting LOW risk is 100% and 67%.

![random_oversampling_result](Resources/random_oversampling_result.PNG)

**2. SMOTE (oversampling)**

* Balanced accuracy scores is 63%
* Precision and sensitivity (recall) score of predicting high risk is 1% and 62%.
* Precision and sensitivity (recall) score of predicting LOW risk is 100% and 64%.

![SMOTE_Oversampling](Resources/SMOTE_Oversampling_result.PNG)

**3. ClusterCentroids (undersampling)**

* Balanced accuracy scores is 53%
* Precision and sensitivity (recall) score of predicting high risk is 1% and 61%.
* Precision and sensitivity (recall) score of predicting LOW risk is 100% and 45%.

![ClusterCentroids_undersampling_result](Resources/ClusterCentroids_undersampling_result.PNG)

**4. SMOTEENN (over- and undersamplin)**

* Balanced accuracy scores is 62%
* Precision and sensitivity (recall) score of predicting high risk is 1% and 70%.
* Precision and sensitivity (recall) score of predicting LOW risk is 100% and 54%.

![SMOTEENN_over_and_undersampling](Resources/SMOTEENN_over_and_undersampling.PNG)

**5. BalancedRandomForestClassifier (ensemble learning)**

* Balanced accuracy scores is 79%
* Precision and sensitivity (recall) score of predicting high risk is 4% and 67%.
* Precision and sensitivity (recall) score of predicting LOW risk is 100% and 91%.

![balanced_random_forest_classifier_result](Resources/balanced_random_forest_classifier_result.PNG)

**6. EasyEnsembleClassifier (ensemble learning)**

* Balanced accuracy scores is 93%
* Precision and sensitivity (recall) score of predicting high risk is 7% and 91%.
* Precision and sensitivity (recall) score of predicting LOW risk is 100% and 94%.

![easy_ensembel_AdaBoost_classifier_result](Resources/easy_ensembel_AdaBoost_classifier_result.PNG)


## Summary
1. Accurancy:

   Model of Easy Ensemble AdaBoost Classifier provides the highest accurancy,93%, among six models.

![accurancy_resample](Resources/accurancy_resample.PNG)

![accurancy_ensemble](Resources/accurancy_ensemble.PNG)


2. Precision score

   Model of Easy Ensemble AdaBoost Classifier provides the highest precision, 7%, among six models.    

![precision_resample](Resources/precision_resample.PNG)

![precision_ensemble](Resources/precision_ensemble.PNG)
   

3. Recall(Sensitivity) score

   Model of Easy Ensemble AdaBoost Classifier provides the highest precision, 91%, among six models.

![recall_resample](Resources/recall_resample.PNG)

![recall_ensemble](Resources/recall_ensemble.PNG)


4. Recommend

   In my option, I do not think that there is a model justify the risk and credit evaluation. The data given is much more low risk than high risk data. In order to better train the model, we applied six different machines learning models to either resampling or ensembling the train data. As the result, all six models are good at predicting low risk which 100 score on precision, which is a sign that the six models might be overfitting on low risk. 

   In real world, the models might lead us to make mistakes. It will just make us lose opportunity to make profits if we turn down to clients who are predicted as high risk but actually low risk. However, we will lose money if we loan to clients who are predicted as low risk but actually high risk. 

   Anyway, if we must have to choose a model to apply prediction for loan, I will pick EasyEnsembleClassifier model, since its recall (Sensitivity score) is the highest ,91%, among six models. That means the model is the most correctly recognize people who are high risk.

   