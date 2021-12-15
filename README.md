# Credit_Risk_Supervised
Supervised Machine Learning

### Initial Analysis:
* This analysis with supervised learning algorithms is used to clarify whether a lending company could use a classification algorithm to identify low-risk loans (borrowers with good credit) and high-risk loans (borrowers with bad credit).

* In the cleaned dataset, there are 347 high-risk loans  and 68,470 low-risk loans. Rought 0.5% of our dataset is high risk loan data, this is an imbalanced dataset. 

* The following algorithms of RandomOverSampler, SMOTE, Undersampling (Cluster Centroids Algorithm), and Combination (SMOTEEN Algorithm) are used to determine the optimal resampling algorithm.

### Resampling Algorithm Comparison: 
#### SMOTE Oversampling:
Balanced Accuracy Score: 55.6%

##### High risk loans (Bad Credit):
* Precision score: 0.01
* Recall score: 0.39
  
* Overall F1 score: 0.83

#### Undersampling (Cluster Centroids Algorithm):
Balanced Accuracy Score: 52.3%

##### High risk loans (Bad Credit):
* Precision score: 0.01
* Recall score: 0.09
  
* Overall F1 score: 0.97

#### Combination (SMOTEEN Algorithm):
Balanced Accuracy Score: 59.4%

##### High risk loans (Bad Credit):
* Precision score: 0.01
* Recall (Sensitivity) score: 0.59
  
* Overall F1 score: 0.75


### Ensemble Algorithm Comparison: 
#### Balanced Random Forest:
##### High risk loans (Bad Credit):
* Precision score: 0.03
* Recall score: 0.65
  
* Accuracy score: 76.5%

#### Easy Ensemble Classifier:
* Precision score: 0.08
* Recall score: 0.90
  
* Accuracy score: 91.8%

#### XGB Classifier:
Precision score: 0.95
* Recall score: 0.38
* 
* Accuracy score: 69.2%

### Analysis of model performance and final recommendation:
The best resampling algorithm would be the combination of over and under(SMOTEEN) because it had the highest recall score for the high risk group, and they all had low precision. 

The best ensemble algorithm is the EasyEnsembleClassifier because it has a relatively high recall and precision. In a severly unbalanced dataset we are expecting a low precision. We don't want a model as strict as XGBClassifier because we prefer a more sensitive model when it comes to credit risk.