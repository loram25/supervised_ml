# Supervised Machine Learning
## Module 17

The goal of supervised machine learning in this module is to predict credit risk in an imbalanced dataset, where there are significantly more low risk loan than high risk. Our goal is find the model that is best for our application.  Because of the financial consequences of loans defaulting, the model priority is identifying high risk loans. Therefore the analysis below will focus of high risk statistics.

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
