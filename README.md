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
do a overview of the preprocessing
- What variable(s) are considered the target(s) for your model?
- What variable(s) are considered to be the features for your model?
- What variable(s) are neither targets nor features, and should be removed from the input data?

### Compiling, Training, and Evaluating the Model
overview of CPE

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
- Were you able to achieve the target model performance?
- What steps did you take to try and increase model performance?

Initial output of model:
![fig1](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/initial.png)

Optimization Attempt 1: increased neurons
![fig2](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt_1_relu_neurons.png)

Attempt 2: added an extra layer = did not work, decreased
![fig3](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt2_added_layer.png)

Attempt 3: change function to tanh
![fig4](https://github.com/retroxsky06/Neural_Network_Charity_Analysis/blob/main/images/attempt3_tanh.png)

## Summary
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.



