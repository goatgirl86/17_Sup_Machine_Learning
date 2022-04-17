# Credit Risk Analysis
## Relevant Folders and/or Files
-	Folder - Challenge
-	credit_risk_resampling.ipynb
-	credit_risk_ensemble.ipynb
-	LoanStats_2019Q1.csv

## Project Overview
### Purpose

The purpose of this challenge was to explore Supervised Machine Learning by helping Jill from “Fast Lending” predict credit card risk using oversampling, undersampling, and various supervised machine learning models.  

### Data Analyzed
-	LoanStats_2019Q1.csv (Credit card credit dataset from LendingClub, a peer-to-peer lending services company)

### Deliverables 
The deliverables for this assignment were:
-	Deliverable 1: Use Resampling Models to Predict Credit Risk 
-	Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk 
-	Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk ## Results

## Results
### Accuracy Scores
-	Naïve Random Over Sampler: 0.62
-	SMOTE Oversampling: 0.65
-	Cluster Centroids Undersampling:0.51
-	Combination Sampling (SMOTEENN): 0.65
-	Balanced Random Forest Classifier: 0.91
-	Easy Ensemble AdaBoost Classifier: 0.94

Easy Ensemble is the most accurate while Cluster Centroid is the least accurate. Lower accuracy scores indicate greater incidence of false positives and/or false negatives.  

### Precision Scores
-	Naïve Random Over Sampler: high=0.01, low=1.0
-	SMOTE Oversampling: high=0.01, low=1.0
-	Cluster Centroids Undersampling: high=0.01, low=1.0
-	Combination Sampling (SMOTEENN): high=0.01, low=1.0
-	Balanced Random Forest Classifier: high=0.04, low=1.0
-	Easy Ensemble AdaBoost Classifier: high=0.07, low=1.0

Easy Ensemble has the best overall precision of all models, but its “high risk” precision score is only marginally better than the other models (none of which are good). Lower precision scores indicate greater incidence false positives (predicted as positive but actually negative).

### Recall Scores
-	Naïve Random Over Sampler: high=0.60, low=0.65
-	SMOTE Oversampling: high=0.64, low=0.66
-	Cluster Centroids Undersampling: high=0.59, low=0.43
-	Combination Sampling (SMOTEENN): high=0.72, low=0.58
-	Balanced Random Forest Classifier: high=0.67, low=0.91
-	Easy Ensemble AdaBoost Classifier: high=0.91, low=0.94

Easy Ensemble has the best overall recall scores while Cluster Centroid has the worst. Lower recall (sensitivity) scores indicate greater incidence of false negatives (predicted as negative but actually positive). 


### Screenshots of Model Summaries

Screenshot 1: Naïve Random Over Sampler

![image](https://user-images.githubusercontent.com/92705556/163703895-6fa140f5-9e7d-4130-9350-e11e2de5e2bc.png)

Screenshot 2: SMOTE Oversampling

![image](https://user-images.githubusercontent.com/92705556/163703906-ba233e37-ac2a-4c33-ae8c-32834640dc5a.png)

Screenshot 3: Cluster Centroids Undersampling

![image](https://user-images.githubusercontent.com/92705556/163703921-ebb0bb88-c3ce-42fd-a251-8f68ddb6eb15.png)

Screenshot 4: Combination Sampling (SMOTEENN)

![image](https://user-images.githubusercontent.com/92705556/163703929-8cf7953f-86c5-423e-8ed7-9f1ebe56a7d0.png)

Screenshot 5: Balanced Random Forest Classifier

![image](https://user-images.githubusercontent.com/92705556/163703940-ac37124b-830b-4259-8b6f-2767cbf06220.png)

Screenshot 6: Easy Ensemble AdaBoost Classifier

![image](https://user-images.githubusercontent.com/92705556/163703950-f74f328b-aedf-4230-9bdf-1984f5da8b1c.png)

Screenshot 7: Feature Importances List (Balanced Random Forest Classifier)

![image](https://user-images.githubusercontent.com/92705556/163703961-0f742bd0-e0de-4ad8-bc8f-b3e106feb58a.png)


## Summary
### Overall Ranking of Assessed Models
Based on the results, this is how I would rank the assessed prediction models. 
1.	(Best) Easy Ensemble AdaBoost Classifier
2.	Balanced Forest Random Classifier
3.	SMOTEENN (Combination Sampling)
4.	SMOTE Oversampling
5.	Naïve Random Oversampling
6.	(Worst) Cluster Centroid Undersampling

### Conclusions
Despite the above rankings (including Easy Ensemble's high ranking on accuracy and recall), ALL models have low precision scores for “high risk” entries. As precision is a measure of the model’s ability to predict positive results correctly, ALL models are going to result in more false positives relative to true positives. That is, there will be more low risk entries predicted as high risk than actual high risk correctly predicted as high risk. While it is better to reject low-risk applicants than accept high-risk applications, if "Fast Lending" accepts any of these models, they jeopardize losing future interest income by rejecting good loan applicants. 

**As a result, before “Fast Lending” uses any of these models, I believe other machine learning prediction models should be assessed.**    
