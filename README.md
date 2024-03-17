# deep-learning-challenge

For this homework challenge we were tasked with utilizing Machine Learning to compile, train, evaluate, and finally optimize the model for the Alphabet Soup Charity data using Keras and Tenserflow.

Results:
Data Preprocessing
The column named "IS_SUCCESSFUL" is target of this model (dependent variable)
During optimization attempts, different feature sets were used to understand their effects on the loss/accuracy.
For all optimization attempts "EIN" and "NAME" variables were removed.
Compiling, Training and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
Main neural network model has contained two hidden layers with 80 and 30 neurons respectively. The hidden layes used "relu"activation function while the output layer used 'sigmoid'activation function. In this analysis, the epochs number was 100.

Were you able to achieve the target model performance?
The original neural network model could not achieve the target model performance which is 75%. The accuracy of this model was approximately 73% and the loss was 56%.

What steps did you take in your attempts to increase model performance?

Six different attempts were run in order to try to optimize the model:

* Attempt #1 To start, two hidden layers were used along with lower input

* Attempt #2 In this attempt, number of epoches was increased to 150 from 100.The new hidden layer that was added in attempt 1 stayed same. After change in the epoch numbers, the accuracy level stayed same (73%) while loss level increase (58%).

* Attempt #3 

* Attempt #4

* Attempt #5

* Attempt #6 In the final attempt,  This new model has 72.8% accuracy and 56.6% loss.

Summary:
None of three optimization attempts had acieved increase in accuracy, instead they were cause to increase in loss. Since there are a lot of categorical data in our dataset, may be trying decision tree or random forrest methods will work better.
