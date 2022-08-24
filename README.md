# Breast Cancer Analysis
Breast Cancer Analysis - Decision Trees, Logistic Regression &amp; KNN

## Introduction
Every year, breast cancer affects two million women. Breast cancer should be treated as soon as it is discovered to increase survival rates. Recurring incidents are seen even when they are still being treated at the first stage. Age, menopause, tumors size, inv nodes, node caps, degree of malignancy, side of the breast, and breast quadrant are some of the characteristics that may contribute to the recurrence of breast cancer that will be examined in this study. The dataset consists of 286 observations and 10 variables. 201 instances of one class and 85 instances of another are included in this data collection. Nine qualities, some of which are linear and some of which are nominal, are used to characterize the instances.

## Meta Data
Age – Age of the patient at the time of diagnosis
Menopause – This is the 12 months after a women’s final period
Tumor size – Tumor size represents the size of the cancer tumor at the time of diagnosis
Inv-nodes – Number (ranges from 0 - 39) of lymph nodes in the armpit that contain the spread of breast cancer visible on histological examination
Node caps – Though the outside of the tumor seems to be contained cancer may expose the risk of metastasis to the lymph node.
Degree of malignancy – This is the grade of cancer that is visible under a microscope
Breast – Which side of the breast, does breast cancer occur
Breast quadrant – Which one of the four regions from the nipple area breast cancer occurred
Irradiation – This is a treatment that destroys cancer cells.

## Descriptive Stats and Exploratory Analysis
### Data Cleaning and Standardization
The Dataset have 286 Observations with 10 Features. 
•	Converting data types of categorical variables to Category from Object.
•	We have 8 Missing values represented by "?" we shall be dropping such observation and not replace it with any value as the data might become inaccurate.
•	After performing cleaning, we are left with 278 Observations.

### Checking Duplicate Values
•	There are 14 duplicate observations observation. We will keep the first occurrence of the duplicate observation and drop the next occurring one.
•	After dropping the duplicate observations, we are left with 264 observations. 

## Chi-Square Test
### Hyphothesis Analysis
H0: The variables are not correlated with each other. 
•	The P-Value of the ChiSqResult_class_irradiat Test is: 0.0006346956730777489
•	The P-Value of the ChiSqResult_class_breast Test is: 0.648198791155018
•	The P-Value of the ChiSqResult_class_tumorSize Test is: 0.07623227729746207
•	The P-Value of the ChiSqResult_breast_tumorSize Test is: 0.6897938621853272

### Conclusion
•	For Class and irradiat, we failed to reject H0, the variables are not related to each other.
•	For Class and breast, we reject H0, the variables are related to each other.
•	For Class and tumorsize, we failed to reject H0, they are not related to each other.
•	For Breast and tumorsize, we reject H0, the variables are related to each other.
•	For Breast and Breast Quad, we reject H0, the variables are related to each other.
 
Pre-Processing Of Categorical Features
•	X as the Feature Matrix 
•	y as the response vector 

## Predictive Models
### Model 1: Decision Tree
Setting up the Decision Tree
We used train/test split on our decision tree. We imported train_test_split from sklearn.cross_validation.
Prediction
Decision Tree Accuracy:  0.6582278481012658
Visualization of the Tree
 
### Model 2: Logistic Regression
 
Applying Logistic Regression Model with K Fold Cross Validation
Avg accuracy: 0.5092162554426706

•	Precision is a measure of the accuracy provided that a class label has been predicted. It is defined by: Precision = TP / (TP + FP)
•	Recall is the true positive rate. It is defined as: Recall = TP / (TP + FN)

### Model 3: KNN

Applying K fold cross validation
The best accuracy was with 0.5849056603773585 with k=1

## Conclusion
Therefore, we can conclude that, although K-nearest neighbors (KNN) with cross validation provided a substantial score, unlike the common logistic regression, which yielded a very low accuracy, the best modal for our case is Decision Tree, with a significant score of 0.6582278481012658 that out performs the other two in our analysis.
