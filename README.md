# Neural_Network_Charity_Analysis

 ## Overview:

Alphabet Soup is a philanthropic, non-profit business dedicated to helping organizations make the world a better place. They donate money to various businesses that strive to improve the quality of life for humans for generations to come. With my knowledge of machine learning and neural networks, I'll use the features in the provided dataset to help create a binary classifier that is capable of predicitng whether applicants will be successful if funded by Alphabet Soup.

## Results:

### Data Preprocessing

1. What variable(s) are considered the target(s) for your model?

 The target variable for this dataset is IS_SUCCESSFUL variable — Was the money used effectively?

2. What variable(s) are considered to be the features for your model?

The following are considered to be features within the dataset:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested

3. What variable(s) are neither targets nor features, and should be removed from the input data?

In the first model, the features 'EIN' and 'NAME' were removed from the input data because they were irrelevant to the question I am trying to answer. 

In the second model (optimization), the features 'EIN', 'NAME', 'STATUS', and 'SPECIAL_CONSIDERATIONS' were removed from the input data in attempt to simplify the input so the algorithm could focus on features that would have a greater impact on the predictive accurary. 


### Compiling, Training, and Evaluating the Model

1. How many neurons, layers, and activation functions did you select for your neural network model, and why?

In the first model, there are 3 hidden layers with 8 neurons in the first layer, 6 neurons in the second layer, and 4 neurons in the third layer. For the input layers, relu was used as the activation function and for the output layer sigmoid was used as the activation function. The activaton functions used were chosen because they best fit our model of non-linear, binary classification. The number of neurons and layers I chose is mostly arbitrary. 

In the second model, there are 5 hidden layers with 3 neurons in the first layer, 7 neurons in the second layer, 1 neuron in the third layer, 5 neurons in the fourth layer, and 7 neurons in the fifth layer. For the input layers, the relu activation was used and for the output layer sigmoid was used as the activation function. The nummber of neurons, hidden layers, and activation functions were chosen after running kerastuner search for best hyperparameters.

2. Were you able to achieve the target model performance?

No I was not.

3. What steps did you take to try and increase model performance?

Here's a list of things I did in attempt to increase model performance:

* removed additional input features that were noisy or didn't add value in terms of increasing predictive accuracy 
* put the values in the ASK_AMT column into bins to simplify the data
* ran kerastuner search for best hyperparameters

## Summary: 

The predictive accuracy of the original model and the optimized model are right around ~73%. In an ideal world, we would want a model that's more accurate to make sound decisions. 

I changed the parameters (layers, neurons, epochs, activation function, etc.) countless times and also ran the data through almost every type of model and could not get the predictive accurary to go any higher. At this time, I do not have any recommendations on a model to solve this classification problem. 
