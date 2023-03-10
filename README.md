# 3-9_Sales_predictions
 The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.
# Predicting Sales with ML models
## LinearRegression vs. DecisionTree

**Author**:Leard Russell 

### Business problem:

Can we predict future sales when given info on:
'Item Fat Content', 'Item Visibility', 'Item Type', 'Item MRP', 'Outlet Establishment Year', 'Outlet Size', 'Outlet Location Type', 'Outlet Type'. 

### Data:
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/ 

## Methods
- Data preparation steps with explanation and justification for choices
- Data Cleaning: getting rid of duplicates rows and incorrect/questionable values
- Validation Split: splitting data to prepare it for machine learning
- Data Transformation: Using transformers and pipelines for preprocessing
- Evaluating a linear regression model and a decision tree regression model for sales predictions


#### Linear Regression performance:
• Results for training data:
  - R² = 0.561
  - RMSE = 1140.388
• Results for test data:
  - R² = 0.566
  - RMSE = 1094.455

#### Decision Tree performance:
• Results for training data:
  - R² = 1.0
  - RMSE = 0.0
• Results for test data:
  - R² = 0.216
  - RMSE = 1470.764
  
  ![image](https://user-images.githubusercontent.com/118066797/224283193-cf2b723b-95a1-446b-8671-f1b1ecbc6498.png)
The features with the highest correlation to the target 'Item_Outlet_Sales' were 'Item_MRP' and 'Outlet_Establishment_Year'
  
![image](https://user-images.githubusercontent.com/118066797/224282368-c09714cb-f4b6-45ab-98c3-b02475a4d164.png)
Supermarket Type 1 had the overwhelming majority of counts while Types 2,3 and grocery store capped at around 1000. 

In contrast to the linear regression model, whose train and test R² scores are nearly identical, the decision tree's R² scores are in stark contrast. We have a huge disparity between our perfect 1.0 Training R² score and our poor 0.216 Test R² score. Of course this means our RMSE for our decision is very large at 1470. 
## Recommendations:

Considering both the R2 and RMSE scores for both regressors, I would recommend using the linear regressor because it has higher predictive power than that of the decision tree regressor. 
The linear regressor's room for error is less than that of that of the decision tree. 

For any additional questions, please contact **leardrussell@gmail.com**
