# deep-learning-challenge

In this challenge, we were tasked with helping a nonprofit, Alphabet Soup, with developing a tool they can use to select applicants for business funding based on their chances of being successful. We were given a dataset of 34,000 of businesses that were previously awarded funding. The dataset contained various information about the data including a column indicating whether the business was successful or not. We usdd this dataset to built a deep neural network model to predict whether applicants for business funding will be successful. 

## Preprocessing the Data

First, we preprocessed the data following these steps:
    
    1. Determine the number of unique values in each column.
    
    2. If any column contained more than 10 unique values, binning was used to group the rare values into an "Other" category. 
    
    3. Use the pd.get_dummies function to convert categorical values into numerical values. 
    
    4. Determine our target and features columns:
    
        -The EIN and Name columns were dropped because they are only used for identification purposes
 
        -The IS_SUCESSFUL column was used as the target 
        
        -The rest of the columns were used as features
  
    5. Split the data into training and testing datasets 
    
    6. Used scikit-learn's StandardScaler() to scale the data.

![image](https://github.com/maiayang/deep-learning-challenge/assets/145394264/21c32c33-5d42-4e57-b357-511b1ea36ebb)
![image](https://github.com/maiayang/deep-learning-challenge/assets/145394264/c2bbdfe6-f5ef-40c0-9c80-14e7edc5f3bd)


## Compile, train, and evaluate the model

Before we compiled the model, we defined the model by creating an instance of it and adding each hidden layer. For our first attempt, we used the following structure:
   
    -Two hidden layers, the first with 8 nodes, the second with 5 nodes
    
    -Hidden activation functions were set to Relu
    
    -Last layer activation function was set to Sigmoid because the outcome is binary

Next we compiled and trained the model using 100 epochs. We achieved a model loss of 0.55 and accuracy score of 0.73.

![image](https://github.com/maiayang/deep-learning-challenge/assets/145394264/c91620b1-b1ec-4dd8-84d0-2ee5ded68b04)
![image](https://github.com/maiayang/deep-learning-challenge/assets/145394264/be2c51f0-872d-4833-8a00-af00fac3e57b)


## Optimization

To try to achieve our target accuracy score of .75, we made three subsequent attempts to optimize the model (see separate Jupyter Notebook).

In the first optimization attempt, we added a third hidden layer and increased the number of nodes in the first, second, and third hidden layers to 80, 50, and 30 respectively. In the second optimization attempt, we changed the activation functions for the hidden layers to the tanh function.  In the third optimization attempt, we increased the number of epochs to 200. In all cases we were not able to achieve an accuracy score higher than the first model.

## Summary

We attempted to develop a machine learning tool that would help Alphabet Soup select applicants for business funding using data from previous awardees. We were not able to achieve an accuracy score of higher than .73, so we can conclude that the dataset is perhaps lacking some fundamental variables that contribute to the success of a business. Some examples of additional information to collect for future analyses include:
   
    -Education level of Founder/CEO
    
    -Geographical information
    
    -Length of time business has been in operation

Sources for code:

https://machinelearningmastery.com/save-load-keras-deep-learning-models/
