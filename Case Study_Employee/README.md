This readme is to help you understand the code and important variables

Main Dataset			
Variable Name	Notes		
attrition	Data is being pulled from CaseStudy2-data.csv file		


70/30 Split Train/Test of the Data 			
Variable Name	Predictors		
train_income	70 percent of the data is split to the training dataset and used to "train" the classifcation models		
test_income	30 percent of the data is split to this data set to validate how well the models are tained based off the training dataset	
train_att	70 percent of the data is split to the training dataset and used to "train" the classifcation models
test_att	30 percent of the data is split to this data set to validate how well the models are tained based off the training dataset
	

Predictions For Missing Values			
Output file	Predictors	Notes	
mean_income	Attrition, JobRole, Age		
Case2Predictionslani Salary	JobRole = "Manager", Age = 37	NB predictions for MonthlyIncome if someone is in a manager role and age 37	
Case2SLRPredictlani Salary	JobRole	Linear Regression	
mode_attrition	Department, JobRole, Age	
Case2Predictionslani Attrition	MonthlyIncome, Age	NB predictions for attrition
Case2OVSampPredictlani Attrition	MonthlyIncome, Age	NB oversampling predictions for attrition


KNN Classification Variables | Attrition ONLY			
Description	Variable Name	Classifiers	Notes
Find the best K option	bestk	guassian	
KNN Model	model3	MonthlyIncome, Age	base line / first attempt
KNN Validation with Confusion Matrix	/	/	Print out directly
Leave One Out Test	model4	MonthlyIncome, Age	base line / first attempt
Threshold Tuning	NewModel	Left, Stayed	Only allows to tune to a limit
Over Sampling Tuning	OverSamp1	Left, Stayed	All about the sweet spot
New KNN Model based off Over Sampling Dataset	model_ov	MonthlyIncome, Age	
KNN Over Sampling Validation with Confusion Matrix	/	/	Print out directly


Naïve Bayes Classification Variables			
Description	Variable Name	Classifiers	Notes
NB Model	nbmod	MonthlyIncome, Age	
NB Model Validation with Confusion Matrix	nbCM		
Over Sampling Tuning	OverSamp	Left, Stayed	All about the sweet spot
New NB Model based off Over Sampling Dataset	nb_mod1	MonthlyIncome, Age	
NB Over Sampling Validation with Confusion Matrix	nb_CM1		
NB Model	nb_mod	MonthlyIncome, Age	
NB Base Line Model Validation with Confusion Matrix	nb_CM		
Over Sampling Tuning	OverSamp	Left, Stayed	All about the sweet spot
New NB Model based off Over Sampling Dataset	nb_mod1	MonthlyIncome, Age	
NB Over Sampling Validation with Confusion Matrix	nb_CM1		


Linear Regression Classification Variables			
Description	Variable Name	Classifiers	Notes
SLR	fit	JobRole	Classification Model
RSE for first baseline SLR	current_rse		Capturing RMSE from the model
SLR prediction	pred		Prediction model

