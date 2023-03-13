# Walmart-Recruiting---Store-Sales-Forecasting

## Objective
 Predicting store sales using  historical sales data for 45 Walmart stores located in different regions.
 
 
## Introduction
Modeling retail data based on historical sales data to predict store sales is very important for Walmart's strategic decision-making process. Accurate data ensures that stock replenishment is in line with future demand, which can help retaillers improve customer staisfaction. Forecasting is often used to adjust ads and marketing campaigns, and it can influence the number of sales.

### stores.csv

This file contains anonymized information about the 45 stores, indicating the type and size of store.

### train.csv

This is the historical training data, which covers to 2010-02-05 to 2012-11-01.

Store - the store number
Dept - the department number
Date - the week
Weekly_Sales -  sales for the given department in the given store
IsHoliday - whether the week is a special holiday week

### test.csv

The same as the train.csv except IsHoliday Column

### features.csv

This file contains additional data related to the store, department, and regional activity for the given dates. It contains the following fields:

Store - the store number
Date - the week
Temperature - average temperature in the region
Fuel_Price - cost of fuel in the region
MarkDown1-5 - anonymized data related to promotional markdowns that Walmart is running. MarkDown data is only available after Nov 2011, and is not available for all stores all the time. Any missing value is marked with an NA.
CPI - the consumer price index
Unemployment - the unemployment rate
IsHoliday - whether the week is a special holiday week

### Performance metric
<img width="365" alt="Screen Shot 2023-03-12 at 7 17 28 PM" src="https://user-images.githubusercontent.com/59128675/224580051-ffe8ea20-a621-4e3e-a5fd-d5fa921a37f9.png">

## Methodogy

### Exploratory Data Analysis

In this part, I analyzed the proportion of data in each store type (A,B,C), 
<img width="422" alt="Screen Shot 2023-03-12 at 8 04 42 PM" src="https://user-images.githubusercontent.com/59128675/224582336-d97cad3a-ad74-4ff5-8956-a1f4a20267a5.png">

and the average weekly sales, average monthly sales per year 
<img width="549" alt="Screen Shot 2023-03-12 at 8 05 39 PM" src="https://user-images.githubusercontent.com/59128675/224582388-ad85845f-537d-4c50-9fb3-bd4388261998.png">
<img width="522" alt="Screen Shot 2023-03-12 at 8 05 59 PM" src="https://user-images.githubusercontent.com/59128675/224582411-0f995c94-9db9-48e8-a3a8-682edd0c5770.png">

and the relationship between size of store and sales, the relationship between temperature and sales, the relationship between fuel price and sales, the relationship between CPI and Sales, the relationship bettween unemployment and Sales. 
<img width="521" alt="Screen Shot 2023-03-12 at 8 07 30 PM" src="https://user-images.githubusercontent.com/59128675/224582544-b8e38af6-8a2d-4fda-8266-3a1c25003cb7.png">
<img width="510" alt="Screen Shot 2023-03-12 at 8 08 01 PM" src="https://user-images.githubusercontent.com/59128675/224582573-afe4e02c-1c20-4811-8b54-106c60a2bff9.png">
<img width="487" alt="Screen Shot 2023-03-12 at 8 08 16 PM" src="https://user-images.githubusercontent.com/59128675/224582586-0c21e291-2a12-4d4c-9e66-afa6a28adcba.png">
<img width="496" alt="Screen Shot 2023-03-12 at 8 08 36 PM" src="https://user-images.githubusercontent.com/59128675/224582601-560233a4-a426-4de3-8641-c4003803fa5d.png">
<img width="495" alt="Screen Shot 2023-03-12 at 8 08 47 PM" src="https://user-images.githubusercontent.com/59128675/224582613-7a787bea-e8a1-4c56-94b5-8c807163d7c9.png">


Using Correlation Matrix to check conform the inferences we have concluded from the above EDA study.
<img width="554" alt="Screen Shot 2023-03-12 at 8 03 13 PM" src="https://user-images.githubusercontent.com/59128675/224582263-bbbe7ad6-e1e4-49ef-ae39-9dbf9437d663.png">


### Data Preparation 

According to the EDA and Coorelation study, dropped the columns with relationship with the target column. Training and created the training, validation datasets.

### Machine Learning

#### Linear Regression

* WMAE for Training set: 14776.36
* WMAE for Validation set: 14884.37

#### Decision Tree

* WMAE for Training set: 0.0
* WMAE for Validation set: 1938.54

#### Random Forest

* WMAE for Training set: 569.99
* WMAE for Validation set: 1571.46


#### Gradient Bopsting Machine

* WMAE for Training set: 16.66
* WMAE for Validation set: 1339.29

## Results

After comparing those models, I can conclude that the best performer is Gradient Boosting with tuned hyperparameters. In a word, store sales forecasting is a critical component of successful retail operations, and retailers should invest in the tools and resources necessary to do it effectively.
