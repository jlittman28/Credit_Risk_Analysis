# Credit_Risk_Analysis

## Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. The client requested us to oversample the LendingClub dataset leveraging different techniques to train and evaluate models with unbalanced classes.

## Results

### Naive Random Oversampling
* Accuracy Score: 63.2%
* Precision High Risk: 1%
* Precision Low Risk: 100%
* Recall High Risk: 56%
* Recall Low Risk: 70%

![image](https://user-images.githubusercontent.com/85204128/136724003-27436c7c-d7fc-4171-aef1-1b44a91339bf.png)

![image](https://user-images.githubusercontent.com/85204128/136723992-286f0a10-3c85-4ba1-b835-345a1aef48c3.png)


### SMOTE Oversampling
* Accuracy Score: 63.9%
* Precision High Risk: 1%
* Precision Low Risk: 100%
* Recall High Risk: 67%
* Recall Low Risk: 61%

![image](https://user-images.githubusercontent.com/85204128/136725072-e98c0375-0cde-4182-b1ee-ae5c73df296b.png)

![image](https://user-images.githubusercontent.com/85204128/136725134-1de711fe-77f4-47fb-a2d8-57ea8a3a2433.png)

### Cluster Centroids Undersampling
* Accuracy Score: 51.8%
* Precision High Risk: 1%
* Precision Low Risk: 100%
* Recall High Risk: 57%
* Recall Low Risk: 46%

![image](https://user-images.githubusercontent.com/85204128/136725287-65b370ca-cc1b-4024-a591-bda559299779.png)

![image](https://user-images.githubusercontent.com/85204128/136725303-22f23e86-813d-4138-b04d-eb9bdc2e1dee.png)

### Combination (over and Under) Sampling
* Accuracy Score: 62.9%
* Precision High Risk: 1%
* Precision Low Risk: 100%
* Recall High Risk: 71%
* Recall Low Risk: 55%

![image](https://user-images.githubusercontent.com/85204128/136725426-f156c864-2993-4c7f-be92-0243a554f4e0.png)

![image](https://user-images.githubusercontent.com/85204128/136725438-b3588176-e308-406c-b3bc-e7a2fb84036b.png)

### Balance Random Forest Classifier
* Accuracy Score: 78.8%
* Precision High Risk: 4%
* Precision Low Risk: 100%
* Recall High Risk: 67%
* Recall Low Risk: 91%

![image](https://user-images.githubusercontent.com/85204128/136725500-67bda100-f04b-466b-9997-7dc39eba1c7d.png)

![image](https://user-images.githubusercontent.com/85204128/136725529-ec291656-1abe-47e6-91e1-71aa4ede6b34.png)

### Easy Ensemble AdaBoost Classifier
* Accuracy Score: 92.5%
* Precision High Risk: 7%
* Precision Low Risk: 100%
* Recall High Risk: 91%
* Recall Low Risk: 94%

![image](https://user-images.githubusercontent.com/85204128/136725620-6f15d0fe-274c-4db1-a8f9-850dd5678ecf.png)

![image](https://user-images.githubusercontent.com/85204128/136725607-7344633f-7e86-4cd7-8a81-cd8a67e0ff9e.png)


## Summary
The model provides the ability to detect the risk level of loans. With that we identified the models that were identified with the least amount of high risk loans that were undetected.

  1. Easy Ensemble (91%)
  2. SMOTE & Balance Random Forest Classifier (67%)

The next important statistic is the low recall risk rate
  1. Easy Ensemble (94%)
  2. Balance Random Forest Classifier (91%)
  3. NAIVE Random Oversampling (70%)

After reviewing the above statistics, we compared the overall accruacy score between all sample methodologies.

  1. Easy Ensemble (92.5%)
  2. Balance Random Forest Classifier (78.8%)
  3. SMOTE Oversampling (63.9%)

Based on the above , I would recommend the Easy Ensemble AdaBoost Classifier as it is the most statistically significant across all models.


