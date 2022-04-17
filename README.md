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
-	Naïve Random Over Sampler: high-0.01, low-1.0
-	SMOTE Oversampling: high-0.01, low-1.0
-	Cluster Centroids Undersampling: high-0.01, low-1.0
-	Combination Sampling (SMOTEENN): high-0.01, low
-	Balanced Random Forest Classifier: high-0.04, low-1.0
-	Easy Ensemble AdaBoost Classifier: high-0.07, low-1.0

Easy Ensemble has the best overall precision of all models, but its “high risk” precision score is only marginally better than the other models (none of which are good). Lower precision scores indicate greater incidence false positives.  

### Recall Scores
-	Naïve Random Over Sampler: high-0.60, low-0.65
-	SMOTE Oversampling: high-0.64, low-0.66
-	Cluster Centroids Undersampling: high-0.59, low-0.43
-	Combination Sampling (SMOTEENN): high-0.72, low-0.58
-	Balanced Random Forest Classifier: high-0.67, low-0.91
-	Easy Ensemble AdaBoost Classifier: high-0.91, low-0.94

Easy Ensemble has the best overall recall scores while Cluster Centroid has the worst. Lower recall (sensitivity) scores indicate greater incidence of false negatives.  

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

**As a result, before “Fast Lending” uses any of these models, I believe other machine learning prediction models need to be assessed.**    
