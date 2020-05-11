# Supervised Machine Learning
## Module 17

The goal of supervised machine learning in this module is to predict credit risk in an imbalanced dataset, where there are significantly more low risk loan than high risk. Our goal is find the model that is best for our application.  Because of the financial consequences of loans defaulting, the model priority is identifying high risk loans. Therefore the analysis below will focus of high risk statistics.

In general, the first 4 logistic models had very low precision scores. This value means the model does not have a high probability of identifying a high risk loan when it predicts one. But here of the first 4 models had a strong sensitivity (recall). This value means the model correctly captured 60% - 71% of the high risk loans in the testing set. Using the balanced accuracy score, these 4 models performed comparably. The cluster-centroid undersmapling performed the worst because of the extreme class imbalance. Of these 4 models, I would choose SMOTEEN combination sampling with Logistic regression due to highest recall score. 

A model that captures the highest amount of real high risk loans will best protect the company from the financial loss through defaulting. Although the low precision likely means more post-processing work by staff to develop a standard for what to do with the thousands of misclassified loans. This work is likely time-consuming and costly in other ways. This fact might shift a company's focus to a better balance between precision and recall.

Which leads us to the final 2 model, using Random Forest and Easy Ensemble. They both provide insight into an improved balances.
The Random Forest prioritizes precision, correctly identifying a high risk loan 72% of the time. An incredible improvement over 1% in the logistic models. The sensitivity is 36% (much less than the 65% of the logistic) but the accuracy is 0.678, which is comparable to the other models. These scores represent a shift to minimizing the staff follow-up work and increasing the exposure to financial risk through defaults.

The Easy Ensemble is the best performing model, with an accuracy score of 0.929. The precision is 14%, much better than the 1% of logistic, which represents over 10x reduction of follow-up work needed on loans flagged for high-risk. It also captures 89% of the true high-risk loans, which makes the follow-up still needed more worthwhile!

My recommendation is to use the Easy Ensemble AdaBoost Classifier. It provides the best accuracy and best balance between capturing highest percentage of high risk loans (thus improving protection from loan defaults) and the amount of work parsing through incorrectly flagged (thus improving the work efficiency of the group responsible for flagging loans). I will note this model is the most computationally intensive, by a large margin. I re-ran the model with 10 estimators, instead of 100, and the computation time decreased dramatically and the model scores are identical. Therefore I would suggest decrease n_estimators as well.

NOTE: Precision and Recall values both reflect High Risk Loans

### Random Oversampling
Precision: 0.01 
Recall: 0.66 
Accuracy: 0.648

### SMOTE Oversampling
Precision: 0.01
Recall: 0.60
Accuracy: 0.627

### Cluster Centroid Undersampling
Precision: 0.01
Recall: 0.63
Accuracy: 0.5215

### SMOTEEN Combination Sampling
Precision: 0.01
Recall: 0.71
Accuracy: 0.637

### Balanced Random Forest w/ Random Oversampling
Precision: 0.72
Recall: 0.36
Accuracy: 0.678

### Easy Ensemble AdaBoost Classifier
Precision: 0.14
Recall: 0.89
Accuracy: 0.929
