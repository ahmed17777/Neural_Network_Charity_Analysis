# Charity Analysis with Neural Networks

Syed Ahmed 
July 6, 2021 

![images](https://user-images.githubusercontent.com/45697471/124657472-8a202d00-de70-11eb-9ff7-6c69c29054f4.jpg)


## Overview 

This project explores Alphabet Soup's charity data to classify the success of charitable donations using deep-learning neural networks with the TensorFlow library in Python. Data was analyzed using the following steps: 

1. Preprocessing data for the neural networks model
2. Copiling, training, and evaluating the model
3. Optimizing the model 

The following is the background provided by the client: 

Bek’s come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

- `EIN and NAME`—Identification columns
- `APPLICATION_TYPE`—Alphabet Soup application type
- `AFFILIATION`—Affiliated sector of industry
- `CLASSIFICATION`—Government organization classification
- `USE_CASE`—Use case for funding
- `ORGANIZATION`—Organization type
- `STATUS`—Active status
- `INCOME_AMT`—Income classification
- `SPECIAL_CONSIDERATIONS`—Special consideration for application
- `ASK_AMT`—Funding amount requested
- `IS_SUCCESSFUL`—Was the money used effectively

## Resources 
`charity_data.csv`

## Results 

Here is what I found after using deep learning the analyze the dataset: 

### Data Preprocessing

- The first step was to remove `EIN` and `NAME` columns from the input data, as they were not relevant to our analysis
- The `IS_SUCCESSFUL` column was our target variable for the deep learning model, as it contains binary data referring to whether or not the charity donation was successful 
- I used the following columns as features for the model: `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT`

![1](https://user-images.githubusercontent.com/45697471/124656928-d7e86580-de6f-11eb-9e13-8ccba560dfd5.png)


### Compiling, Training, and Evaluating the Model 

![2](https://user-images.githubusercontent.com/45697471/124657054-ff3f3280-de6f-11eb-907c-54b37cbb7049.png)


- As we can see from the image, the neural network model has two hidden layers with 80 neurons in the first layer and 30 in the second \
I used the `ReLU` activation function for the hidden layers, and `Sigmoid` for the output layer 
- The original model accuracy was about 73%, which is not optimal to predict the outcome of the charity donations 
- To improve the performance of the model, I did the following: \
Applied binning to the `ASK_AMT` feature to organize the values by set intervals \
Added more hidden layers to the model \
I also used a different activation function in the hidden layers (`tanh`), which gave us the highest accuracy score out of all other attempts, but still under 75%

## Summary

Unfortunately, even after all attempts to optimize the model, the accuracy did not reach our minimum requirement of 75%. Therefore, we cannot successfully use this model to classify charitable donations. Due to the fact that the target variable is binary, making this a binary classification, supervised machine learning could be useful in trying to classify the success of charitable donations, rather than deep learning. Perhaps the Random Forest Classifier could be used in this model to create decision trees that could classify the target variable. 

### Contact 
Email: mishaal22s@gmail.com
