# Automobile-price-prediction
This data set consists of three types of entities: (a) the specification of an auto in terms of various characteristics, (b) its assigned insurance risk rating, (c) its normalized losses in use as compared to other cars. The second rating corresponds to the degree to which the auto is more risky than its price indicates. Cars are initially assigned a risk factor symbol associated with its price. Then, if it is more risky (or less), this symbol is adjusted by moving it up (or down) the scale. Actuarians call this process "symboling". A value of +3 indicates that the auto is risky, -3 that it is probably pretty safe.    
The third factor is the relative average loss payment per insured vehicle year. This value is normalized for all autos within a particular size classification (two-door small, station wagons, sports/speciality, etc…), and represents the average loss per car per year.   
Shape of Data = 205x26



##TODO-----


## Aim of this project 📝   
Predict the price of the car based on the features in the dataset.




## Evaluation ✔️  
A model with good r2 score > 0.90




Before we start analysing our dataset, we need to do some data preprocessing in order to handle missing values and outliers. As we can see there are some '?' in normalized-losses column.    
<img width="657" alt="Untitled" src="https://user-images.githubusercontent.com/91877930/141124479-75594987-d608-48cc-a9d4-a7abef4632c2.png">



## Data Preprocessing (Cleaning) 🧹  

Though we do not get any null values while checking with isnull().sum() there are numerous '?' values. So we replace '?' with NaN and subsequently replace it with mean value for each numerical feature.
For categorical features the missing value was replaced by the most frequent entry throughout the feature.

## Exploratory Data Analysis 📉

Correlation between numerical features with the target price
![image](https://user-images.githubusercontent.com/91877930/141129748-ceccf152-aa27-4627-9ac5-02a99f466271.png)    
Univariate, Bivariate analysis also done on the numerical features.


## Feature Engineering ⚙️

Checked for outliers in the numerical features using boxplots
![image](https://user-images.githubusercontent.com/91877930/141130857-66ea837b-b54d-4632-9cda-c2f0aa84b970.png)

Performed dummy variable encoding on categorical features

## Building Machine Learning Model 🤖

Did a training and test split and fit various regression models on the training data and checked the R2 score for each model.    
### Conclusion
### Gradient Boosting Regressor with r2 score of 0.93 performed better than other regression models
![image](https://user-images.githubusercontent.com/91877930/141132165-7026ffa0-9537-43a7-8431-f763b785acb8.png)




