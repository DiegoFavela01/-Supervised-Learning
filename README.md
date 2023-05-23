# Supervised-Learning
Challenge 12 - University of Berkeley Financial Technology Boot Camp
## Credit Risk Analysis

### Overview of the Analysis
The analysis aimed to compare the performance of two machine learning models used to classify loans as either 'healthy' or 'high risk'.
The dataset used for modeling comprised a total of 77,536 observations, each with 7 features and the target variable. The data exhibited a significant class imbalance, with only 3.22% of observations labeled as 'high risk'.
The dataset was divided into training and test sets, with 75% used for training purposes.
Both models employed logistic regression, utilizing Scikit-learn's LogisticRegression model. The first model utilized the original data, while the second model employed resampling through imblearn's RandomOverSampler.
The oversampled data resulted in a balanced dataset, containing 56,244 observations for both 'healthy' and 'high risk' loans.
### Results
| Machine Learning Model 1 (original data) | Machine Learning Model 2 (resampled data) |
|------------------------------------------|------------------------------------------|
| **Average metrics**                      | **Average metrics**                     |
| Balanced accuracy: 95.3%                 | Balanced accuracy: 99.5%                |
| Average precision: 99%                   | Average precision: 1.00                 |
| Average recall: 99%                      | Average recall: 0.99                    |
| Average f1: 99%                          | Average f1: 0.99                        |
|                                          |                                         |
| **'High risk' loan metrics**             | **'High risk' loan metrics**            |
| Precision: 0.85                          | Precision: 0.85                         |
| Recall: 0.91                             | Recall: 1.00                            |
| F1: 0.88                                 | F1: 0.92                                |
|                                          |                                         |
| **'Healthy' loan metrics**               | **'Healthy' loan metrics**              |
| Precision: 1.00                          | Precision: 1.00                         |
| Recall: 1.00                             | Recall: 0.99                            |
| F1: 1.00                                 | F1: 1.00                                |


### Summary
There is a noticeable difference in performance between the two models.
The overall balanced accuracy of the resampled data was 99.5%, significantly higher than the 95.3% achieved by the original data model.
Regarding the 'healthy' class, both models exhibited comparable performance, with the original data model showing a slightly better recall score.
However, for the 'high risk' class, the resampled data model displayed improved recall and f1 scores.
Considering the importance of correctly classifying the 'high risk' class, I recommend utilizing the second model due to its enhanced scoring, particularly in relation to the 'high risk' class.
