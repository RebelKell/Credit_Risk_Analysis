# Credit Risk Analysis

## Overview
Throughout this analysis we seek to better understand credit card risk by creating multiple models that predict credit risk. The hope is that our model will work effectively and efficiently in identifying individuals who are best to extend credit to and those that may incur more risk.

## Results
For our analysis we leveraged six  machine learning models to over sample, under sample and combination over- and under-sample our data to determine the effectiveness of each in predicting credit risk. Each method had different results, which are shown below: 

- <strong>Oversampling using Naive Random Oversampling</strong><br />
   - Balanced Accuracy Score: 66.29%
   - Precision: 1% for high-risk and 100% for low-risk. 
   - Recall Scores: 64% for high-risk and 68% for low-risk.
   <br /><br />

   ![Naive Random Oversampling](/Images/NaiveRandomOversampling.png)

- <strong>Oversampling using SMOTE</strong><br />
   - Balanced Accuracy Score: 63.94%
   Precision: 1% for high-risk and 100% for low-risk. 
   - Recall Scores: 54% for high-risk and 74% for low-risk.
   <br /><br />

   ![SMOTE](/Images/SMOTE.png)
    <br /><br />

- <strong>Undersampling using Cluster Centroids</strong><br />
   - Balanced Accuracy Score: 53.18%
   Precision: 1% for high-risk and 99% for low-risk. 
   - Recall Scores: 53% for high-risk and 53% for low-risk.
   <br /><br />

   ![Cluster Centroids](/Images/ClusterCentroids.png)
    <br /><br />
   
- <strong>Combination over- and under-sampling using SMOTEENN</strong><br />
   - Balanced Accuracy Score: 64.68%
   Precision: 1% for high-risk and 99% for low-risk. 
   - Recall Scores: 73% for high-risk and 56% for low-risk.
   <br /><br />

    ![SMOTEENN](/Images/SMOTEEN.png)
   <br /><br />


- <strong>Ensemble learning using Balanced Random Forest Classifier</strong><br />
  - Balanced Accuracy Score: 77.87%
   - Precision: 7% for high-risk and 100% for low-risk. 
   - Recall Scores: 73% for high-risk and 56% for low-risk.
   <br /><br />

    ![BRFC](/Images/BRFC.png)
   <br /><br />


- <strong>Ensemble learning using Easy Ensemble AdaBoost classifier</strong><br />
   - Balanced Accuracy Score: 92.93%
   - Precision: 7% for high-risk and 100% for low-risk. 
   - Recall Scores: 92% for high-risk and 93% for low-risk.
   <br /><br />

    ![EEC](/Images/EEC.png)
   <br /><br />



## Summary
In assessing credit risk, we are more interested in precision more so than sensitivity (aka recall) because while sensitivity will cast a wide net and catch many potential credit risks, it also may be too aggressive leadiung to more rejected credit than we want. We really only want to highlight credit applications that are truly potential credit risks so a focus on precision is more important here.

Based on these results we can conclude that there are some clear low-performering models and a couple high-performing models.

The logisitc regression-based models, in general, perfomed the worst, all with accuracy scores below 70%. Their precision scores for both low and high-risk borrowers were the same (100% and 1% respectively) across all models while their sensitivity scores varied, but never got over 74%. 

The Ensemble Classifiers on the other hand proved to be more reliable with the Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier both showing an increased precision score (at 7%) for high risk borrowers and an average sensitivity of 93%.Compare this to the previous model's 1% precision score and it's clear that these two are doing better at zeroing in on high-risk borrowers, making it easier to detect them. 

The accuracy scores of the Ensemble Classifiers are also higher with the Easy Ensemble AdaBoost Classifier showing 92.93%. However, the low f1 scores are concerning and illustrate that there is tension between the precision and sensitivity of the model.

Overall, most of the models do not do a great job at prediciting credit risk, but the Easy Ensemble AdaBoost Classifier does the best and would be recommended out of these models.


