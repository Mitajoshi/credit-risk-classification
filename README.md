# Credit Risk Classification

## Overview
Various techniques to train and evaluate a model are used, based on loan risk. A dataset of historical lending activity from a peer-to-peer lending services company is utilized in this study, to build a model that can identify the creditworthiness of borrowers.

## Procedure
The data exploration and analysis for this study has been performed in the following manner:

1. Stage 1- Split the Data into Training and Testing Sets

2. Stage 2 - Create a Logistic Regression Model with the Original Data

3. Stage 3 - Create a Logistic Regression Model with Resampled Data which has been balanced through a RandomOverSampler module  

4. Stage 4 - Analyze above models to create a Credit Risk Analysis Report

## Description of the Model Outcomes


<img width="105" alt="image" src="https://github.com/Mitajoshi/credit-risk-classification/assets/142932546/bdbfec68-233b-43a3-a30e-54058247224d">


- Accuracy: 99%
- Precision: Score of 1.00 for healthy loans and score of 0.87 for high-risk loans. 
- Recall: Score of 1.00 for healthy loans and score of 0.95 for high-risk loans. 


<img width="107" alt="image" src="https://github.com/Mitajoshi/credit-risk-classification/assets/142932546/9626de8e-9d2c-4431-9db4-bae7bcb9dc75">


- Accuracy: 99%
- Precision: Score of 1.00 for healthy loans and score of 0.87 for high-risk loans. 
- Recall: Score of 1.00 for healthy loans and score of 1.00 for high-risk loans. 



## Credit Risk Analysis Report

### Prediction of healthy vs high-risk loans in the Original Dataset

Upon initial inspection of the original data, it is perceived that the dataset was skewed. The number of zeros (healthy loans) far outnumbered the ones (high-risk loan). 

<img width="165" alt="image" src="https://github.com/Mitajoshi/credit-risk-classification/assets/142932546/1365e691-a057-411a-bf48-a4e529e525c3">


With this discovery, it was with this knowledge that the Logistic Regression model was employed to train and test the original dataset. 

 According to the classification report of the logistic regression model, the healthy loans (0) get predicted with 100% accuracy and the high-risk loans (1) get predicted at 91% accuracy on average. 

<img width="361" alt="image" src="https://github.com/Mitajoshi/credit-risk-classification/assets/142932546/fcee7b4a-6319-477e-a240-d340d33e0807">


While 91% is not a bad prediction rate, it may be lower than the 100% accuracy of the healthy loans since there were far more healthy loans to train the model on, as opposed to the high-risk loan cases. The accuracy of the overall model is 99%, which is highly acceptable. 

### Prediction of healthy vs high-risk loans in the Oversampled Dataset

 The original dataset was skewed and this part of the exercise was aimed at examining the model performance on a balanced dataset. By recruiting the RandomOverSampler() function, the healthy loans and the high-risk loans were evened out to 56277 a piece. 

<img width="207" alt="image" src="https://github.com/Mitajoshi/credit-risk-classification/assets/142932546/f556a41e-2e9f-4f09-b82c-b002a0887f63">


The Logistic Regression model was again employed to train and test the oversampled dataset. 


<img width="348" alt="image" src="https://github.com/Mitajoshi/credit-risk-classification/assets/142932546/f6594fab-5773-4b0e-82b9-f70c6597a774">


 The logistic regression model that was fit with the oversampled data performed slightly better than the previous model in the case of predicting the high-risk loans (1). It increased from an overall 91% to 93%. This test is a better prediction of high-risk loans by 2%. The false negative prediction was reduced significantly in this case. The healthy loans (0) got predicted at 100% in both cases.The accuracy of the overall model is 100%, which is the best possible outcome. 




