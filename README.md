# Neural_Network_Charity_Analysis
## Overview
The purpose of this analysis is to create a neural network model that can predict whether applicants will be successful if funded by Alphabet Soup's nonprofit sponsorships. To create our model, we will use Alphabet's data of previously sponsored nonprofit organization. This data contains if the non-profit organization has been successful and other features such as total income, application type, affiliation, used case, and classification. 
## Results
1. Data Preprocessing:
    1. The target for this model will be weather the non-profit organization has been successful or not, shown in our data as column "IS_SUCCESSFUL". 
    2. The data variables titled non-profit "EIN" and "NAME" are irrelevant to this study and have been removed. 
    3. All other variables will be considered as features (inputs) for this neural network model. 
2. Compiling, Training, Evaluating the Model:
    1. For our first attempt at creating a neural network model, we started with a two-layer neural network model. Both layers used the linear activation functions, while the output layer used sigmoid activation functions. The linear activation function where used due to its applicability, and since they can easily be stacked. The first model yielded a 72% accuracy.   
    ![Accuracy.PNG](https://github.com/rick2stack/Neural_Network_Charity_Analysis/blob/main/Resources/first_accuracy.PNG)

    ![Loss.PNG](https://github.com/rick2stack/Neural_Network_Charity_Analysis/blob/main/Resources/first_loss.PNG)

    2. For the second attempt, we ended up optimizing the first design with the following: 
        * First optimization, we increase the quantity of the nodes by a factor of two, and the model started to show signs of overfitting. This model yielded the same accuracy of 72%. 
        ![Accuracy_and_Loss](https://github.com/rick2stack/Neural_Network_Charity_Analysis/blob/main/Resources/second_attempt_try1_metrics.PNG)
        
        ![Accuracy_and_Loss_Charts](https://github.com/rick2stack/Neural_Network_Charity_Analysis/blob/main/Resources/second_attempt_try1.PNG
        * Second optimization, we changed the second layer from a linear relationship to a "LeakyRelu", this will allow for the model to continue learning if any input coefficients are negative and will allow us to determine if they are any thresholds for any of the features.  This model also yielded the same accuracy of 72%.
        ![Accuracy_and_Loss](https://github.com/rick2stack/Neural_Network_Charity_Analysis/blob/main/Resources/second_attempt_try2_metrics.PNG)
        
        ![Accuracy_and_Loss_Charts](https://github.com/rick2stack/Neural_Network_Charity_Analysis/blob/main/Resources/second_attempt_try2.PNG
        * Third optimization, we added a neural network layer with a "ReLu" activation function.This model yielded a bit better, with an accuracy of 73%.
        ![Accuracy_and_Loss](https://github.com/rick2stack/Neural_Network_Charity_Analysis/blob/main/Resources/second_attempt_try3_metrics.PNG)
        
        ![Accuracy_and_Loss_Charts](https://github.com/rick2stack/Neural_Network_Charity_Analysis/blob/main/Resources/second_attempt_try3.PNG

## Summary

All models seemed to be reaching that 74%-75% accuracy threshold.  While the second and third optimization on the second model didn't show signs of major overfitting, the first optimization did show signs of overfitting.  There are times where a neural network model appears to be overfitting only to bump up to a new accuracy threshold if given enough epochs.  Another suggestion is to use a random forest reggression model since this is tabular data.  



