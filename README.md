# deep-learning-challenge

In this challenge, we used a deep neural network model to predict whether applicants for business funding will be successful. The dataset we used contained information about 34,000 organizations with an outcome column indicating whether the business was successful or not.

First, we preprocessed the data by determining the number of unique values in each column. If any column contained more than 10 unique values, binning was used to group the rare values into an "Other" category. Then we used the pd.get_dummies function to convert categorical values into numerical values. Lastly, we split the data into training and testing datasets and used the StandardScaler to scale the data.

Next, we defined the model by determining the number of hidden layers along with the number of nodes and input dimensions for each layer. We instantiated the model and added each hidden layer to the model with our activation function of choice. We used a sigmoid activation function for the last layer because the outcome is binary.

The last step was to compile, train, and evaluate the model. The number of epochs for training was set to 100. The model loss and model accuracy were computed. We saved the model to an .h5 file.

Sources for code:

https://machinelearningmastery.com/save-load-keras-deep-learning-models/