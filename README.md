# Neural Network Charity Analysis

## Project Overview
The purpose of this project is to apply a Neural Network Machine Learning Model to create a binary classifier that is capable of predicting whether applicants will be successful if funded by a fictional company, "Alphabet Soup."  A csv dataset is preprocessed, compiled, trained, and evaluated.  Lastly, several attempts are made to optimize the model in hopes to increase the accuracy to 75% or higher.

### Software & Resources
- Python
- Jupyter Notebook
- Libraries: Scikit-learn, TensorFlow, Pandas
- Data: [charity_data.csv](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv)

## Results

Results: Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
Prior to analysis, the csv dataset is first read into a Pandas DataFrame and then cleaned and transformed. The preprocessing method includes:   
1) Dropping the columns 'EIN' and 'NAME' as they do not contain any valuable information.
2) Binning the columns, 'CLASSIFICATION' and 'APPLICATION_TYPE' as they have more than 10 uniqiue values (rare categorical data points) into a new column, 'Other.'
3) Generating a list of categorical variables and encoding the list using OneHotEncoder; then storing encoded variables in a new DataFrame.
4) Finally, merging the one-hot encoded DataFrame with the orifinal DataFrame and dropping the originals.

**Features & Target for the model:**
The variable considered the **target** for the model is 'IS_SUCCESSFUL.'  The remaining colmumns in the DataFrame are considered the **features.**

**Neither targets or features:**
The variables that were not considered to be either features or targets are 'ID' and 'EIN,' as they did not contain any valuable information for the neural netwrok algorithm.

### Compiling, Training, and Evaluating the Model
After preprocessing the data, a neural network model is designed to create a binary classification model that can predict if an "Alphabet Soup" funded organization will be successful based on the features in the dataset. 

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
- Were you able to achieve the target model performance?
- What steps did you take to try and increase model performance?

**Initial output of model:**

![fig1](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/initial.png)
- For the initial iteration of the model, two hidden layers were applied with 80 neurons in the first, while 6 in the second. A Rectified Linear Unit (ReLU) is used as the activation function for both the first and second hidden layers, while Sigmoid is used as the outer layer activation function.  

**Optimization Attempt 1: Increased neurons**

![fig2](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt_1_relu_neurons.png)
- 
**Optimization Attempt 2: Added a third hidden layer**

![fig3](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt2_added_layer.png)

**Attempt 3: Changed function to tanh**

![fig4](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt3_tanh.png)

## Summary
Through several optimization trials, none of the attempts were able to produce a model with a predictive accuracy of 75% or higher.

Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.



