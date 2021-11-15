# Neural Network Charity Analysis

## Project Overview
The purpose of this project is to apply a Neural Network Deep Learning Model to create a binary classifier that is capable of predicting whether applicants will be successful if funded by a fictional company, "Alphabet Soup."  A csv dataset is preprocessed, compiled, trained, and evaluated.  Lastly, several attempts are made to optimize the model in hopes to increase the accuracy to 75% or higher.

### Software & Resources
- Python
- Jupyter Notebook
- Libraries: Scikit-learn, TensorFlow, Pandas
- Data: [charity_data.csv](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv)

## Results
### Data Preprocessing
Prior to analysis, the csv dataset is first read into a Pandas DataFrame and then cleaned and transformed. The preprocessing method includes:   
1) Dropping the columns 'EIN' and 'NAME' as they do not contain any valuable information.
2) Binning the columns, 'CLASSIFICATION' and 'APPLICATION_TYPE' as they have more than 10 uniqiue values (rare categorical data points) into a new column, 'Other.'
3) Generating a list of categorical variables and encoding the list using OneHotEncoder; then storing encoded variables in a new DataFrame.
4) Finally, merging the one-hot encoded DataFrame with the orifinal DataFrame and dropping the originals.

**Features & Target for the model:**
The variable considered the **target** for the model is 'IS_SUCCESSFUL.'  The remaining colmumns in the DataFrame are considered the **features.**

**Neither targets or features:**
The variables that were not considered to be either features or targets are 'ID' and 'EIN,' as they did not contain any valuable information for the neural network algorithm.

### Compiling, Training, and Evaluating the Model
After preprocessing the data, a neural network model is designed to create a binary classification model that can predict if an "Alphabet Soup" funded organization will be successful based on the features in the dataset. 

**Initial output of model:**

![fig1](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/initial.png)
For the initial iteration of the model, two hidden layers were applied with 8 neurons in the first layer, while 6 were selected in the second. A Rectified Linear Unit (ReLU) is used as the activation function for both the first and second hidden layers, while Sigmoid is used as the outer layer activation function.  
Although a predictive accuracy of 72.6% is achieved, we would like to optimize our model using TensorFlow to attain a target predictive accuracy of 75% or higher.  Results of four attempts made are displayed below.

**Optimization Attempt 1: Increased neurons**

![fig2](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt_1_relu_neurons.png)
The first attempt to optimize the model was to increase the neurons in the hidden layers, with 15 applied to the first layer, and 10 to the second. This had a positive affect as the accuracy became 72.7%; however it did not meet the 75% or higher goal.

**Optimization Attempt 2: Added a third hidden layer**

![fig3](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt2_added_layer.png)
The second attempt to optimize the model was to add a third layer with 10 neurons, while retaining the first attempt neurons (15 and 10). This change reduced the model's accuracy to 72.3%. Due to the negative effect of this added layer, it was removed from the model.

**Attempt 3: Changed function to tanh**

![fig4](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt3_tanh.png)
The third attempt to optimize the model was to change the second layer's activation function to 'tanh,' while retaining the first attempt neurons (15 and 10). The predictive accuracy rate was 72.5%. 

**Optimization Attempt 4: Increase neurons from Attempt 1**

![fig4](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt4.png)
The first attempt to optimize the model seemed promising as there was a slight increase from the initial iteration. To further explore if increased neurons would be a favorable change to the model, a fourth attempt was made by increasing the two hidden layers, with 80 applied to the first layer, and 60 applied to the second. The significant increase of neurons on both hidden layers decreased the predictive accuracy to 72.5%.

## Summary
Through several optimization trials, none of the attempts were able to produce a model with a predictive accuracy of 75% or higher.  A variety of reasons may be occurring as to why the model did not achieve the 75% or higher goal, which may include the epochs needing to be changed during the training phase, the input data may harbor outliers that are causing confusion in the model, and/or the activation functions need to be altered. Additionally, a different model may be utilized, such as a Random Forest Classifier, that can hold complex data while being much simpler to build and train.  


