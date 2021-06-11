# Predicting the sale price of bulldozers, using machine learning

Predicting the future sale price of a bulldozer, given its characteristics & previous examples of how much similar bulldozers have been sold for.  
This is a single notebook project which demonstrates some foundational machine learning and data science concepts by exploring the problem of sales price prediction.  

## Environment requirments

This project is a single notebook(.ipynb file) in Python3, created using [Google Colab](https://research.google.com/colaboratory/).  

## Problem Statement

**Supervised Learning - Regression Problem:** Predict the future sale price of a bulldozer, based on it's usage, equipment type, and configuaration.  

## Data to solve the problem:

The data is taken from the Blue Book for Bulldozers Kaggle Competition.([link here](https://www.kaggle.com/c/bluebook-for-bulldozers/data))  
The data for this competition is split into three parts:
1. Train.csv is the training set, which contains data through the end of 2011.
2. Valid.csv is the validation set, which contains data from January 1, 2012 - April 30, 2012.
3. Test.csv is the test set. It contains data from May 1, 2012 - November 2012.  

Since this data contains data points indexed in time order(in saledate feature), this dataset is a Timeseries data.  
Refer the [data dictionary](https://github.com/kdineshchitra/predicting-the-sale-price-of-bulldozers/blob/master/Data%20Dictionary.csv) provided (by Kaggle competition creators) with this dataset to understand more about the features of the data.  

