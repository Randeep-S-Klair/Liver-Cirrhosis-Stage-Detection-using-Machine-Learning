# Liver-Cirrhosis-Stage-Detection-using-Machine-Learning
Liver Cirrhosis Stage Detection - Machine Learning Project Report
________________________________________
1. Project Overview
This project focuses on predicting the histologic stage of liver cirrhosis (Stage 1, 2, or 3) using patient clinical and biochemical data from the Mayo Clinic study. The goal is to compare the performance of different machine learning models in classifying cirrhosis stages accurately.
________________________________________
Models Compared
•	Logistic Regression
•	Support Vector Machine (SVM)
•	Random Forest
•	XGBoost
________________________________________
2. Dataset
The dataset contains patient clinical and biochemical data with the following features:
•	N_Days: Number of days of follow-up
•	Status: Patient status (Censored or Deceased)
•	Drug: Type of drug administered
•	Age: Patient age
•	Sex: Patient gender
•	Clinical indicators: Ascites, Hepatomegaly, Spiders, Edema
•	Biochemical measurements: Bilirubin, Cholesterol, Albumin, Copper, Alk_Phos, SGOT, Tryglicerides, Platelets, Prothrombin
•	Target: Stage (1, 2, or 3)
________________________________________
3. Data Preprocessing
1.	Handling Missing Values: Numeric missing values were filled with median values
2.	Categorical Encoding: Label encoding was applied to categorical variables including:
o	Platelets, Prothrombin, Ascites, Hepatomegaly, Spiders, Bilirubin, Edema
3.	Feature Scaling: StandardScaler was used to standardize all features
4.	Target Mapping: Stage values were mapped from [1,2,3] to [0,1,2] for ML compatibility
5.	Train-Test Split: 70-30 split with random_state=42
________________________________________
4. Model Performance
Random Forest
•	Accuracy: 95.43%
•	Precision: 95% (macro avg)
•	Recall: 95% (macro avg)
•	F1-score: 95% (macro avg)
•	Confusion Matrix shows strong performance across all classes
Logistic Regression
•	Accuracy: 58.36%
•	Precision: 58% (macro avg)
•	Recall: 59% (macro avg)
•	F1-score: 58% (macro avg)
•	Significant misclassifications between all three stages
XGBoost
•	Accuracy: 96.21% (Best performing model)
•	Precision: 96% (macro avg)
•	Recall: 96% (macro avg)
•	F1-score: 96% (macro avg)
•	Excellent performance with minimal misclassifications
SVM
•	Accuracy: 81.99%
•	Precision: 82% (macro avg)
•	Recall: 82% (macro avg)
•	F1-score: 82% (macro avg)
•	Moderate performance with some confusion between classes
________________________________________
5. Model Comparison
Model	Accuracy	Precision (macro)	Recall (macro)	F1-score (macro)
XGBoost	96.21%	96%	96%	96%
Random Forest	95.43%	95%	95%	95%
SVM	81.99%	82%	82%	82%
Logistic Regression	58.36%	58%	59%	58%
________________________________________
6. Key Findings
1.	XGBoost outperformed all other models with 96.21% accuracy
2.	Tree-based models (XGBoost and Random Forest) significantly outperformed linear models
3.	Logistic Regression performed poorly, suggesting non-linear relationships in the data
4.	The dataset appears to be well-suited for ensemble methods
5.	All models showed consistent performance across the three classes
________________________________________
7. Recommendations
1.	XGBoost should be selected as the primary model for deployment
2.	Feature importance analysis could provide insights into which clinical factors are most predictive
3.	Hyperparameter tuning could further improve model performance
4.	Cross-validation should be implemented for more robust performance estimation
5.	Clinical validation is recommended before deployment in medical settings
________________________________________
8. Limitations
1.	The dataset may have class imbalance issues that weren't addressed
2.	No feature importance analysis was conducted
3.	Hyperparameter tuning was not performed for most models
4.	No cross-validation results are reported
________________________________________
9. Future Work
1.	Implement hyperparameter tuning for all models
2.	Conduct feature importance analysis
3.	Address potential class imbalance
4.	Implement cross-validation for more reliable results
5.	Explore deep learning approaches for comparison
6.	Conduct clinical validation with medical experts
________________________________________
10. Conclusion
This project successfully demonstrates that machine learning can effectively predict liver cirrhosis stages from clinical data, with XGBoost achieving excellent performance (96.21% accuracy). The results suggest potential for clinical application in assisting medical professionals with cirrhosis staging.


