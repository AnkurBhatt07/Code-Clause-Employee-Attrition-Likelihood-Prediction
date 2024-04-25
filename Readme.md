Project Summary:

This Project aims to create a ML model that can help in the prediction of employee attrition likelihood . 
We have used the famous HR Employee Attrition dataset for the model creation.The dataset has 1470 rows and 35 columns. 

The names of the columns are as -  'Age', 'Attrition', 'BusinessTravel', 'DailyRate', 'Department',
       'DistanceFromHome', 'Education', 'EducationField', 'EmployeeCount',
       'EmployeeNumber', 'EnvironmentSatisfaction', 'Gender', 'HourlyRate',
       'JobInvolvement', 'JobLevel', 'JobRole', 'JobSatisfaction',
       'MaritalStatus', 'MonthlyIncome', 'MonthlyRate', 'NumCompaniesWorked',
       'Over18', 'OverTime', 'PercentSalaryHike', 'PerformanceRating',
       'RelationshipSatisfaction', 'StandardHours', 'StockOptionLevel',
       'TotalWorkingYears', 'TrainingTimesLastYear', 'WorkLifeBalance',
       'YearsAtCompany', 'YearsInCurrentRole', 'YearsSinceLastPromotion',
       'YearsWithCurrManager'

The 'Attrition' column is the target column containing two unique values 'Yes' and 'No' implying whether the employee left the company(attrition) or not.
Since the target column is containing categorical values , we will build classification models for the prediction.

Out of all the columns , these are the independent numerical columns - 
        
        'Age', 'DailyRate', 'DistanceFromHome', 'Education', 'EmployeeCount',
       'EmployeeNumber', 'EnvironmentSatisfaction', 'HourlyRate',
       'JobInvolvement', 'JobLevel', 'JobSatisfaction', 'MonthlyIncome',
       'MonthlyRate', 'NumCompaniesWorked', 'PercentSalaryHike',
       'PerformanceRating', 'RelationshipSatisfaction', 'StandardHours',
       'StockOptionLevel', 'TotalWorkingYears', 'TrainingTimesLastYear',
       'WorkLifeBalance', 'YearsAtCompany', 'YearsInCurrentRole',
       'YearsSinceLastPromotion', 'YearsWithCurrManager'

We dropped some unnecessary columns .

We did ordinal encoding on some ordinal categorical features and one hot encoding on some nominal categorical features . We also kept in check the dummy variable trap arising from the ohe of the features.

Then we did feature scaling on the numerical features , except for the ohe encoded features. 

Then we did label encoding for the target variable.

Finally implemented multiple classification algorithmns for the model creation for the processed data.


Conclusion


 In This Employee Attrition Likelihood Prediction Model , it is most important for our model to correctly predict the True Positives i.e the employees who are likely to leave the company . In other words , the model with the highest recall score is the most appropriate model . We need less False negatives in the model . 

 Hence looking at the Recall scores of the above models , We see that the tuned logistic Regression ( Tuned) is performing the best out of all with the Recall score of 70.21%  .

 Logistic regression (Tuned) model is giving a higher False positive instances compared to the DT model and Random Forest models.The best precision or the lowest false positive is given by the Random Forest models , however there recall scores are lowest hence they cannot be chosen as the model for this particular project.

 As per the Confusion Matrix of Logistic regression (tuned) we can see that the False Negative instances = 14 and False Positive instances = 54.The True Positive instances = 33 (the most significant value) .

 Other metrics of Logistic regression (tuned) - 
                                                Accuracy Score  =  0.7687074829931972
                                                Precision Score  =  0.3793103448275862
                                                Recall Score =  0.7021276595744681
                                                F1 score =  0.4925373134328358
 
