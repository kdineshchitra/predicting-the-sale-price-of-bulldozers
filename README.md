# Predicting the sale price of bulldozers, using machine learning

Predicting the future sale price of a bulldozer, given its characteristics & previous examples of how much similar bulldozers have been sold for.  
This is a single notebook project which demonstrates some foundational machine learning and data science concepts by exploring the problem of sales price prediction.  

## Environment requirments

This project is a single notebook(.ipynb file) in Python3, created using [Google Colab](https://research.google.com/colaboratory/).  

## Problem Statement

**Supervised Learning - Regression Problem:** Predict the future sale price of a bulldozer, based on it's usage, equipment type, and configuaration.  

## Data to solve the problem:

The data is taken from the [Blue Book for Bulldozers Kaggle Competition](https://www.kaggle.com/c/bluebook-for-bulldozers/data).  
The data for this competition is split into three parts:
1. Train.csv is the training set, which contains data through the end of 2011.
2. Valid.csv is the validation set, which contains data from January 1, 2012 - April 30, 2012.
3. Test.csv is the test set. It contains data from May 1, 2012 - November 2012.  

Since this data contains data points indexed in time order(in saledate feature), this dataset is a Timeseries data.  
Refer the [data dictionary](https://github.com/kdineshchitra/predicting-the-sale-price-of-bulldozers/blob/master/assets/Data%20Dictionary.csv) provided (by Kaggle competition creators) with this dataset to understand more about the features of the data.  

## Data Cleaning & Preprocessing

The 'train and valid' data has 412698 examples(412698 rows) with 52 features + 1 label variable(53 columns). There are lot of missing values and they are in various datatypes.  

So in order to feed the data into a ML model, there is need for imputation(filling missing values) and feature encoding(converting non-numerical data to numerical data).  
To do so, the advantage of Pandas library is utilized. The missing numeric values or filled with median value and non-numeric values are converted into Pandas categorical datatype and filled.  

Since the `saledate` column is parsed as `pandas.datatime` object, the different datetime attributes are accessed and new columns like `SaleDate`, `SaleMonth`, `SaleYear` are created.  

The processed data is split into train and vaild sets using the timestamp `SaleYear` feature(curated from `saledate` feature).  
Then the separated train and valid sets split into feature(X_train, X_valid) and target labels(y_train, y_valid).  

## Model building & Performance

The main ML algorithm used in this notebook is [RandomForestRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html).  
There are lot of regression algorithms out there; but for simplicity, clarity and understanding the process this commonly used essential regression algorithm is chosen and utilized.  

According to [Kaggle Bluebook for Bulldozers competition](https://www.kaggle.com/c/bluebook-for-bulldozers/overview/evaluation), the recommended evaluation metric to use is **root mean squared log error (RMSLE)**.  
Other than RMSLE, the following evaluation metrics are used to test the model performance.  
- r2_score (the coefficient of determination)
- mean_squared_error
- mean_absolute_error
- mean_squared_log_error  

Finally the trained model is analyzed to find the feature importances.  
<img src="assets/Feature Importance.png" alt="Feature Importance" />  

## Further experiment and analysis

***Apart from the things which were tried in this project, there are so many methods and ways to explore a structured dataset and extract insights from it.***  
In addition to these, the other ideas or concepts can be used to utilize this data and extract more insights.  
Such as,  

- Generally, Collecting more data would be very useful.
- Trying different algorithms to build a better model.
- More research & trying different hyperparameters for tuning the current model.
- Modifying/Improving the model evaluation methods & metrics

Spending more time to understand the problem and data helps, ALWAYS.  
Consulting a subject matter export(SME) on the data would be great to see all the information in a productive way with the domain knowledge.  

The machine learning model creation, training and development are always an iterative experimentation process. Every problems and questions which are required answer have their own different kind of solutions. Approaching different problems in their own ways within the given situation and statements is important.  
Starting with understanding the problem statement, which question is to be answered, why and how much it is to solve are paramount.  

---
Thanks for viewing this project and my [Github Profile](https://github.com/kdineshchitra).  
Please provide your thoughts and insights to this little project.  
Always ready to collaborate, learn and grow with others. See you in my next project.

