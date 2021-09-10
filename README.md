# Neural Network Charity Analysis

## Overview of the analysis

This analysis will use a neural network to provide Alphabet Soup with a binary classifier that will predict whether applicants will be successful if given funding.

## Results

#### Data Preprocessing
- The main target variable for this model is within the "IS_SUCCESSFUL" column of the dataset.
- All other columns were used as features for the model. The "CLASSIFICATION" and "APPLICATION_TYPE" columns were identified as having numerous unique values, and the least frequently occurring ones were binned as "Other." 
- The "EIN" and "NAME" columns were identified as not having valuable information to the classifications, and the columns were removed.

#### Compiling, Training, and Evaluating the Model
- Initially, two hidden layers were usesd for the model. The first layer used 80 neurons and the second used 30. Both layers used the relu function (screenshot below).</br>
    ![Alt Text](https://github.com/lyanneagger/Neural_Network_Charity_Analysis/blob/main/Resources/OptAtt1.png "First Optimization Attempt")</br>
- The initial model and all three subsequent optimization attempts were unable to achieve the target model performance.
- Three optimization attempts were made: 
    -  In the first optimization attempt, the number of neurons in each layer was increased, which increased accuracy from 47.6% with the initial model to 66.1%.</br>
    -![Alt Text](https://github.com/lyanneagger/Neural_Network_Charity_Analysis/blob/main/Resources/OptAtt1_results.png "Results for First Optimization Attempt")</br>
    -  The second optimization attempt added an additional layer, which reduced the accuracy to 53.6%. 
    -  The third optimization attempt removed the third layer and changed the activation function of the second layer from relu to tanh, which further decreased the accuracy to 49.2%.

## Summary

The initial optimization attempt achieved the most accurate results at 66.1%. Further increasing neurons within those two layers may yield improved results. Additionally, the dataset may contain potentially noisy variables. An attempt at removing some of the noisy data may produce more accurate results as well.