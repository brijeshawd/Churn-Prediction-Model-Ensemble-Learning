**Churn Prediction Model for Cab Drivers:**

**Overview:**

Recruiting and retaining drivers is seen by industry watchers as a tough battle for multiple cab organizations. Churn among drivers is high and it’s very easy for drivers to stop working for the service on the fly or jump to other cab services depending on the rates. As the companies get bigger, the high churn could became a bigger problem. To find new drivers, cab organizations are casting a wide net, including people who don’t have cars for jobs. But this acquisition is really costly.Losing drivers frequently impacts the morale of the organization and acquiring new drivers is more expensive than retaining existing ones.

**Problem Statement:**

1. Perform univariate, bivariate and multivariate analysis to understand what factors are affecting in churning.
2. Build a Bagging/Boosting model which can classify whether driver will churn or stay.
3. Check model performance using below metric: ROC AUC,Precision,Recall,F1 Score
4. Find the features which are important in classifying the churning.
5. Provide actionable insights and recommendations which organization can follow during recruitment of drivers.

**Results Achieved:**

1. Developed a predictive model to identify cab drivers who are likely to churn using different ensemble model such as Random Forest, Gradient Boosting, and XGBOOST.
2. Conducted feature importance analysis and compared the performance of individual models using metrics like Precision, Recall and F1-Score to identify the best model .

**Feature Importance:**
![FeatureImportance](https://user-images.githubusercontent.com/17064605/230015261-dfaa73bf-81d7-4d51-a67a-3dabde94380a.png)


**Evaluation of Model:**
Confusion Matrix:
<img width="547" alt="image" src="https://user-images.githubusercontent.com/17064605/230015475-8b43defe-bba8-45fd-b941-063d3356e528.png">


**Insights:**
1. 68% of the drivers have churned whereas 32% are still working in organization.
2. Churned drivers have a high negative correlation with Quaterly rating and total business value and we have also observed that Quaterly rating and total business value has highest feature importance.
3. Male drivers are churning more compared to female drivers.
4. Drivers with a grade of 1 and 2 are churning more compared to other grade drivers.
5. Median Income of drivers who didnt churned is higher than churned drivers.
6. Below are the features which are significant in classifying churned drivers:
 -Quarterly Rating(Feature Imp=0.366)
 -IncresedQuarterlyRating(Feature Imp=0.166)
 -Gender(Feature Imp=0.133)
 -YearsOfService(Feature Imp=0.047)
 -Age(Feature Imp=0.046)
 -Education_Level(Feature Imp=0.053)
 -Total Business Value(Feature Imp=0.040)
 -City(Feature Imp=0.037)
 -Grade(Feature Imp=0.037)
 -Income(Feature Imp=0.030)
 -Joining Designation(Feature Imp=0.021)
 -IncresedMonthlyIncome(Feature Imp=0.024)
 7. With the above feature significance value, precision and recall score when trained with xgboost are 0.81 and 0.92 respectively.
8. Train scores for trained models are as follows:
-Decision Trees:0.828
-Random Forest:0.839
-GBDT:0.86
-XgBoost:0.88
9. Clearly, XgBoost is performing well among all the models with Precision Recall Score of 0.90 and f1 score of 0.86.

**Recommendations:**
1. Quarterly Rating, Gender and YearsOfService are the most important features in determining whether a driver will churn or not. So, organization can look upto these features in detailed manner during recruitment of drivers.
2. More features like completed trips, cancelled trips, distance covered can be provided for analysis to get more confidence whether driver will churn or stay.
3. Females are less likely to churn so more females can be hired.
4. Organization can have a proper discussion with drivers who have bad ratings/ grade and motivate them to get good ratings.
