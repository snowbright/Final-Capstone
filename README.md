# What's in the Job Title? 
Note: the project files and the PowerPoint Presentation are located in the same repo.

## Problem Statement 
* Gap between actual salary and job seeker's expectation 
* Job seekers spend time on researching salaries 

## Objectives 
* Build an algorithm to estimate annual income based on target job title, employment length and location
* Examine the importance of job title in predicting income

## Data 
* 2018 data from Lending Club dataset 
* 495,242 rows 

## Part I: Predict annual income with job title, employment length and location
### Features 
Feature | Example | Type | Cardinality 
------------ | ------------- |------------- |------------- 
Job Title | Chef | Natural Language | 129,443
Zip Code | 109xx | Categorical | 895
Employment Length | 10+ years | Categorical | 11

### Feature Engineering 
* Employment Length: categorical to ordinal 
* Zip Code: one-hot encoding 
* Job Title: NLP, spaCy (En_core_web_lg)

### Models 
* Stochastic Gradient Descent
* Ridge Regression
* Lasso Regression 
* Neural Network (Deep Learning)

### Final Model 
* 2-Layer Neural Network 
* R-squared: 0.14
* RMSE: $78K

## Part II: Use only job title to predict salary for zip code 112xx

### Semantic Analysis 
* NLP job title 
* Compute consine similarity on the 300d word2vec vectors
* Use similarity scores as predictors 

### Final Model 
* Polynomial Ridge Regression 
* R-squared: 0.12
* RMSE: $48K

## Future Work 
* Add time series data
* Find more data for each zip code 
* Incorporate numeric geographic variables if possible


