# Unit 21 Homework Report: Charity Funding Predictor

## Overview of the analysis:

The aim of this analysis is to create a model to predict if applicants funded by Alphabet Soup will be successful.


## Data Preprocessing


### What variable(s) are the target(s) for your model?

The target of the model is the "Is_Successful" variable.

### What variable(s) are the features for your model?

The feautures of the model are: "'STATUS', 'ASK_AMT',  'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'INCOME_AMT' &        'SPECIAL_CONSIDERATIONS'"

### What variable(s) should be removed from the input data because they are neither targets nor features?

The "EIN" &  "NAME" variables have been removed as we have need to identify individual datapoints. 

## Compiling, Training, and Evaluating the Model

### How many neurons, layers, and activation functions did you select for your neural network model, and why?

The initial model had 3 hidden layers with 5 units each, an input and output layer, with all having the "relu" activation function bar the output, which used "sigmoid". These were chosen as this had been used in other modelling examples. 

### What steps did you take in your attempts to increase model performance?

Initially an additional layer was added to the model, then a keras tuner funtion was used to optimise the number of neurons and layers, which was determined to be 4 layers (6,6,16&11 neurons respectively). Finally, the activation function was changed to "tahn". 

### Were you able to achieve the target model performance?

None of the model were able to reach the 75% accuarcy target. The keras tuned model was the closest with a 73.2% accuracy. Below are the results of each model:



## Summary:

Overall the deep learning was close to predicting the success rate accurately, however was not sufficient. It may be more prudent to run a linear regression model as well as a PCA to limit the number of features. This will limit the data to only the most important features and may provide a more accurate modelling.
