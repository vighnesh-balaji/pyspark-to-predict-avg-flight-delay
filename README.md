# pyspark-to-predict-avg-flight-delay
Use Pyspark for an end-to-end project. Utilizing SQL and ML for PySpark

## Average Delay Estimator: Project Overview
- Read in data using pyspark
- Performed Feature engineering from the existing columns
- EDA on the various columns from all the datasets (flights,planes and airports)
- Utilized SQL for pyspark to join datasets (over 10000 rows)
- Optimized Linear Regression using ParamGrid to reach the best model
- Predicted the average flight delays

## Code and Resources Used
Python Version: 3.9
Packages: pandas, numpy, pyspark SQL functions, pyspark ml

## EDA and Feature Engineering

Determined the following from the data 
- avg speed
- flight duration in hrs
- avg air time of Delta Airlines that left "SEA"
- Total number of hours of all planes
- average departure delay
- Found out the carriers that work between "SEA" and "PDX"

Created features that helped in flight delay prediction and converted datatypes of columns 

## Model Building

First, I transformed the categorical variables into dummy variables. I also split the data into train and test sets with a test size of 40%.

I tried Logistic Regression with Grid Search and evaluated them using AUC(Area Under the Curve). This evaluator calculates the area under the ROC. This is a metric that combines the two kinds of errors a binary classifier can make (false positives and false negatives) into a simple number.

I tried param grid builder for hyperparameter tuning. 
Got a model with an accuracy of close to 70%
