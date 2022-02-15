# Neural_Network_Charity_Analysis

## Overview of the analysis:

The purpose of this analysis is to create a binary classifier in order to predict whether applicants will be successful if funded by Alphabet Soup. The gathered data cleaned, trained and evaluated based on the points provided using Neural Network Model to assess how likely a business is to successfully use the funding.

## Results:

### Data Preprocessing:

Upon reading charity_data.csv preprocessing consisted of dropping columns "EIN" and "NAME" as these do not contain added values for the analysis. Columns "APPLICATION_TYPE" and "CLASSIFICATION" are dissected to determine the number of unique values held in each columns and then is consolidated to bucket the single or less frequent occurring items. 

Using the OneHotEncoder the "APPLICATION_TYPE" is broken down to unique columns which are then classified using the binary classification in order for the Neural Network model analysis. 

Initially the model was created with two layers, the first layer contained 8 neurons and the second layer contained 3 neurons, model was ran using a 50 epoch interval. This yielded a 51.3% accuracy score. 

![](https://github.com/LMarty22/Neural_Network_Charity_Analysis/blob/main/Images/Initial_Attempt_ASC.png)

In the goal to optimize the accuracy score the first model was ran using three layers. First layer contained 12 neurons, second layer contained 7 neurons and the third layer containing 7 neurons. This yielded a 67.3% accuracy score. 

![](https://github.com/LMarty22/Neural_Network_Charity_Analysis/blob/main/Images/First_Attempt_Optimization.png)

Second attempt was ran using two layers, first and second layers containing 11 neurons each. This yielded a 70% accuracy score.

![](https://github.com/LMarty22/Neural_Network_Charity_Analysis/blob/main/Images/Second_Attempt_Optimization.png)

Third attempt was ran using two layers, first layer containing 11 neurons and the second containing 17 neurons, and "INCOME_AMT" column was dropped prior to analysis. This yielded a 53.5% accuracy score.
![](https://github.com/LMarty22/Neural_Network_Charity_Analysis/blob/main/Images/Third_Attempt_Optimization.png)

## Summary: 

The deep learning neural network model was not successful at achieving 75% accuracy. The following methods were attempted: 

- Adding neurons to hidden layers.
- Adding additional hidden layers.
- Removing other non influential columns in the original data set.

Another model which should be considered is the Random Forest Classifier per its ease of setting up code. The two models could be similar in the accuracy results they yield, but Random Forest Model would be more time efficient in setting up.
