# Neural_Network_Charity_Analysis
## Overview
The purpose of this analysis is to create a neural network model that can predict whether applicants will be successful if funded by Alphabet Soup's nonprofit sponsorships. To create our model, we will use Alphabet's data of previously sponsored nonprofit organization. This data contains if the non-profit organization has been successful and other features such as total income, application type, affiliation, used case, and classification. 
## Results
1. Data Preprocessing:
    1. The target for this model will be weather the non-profit organization has been successful or not, shown in our data as column "IS_SUCCESSFUL". 
    2. The data variables titled non-profit "EIN" and "NAME" are irrelevant to this study and have been removed. 
    3. All other variables will be considered as features (inputs) for this neural network model. 
2. Compiling, Training, Evaluating the Model:
    1. For our first attempt at creating a neural network model, we started with a two-layer neural network model. Both layers used the linear activation functions, while the output layer used sigmoid activation functions. The linear activation function where used due to its applicability, and since they can easily be stacked. 

    2. For the second attempt, we ended up optimizing the first design with the following: 
        * First optimization, we increase the quantity of the nodes by a factor of two, and the model started to show signs of overfitting. 
        * Second optimization, we changed the second layer from a linear relationship to a "LeakyRelu", this will allow for the model to continue learning if any input coefficients are negative and will allow us to determine if they are any thresholds for any of the features. 
        * Third optimization, we added a neural network layer. 

## Summary

