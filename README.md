# Credit_Risk_Analysis
## Overview of the loan prediction risk analysis

The purpose of this analysis is to use resampling to train and evaluate models with unbalanced classes, and evaluate the performance of these models to give recommendation on predicting credit card risk. We will use imbalanced-learn and scikit-learn libraries to build and evaluate the performance of 6 different machine learning models. The credit card credit dataset used is from LendingClub.

## Results
There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models 
### Naive Random Oversampling: 
- balanced accuracy score 0.6463970560994359
- precision 0.01, low for High-risk loans, high for Low-risk loans
- recall 0.71/0.58

![img1](https://github.com/siqiou/Credit_Risk_Analysis/blob/6616e8d81f4e9ce277683b0148be4442c1021bf3/images/Naive%20Random%20Oversampling.png)
### SMOTE Oversampling: 
- balanced accuracy score 0.6586230769943224
- precision 0.01, low for High-risk loans, high for Low-risk loans
- recall 0.63/0.68

![img2](https://github.com/siqiou/Credit_Risk_Analysis/blob/6616e8d81f4e9ce277683b0148be4442c1021bf3/images/SMOTE%20Oversampling.png)
### Undersampling: 
- balanced accuracy score 0.5442369453268994 
- precision 0.01, low for High-risk loans, high for Low-risk loans
- recall 0.69/0.40

![img3](https://github.com/siqiou/Credit_Risk_Analysis/blob/6616e8d81f4e9ce277683b0148be4442c1021bf3/images/Undersampling.png)
### Combination (Over and Under) Sampling: 
- balanced accuracy score 0.6480442302883235
- precision 0.01
- recall 0.72/0.57

![img4](https://github.com/siqiou/Credit_Risk_Analysis/blob/6616e8d81f4e9ce277683b0148be4442c1021bf3/images/Comnbination%20Sampling.png)
### Balanced Random Forest Classifier: 
- balanced accuracy score 0.7844011748069183
- precision 0.03
- recall 0.68/0.89

![img5](https://github.com/siqiou/Credit_Risk_Analysis/blob/6616e8d81f4e9ce277683b0148be4442c1021bf3/images/Balanced.png)
### Easy Ensemble AdaBoost Classifier: 
- balanced accuracy score 0.925427358175101
- precision 0.07
- recall 0.91/0.94

![img6](https://github.com/siqiou/Credit_Risk_Analysis/blob/6616e8d81f4e9ce277683b0148be4442c1021bf3/images/EaseEnsember.png)


## Summary
The accuracy score are very similar in the first 4 models, indicating they are able to classify 54-65% of the transactions. the highest accuracy score is found in the Easy Ensemble AdaBoost Classifier model, with 92% accuracy. However, it fails to detect the rest fraudulent data.

By looking at the precision values to measure how reliable a positive classification is, the first 4 models' precision values are 0.01, which are the least reliable. The most reliable model would be the last one, Easy Ensemble AdaBoost Classifier.

The recall score is more important in this case, the model with highest sensitivity means few false negatives, since we don't want to miss any fraudulent transactions, the last model - Easy Ensemble AdaBoost Classifier seems to be the best performer.

In summary, it is suggest to use the Easy Ensemble AdaBoost Classifier as it has the highest accuracy, precision, and recall score.
