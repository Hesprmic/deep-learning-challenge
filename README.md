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
The original neural network model could not achieve the target model performance which is 75%. The accuracy of this model was approximately 73% and the loss was 56% 55.2%.

What steps did you take in your attempts to increase model performance?

Six different attempts were run in order to try to optimize the model:

* Attempt #1 To start, two hidden layers (relu for the 1st activation and sigmoid for the 2nd hidden layer) were used along with lower inputs (15 for the first and 10 for the second). All attempts used 100 epochs

* Attempt #2 In this attempt, number of epoches was increased to 150 from 100.The new hidden layer that was added in attempt 1 stayed same. After change in the epoch numbers, the accuracy level stayed same (73%) while loss level increase (58%).

* Attempt #3 

* Attempt #4 This attempt yielded the lowest loss of the six tries (see below). Changes made to this one were the inputs increased to 128 for the 1st hidden layer, 64 for the 2nd layer, and 32 for the 3rd. The other major change for this attempt was the Optimizer was changed from adam to SGD(Stochastic Gradient Descent). The accuracy from 72.7% to and the loss decreased from 55.6% to 55.2%.

  ![image](https://github.com/Hesprmic/deep-learning-challenge/assets/144865763/17f8cdbd-c0a4-4ff7-847f-abbce5444f16)


* Attempt #5 This attempt yielded the highest accuracy of the six tries (see below). The hidden layer input numbers were changed again to 48, 32, 16 respectively through the three hidden layers. The biggest change came in the form of switching the optimizer, this time to RMSprop.

![image](https://github.com/Hesprmic/deep-learning-challenge/assets/144865763/62505d0c-ab38-489d-9344-f393dbc0bcc1)


* Attempt #6 In the final attempt, the only change from the previous attempt was a change of the 3rd hidden layer from sigmoid to relu. This new attempt has 72.8% accuracy and 56.4% loss.

Summary:
None of six optimization attempts had achieved increase in accuracy, instead they were cause to increase in loss. Overall, the deep learning model achieved a moderate accuracy of around 72.79%. To potentially improve the classification performance, I would recommend exploring the following:

Ensemble methods such as Random Forests or Gradient Boosting Machines could be explored. These methods often perform well with tabular data and can capture complex relationships between features.

Hyperparameter Tuning: Utilize techniques like grid search or random search to systematically explore different hyperparameter configurations and find the optimal combination for improved performance.

Feature Engineering: Feature engineering can be crucial for improving model performance. Analyze the data further to create new features or transform existing ones to better represent patterns in the data.

Model Interpretability: Consider using interpretable models like decision trees or logistic regression, which offer transparency and insights into the decision-making process, especially if model interpretability is important for the application.
By employing these strategies and potentially exploring different types of models, it's possible to achieve better performance in the classification problem.

Note: Tyler helped with a fair amount of the preprocessing coding. I also did research on Keras.io to get other optimizers. 
