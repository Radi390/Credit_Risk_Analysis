# Credit_Risk_Analysis
## Overview
This analysis is about Credit and risk. A dataset from LendingClub, a peer-to-peer lending services company, is used to decide each loan application classified as "Low-Risk" or "High-Risk." Like every Credit and Risk problem, the dataset contains unbalanced counts for each class, and it is crucial to sensitively find out High-Risk applications in the trade-off between precision and recall.
To fulfill the problem, I used "imbalanced-learn" and "scikit-learn" libraries to build and evaluate models utilizing resampling. Six different algorithms, include RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier, and EasyEnsembleClassifier, are used to predict credit risk and evaluate the performances of these models.

## procedure
This analysis starts by preprocessing data and transforming none numeric data to numeric data by format changing and encoding with "get_dummies."
After that, in the "credit_risk_resampling" notebook, two oversampling, an undersampling, and one model combination of both over and undersampling are used separately to resample the data. Then, the Logistic Regression model was applied to resampled data for each four resampling models. Finally, a balanced accuracy score, confusion matrix, and imbalanced classification report were used to evaluate the performance of each algorithm.
In the "credit_risk_ensemble" notebook 

## Results

- RandomOverSampler model delivers a balanced accuracy score of 0.64. The precision score for the low-risk class is 1.00, and the high-risk is 0.01. For the low-risk, recall score is 0.59, and 0.69 for the high-risk. The F1 score for the low-risk is 0.74 and is 0.02 for the high-risk.
![This is an image](/oversampling_model.jpg)

- SMOTE algorithm shows a balanced accuracy score of 0.66. The precision score for the low-risk class is 1.00, and the high-risk is 0.01. The recall score is 0.69 for the low-risk and 0.63 for the high-risk. The F1 score for the low-risk is 0.82 and is 0.02 for the high-risk.
![This is an image](/smote_model.jpg)

- Cluster Centroids model shows a balanced accuracy score of 0.54. The precision score for the low-risk class is 1.00, and the high-risk is 0.01. For the low-risk, recall score is 0.40, and 0.69 for the high-risk. The F1 score for the low-risk is 0.57 and is 0.01 for the high-risk.
![This is an image](/undersampling_model.jpg)

- SMOTEENN algorithm delivers a balanced accuracy score of 0.638. The precision score for the low-risk class is 1.00, and the high-risk is 0.01. For the low-risk, recall score is 0.57, and 0.70 for the high-risk. The F1 score for the low-risk is 0.73 and is 0.02 for the high-risk.
![This is an image](/smoteenn_model.jpg)

- The Balanced Random Forest Classifier method delivers a balanced accuracy score of 0.788. The precision score for the low-risk class is 1.00, and the high-risk is 0.03. The recall score is 0.87 for the low-risk and 0.70 for the high-risk. The F1 score for the low-risk is 0.93 and is 0.06 for the high-risk.
![This is an image](/randomforest_model.jpg)

- Finally, the Easy Ensemble Classifier made a balanced accuracy score of 0.93. The precision score for the low-risk class is 1.00, and the high-risk is 0.09. For the low-risk, recall score is 0.94, and 0.92 for the high-risk. The F1 score for the low-risk is 0.97 and is 0.16 for the high-risk.
![This is an image](/eec_model.jpg)


## Summary

### Results

![This is an image](/Results.jpg)



### Conclusion
In conclusion, Easy Ensemble Classifier performs better than others by far between these six models. Its accuracy score is 0.93 and delivers sensitivity of 0.92 and 0.94 for High-risk and Low-risk. Furthermore, precision for High-risk is 0.09, which is three times better than Balanced Random Forest Classifier and nine times better than other models. After this analysis, we could determine that between these six algorithms, the Easy Ensemble Classifier is a better choice.
