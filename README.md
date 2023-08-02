# deep-learning-challenge

## Overview
 * Alphabet Soup has asked for a tool to help them decide which applicants have the best chance of success in order to choose who to fund. 
 * To do this, I have created a deep learning model to try and predict the outcome of their ventures.
 * This model was trained from a csv file from Alphabet Soup containing more than 34,000 organizations.
 * The data is labeled as such:
     - EIN and NAME—Identification columns
     - APPLICATION_TYPE—Alphabet Soup application type
     - AFFILIATION—Affiliated sector of industry
     - CLASSIFICATION—Government organization classification
     - USE_CASE—Use case for funding
     - ORGANIZATION—Organization type
     - STATUS—Active status
     - INCOME_AMT—Income classification
     - SPECIAL_CONSIDERATIONS—Special considerations for application
     - ASK_AMT—Funding amount requested
     - IS_SUCCESSFUL—Was the money used effectively
 * 'EIN', 'NAME', and 'USE_CASE' were dropped from the data set due to irrelevance.
 * The data was then split into the features and labels, and then training and testing sets. 
 * Then the model was created and used to analyze and predict each orgs. success
    
## Results
 * We Tested for the 'IS_SUCCESSFUL' column in the dataset.
 * All columns not removed are features of the dataset.
 * 'EIN' and 'NAME' are simply identifiers and not relevant to the data.
 * 'USE_CASE' is an important part of the data for humans but needlessly complicates the network and results in a poorer accuracy for the model.
 
 **Manually Optimized**
 * The model is made up of 2 hidden layers, the first contains 8 nodes and the second contains 16
 * For the activation of these two layers I chose tanh, for its ability to retain distance of the data from 0.
 * The final output layer uses only one node and the sigmoid activation. 
 * The accuracy and loss of the model was found to be: Loss: 0.55, Accuracy: 73%

 **Automatically Optimized**
 * The model is made up of 2 hidden layers, the first contains 9 nodes and the second contains 1
 * For the activation sigmoid was chosen
 * The final output layer uses only one node and the sigmoid activation. 
 * The accuracy and loss of the model was found to be: Loss: 0.57, Accuracy: 73%


 * While both of these models work well to determine the outcome of an applicants success, having both high accuracy and relatively low loss, my model has a slightly lower loss score and is my reccomendation.
