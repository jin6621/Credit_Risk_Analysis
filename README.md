# Credit_Risk_Analysis

Reference website:

[BalancedRandomForestClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.BalancedRandomForestClassifier.html)

[EasyEnsembleClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.EasyEnsembleClassifier.html)

---

### 1. Overview of the analysis: Explain the purpose of this analysis. 

The purpose of this analysis is to demonstrate skills in data preparation, statistical reasoning, and machine learning. With imbalanced-learn and scikit-learn libraries to build models using resampling, we will employ different techniques to train and evaluate models with unbalanced classes.

### 2. Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

- Naive Random Oversampling:
 - Accuracy Score: 62.1%
 - High Risk Precision: 1%
 - High Risk Recall: 64%

![1.png](resources/1.png)
 
 
- SMOTE Oversampling
 - Accuracy Score: 65.6%
 - High Risk Precision: 1%
 - High Risk Recall: 63%

![2.png](resources/2.png)

- Undersampling
 - Accuracy Score: 44.97%
 - High Risk Precision: 1%
 - High Risk Recall: 61%

![3.png](resources/3.png)

- Combination (Over and Under) Sampling
 - Accuracy Score: 55.37%
 - High Risk Precision: 1%
 - High Risk Recall: 71%

![4.png](resources/4.png)

- Balanced Random Forest Classifier
 - Accuracy Score: 78.78%
 - High Risk Precision: 4%
 - High Risk Recall: 67%

![5.png](resources/5.png)

- Easy Ensemble AdaBoost Classifier
 - Accuracy Score: 92.55%
 - High Risk Precision: 7%
 - High Risk Recall: 91%

![6.png](resources/6.png)


### 3. Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

In my opinion, out of the six models, Easy Ensemble AdaBoost Classifier was the one that out-performed the other models with high risk recall of 91%. (Which in this case, we care about recall very much because we want the model to have high accuracy of predicting high_risks. (Out of 87 actual high_risks, the model is able to capture 79). However, too many of the low risks were incorrectly detected as high risks. This will potentially cause a lot of unnecessary trouble to the lender. 