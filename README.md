# Data Science Capstone - Starbucks Report

## Installation/Dependencies

- pandas
- numpy
- matplotlib 
- scikit-learn==0.20.0 

## Project Overview
the aim of this study is to build a model that would predict whether or not the customer would complete a bogo or a discount offer.

This is a udacity course, to showcase Data science skills by building a project and communicating the results to a wider audience through code repository (github) and a write up in a blog (Medium blogpost)

The data set contains simulated data from StarBucks rewards mobile app, which provides an informational or an actual offer such as discount or BOGO (buy one get one free).

for this model though, we would focus on the latter, which identifies an actual offer rather than an informational content for the app.

this would actually identify effectiveness of the offer to the particular to a customer before sending the offer across.


## Problem Statement

Build a model that would identify a customer who would complete an offer for bogo or discount.

there are 3 types of offer that starbucks has been providing
- bogo (buy one get one free)
- discount (providing a form of discount)
- informational *

however, for this specific study, I have focused on bogo and discount effectiveness as the main subject of the study or target variable to predict.

setting informational offer type as a form of explanatory feature, showing a form of "visibility" to customers.
though it may also lead towards a transaction (customer spending), bogo and discount are more tangible to measure if crosses the full journey, offer recieved -> offer viewed -> offer completed.

## Metrics used
the model will use AUC and F1-score to measure how well the model does on training and test data.

## Conclusion/Result: as a baseline model, we used logistic regression model that has been optimized using GridsearchCV to select best parameters. with an AUC of 0.75 and F1 score somewhere on 0.7. a decent one for baseline model which can be further improved by exploring further additional features in the future.

I also implemented a Random Forest Classifier tuning the hyperparameters to improve its performace which recorded and AUC of 0.79 which is better the the previous classifer

if time permits, i can consider other features to build such as how long has the last offer/discount been 
approved


## Assumptions
as this is a past data, and I would like to create a "Tenure" feature, we would assume that today is 2018-01-01. which would provide a tenure in days for customers who had become a member. providing insights whether or not they stayed long as a customer.



## File description

- Starbucks_Capstone_notebook.ipynb - shows the codebase used, 
- model.pkl - model that can be used in production environment
- Data/ 
- Readme.md


```
├── README.md
├── Starbucks_Capstone_notebook.ipynb
├── data
│   ├── portfolio.json
│   ├── profile.json
│   └── transcript.json
└── model.pkl
```


## Other links
- Codebase (Github Repo)
- Blog

## Licensing
If you  would like to do further more, it is available below under MIT license.

## Acknowledgements

Data cleaning: 
https://towardsdatascience.com/how-to-extract-key-from-python-dictionary-using-value-2b2f8dd2a995

Model - Random forest hyper parameter tuning
https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74
