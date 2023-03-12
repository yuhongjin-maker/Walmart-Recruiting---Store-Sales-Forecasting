# Walmart-Recruiting---Store-Sales-Forecasting

## Objective
 Predicting store sales using  historical sales data for 45 Walmart stores located in different regions.
 
 
## Introduction
Modeling retail data based on the historical sales data to predict stores sales, it is a very important for WalMart's strategic decisions accurate data will ensure that stock replenishment is at par with future demand.

### stores.csv

This file contains anonymized information about the 45 stores, indicating the type and size of store.

### train.csv

This is the historical training data, which covers to 2010-02-05 to 2012-11-01. Within this file you will find the following fields:

Store - the store number
Dept - the department number
Date - the week
Weekly_Sales -  sales for the given department in the given store
IsHoliday - whether the week is a special holiday week
test.csv

This file is identical to train.csv, except we have withheld the weekly sales. You must predict the sales for each triplet of store, department, and date in this file.

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

## Methodogy

### Exploratory Data Analysis
In this part, I analyzed the proportion of data in each store type (A,B,C), and the average weekly sales, average monthly sales, average department sales per year and the relationship between size of store and sales, the relationship between temperature and sales, the relationship between fuel price and sales, the relationship between CPI and Sales, the relationship bettween unemployment and Sales. 
Using Correlation Matrix to check conform the inferences we have concluded from the above EDA study.


### Feature Enginerring
### Visualizing Correlations
### Encoding Store Column


## Results
