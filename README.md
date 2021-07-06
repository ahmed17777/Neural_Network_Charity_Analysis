# Charity Analysis with Neural Networks

Syed Ahmed 
July 6, 2021 

## Overview 

This project explores Alphabet Soup's charity data to classify the success of charitable donations using deep-learning nerual networks with the TensorFlow tool in Python. Data was analyzed using the following steps: 

1. Preprocessing data for the neural networks model
2. Copiling, training, and evaluating the model
3. Optimizing the model 

The following is the background provided by the client: 

Bek’s come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Resources 
charity_data.csv

## Results 

Here is what I found after using deep learning the analyze the dataset: 

### Data Preprocessing

- The first step was to remove `EIN` and `NAME` columns from the input data, as they were not relevant to our analysis
- The `IS_SUCCESSFUL` column was our target variable for the deep learning model, as it contains binary data referring to whether or not the charity donation was successful 
- I used the following columns as features for the model: `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT`
