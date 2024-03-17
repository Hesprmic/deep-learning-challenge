# deep-learning-challenge

For this homework challenge we were tasked with utilizing Machine Learning to compile, train, evaluate, and finally optimize the model for the Alphabet Soup Charity data using Keras and Tenserflow.

Results:

Data Preprocessing

The column named "IS_SUCCESSFUL" is target of this model (dependent variable)
Different feature variables were used to understand their effects on the loss/accuracy.
For all optimization attempts "EIN" and "NAME" variables were removed.

Compiling, Training and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
See below for individual attempts.

Were you able to achieve the target model performance?
No, the original neural network model could not achieve the target model performance which was 75%. The accuracy of this model was approximately 73% and the loss was 55.0%.

What steps did you take in your attempts to increase model performance? Adjusted different optimizers, layers, neurons.

Six different attempts were run in order to try to optimize the model:

* Attempt #1 To start, two hidden layers (relu for the 1st activation and sigmoid for the 2nd hidden layer) were used along with lower inputs (15 for the first and 10 for the second). All attempts used 100 epochs and a loss using binary crossentropy. This attempt yielded 72.8% accuracy and 55.1% loss.

* Attempt #2 In this attempt, the 2nd hidden layer was changed from sigmoid to relu. The input numbers were changed from 80 and 32 for the first and second layers respectively. This attempt yielded 72.7% accuracy and 55.6% loss.

* Attempt #3 Next this attempt had another hidden layer added making the 3rd layer a sigmoid. The inputs were changed for the first hidden layer to 48 and the 3rd layer was set to 8. This attempt yielded 72.7% accuracy and 55.2% loss.

* Attempt #4 This attempt yielded the lowest loss of the six tries (see below). Changes made to this one were the inputs increased to 128 for the 1st hidden layer, 64 for the 2nd layer, and 32 for the 3rd. The other major change for this attempt was the Optimizer was changed from adam to SGD(Stochastic Gradient Descent). The accuracy from 72.7% to and the loss decreased from 55.2% to 55.0%.

  ![image](https://github.com/Hesprmic/deep-learning-challenge/assets/144865763/17f8cdbd-c0a4-4ff7-847f-abbce5444f16)


* Attempt #5 This attempt yielded the highest accuracy of the six tries (see below). The hidden layer input numbers were changed again to 48, 32, 16 respectively through the three hidden layers. The biggest change came in the form of switching the optimizer, this time to RMSprop. The accuracy from 73% to and the loss was 55.3%.

![image](https://github.com/Hesprmic/deep-learning-challenge/assets/144865763/62505d0c-ab38-489d-9344-f393dbc0bcc1)


* Attempt #6 In the final attempt, the only change from the previous attempt was a change of the 3rd hidden layer from sigmoid to relu. This last attempt has 72.8% accuracy and 56.4% loss.

Summary:
None of six optimization attempts had achieved increase in accuracy enough to reach the target performance. Overall, the deep learning model achieved a moderate accuracy of around 73%. To potentially improve the classification performance, I would recommend exploring the following:

Ensemble methods such as Random Forests or Gradient Boosting Machines could be explored. These methods often perform well with tabular data and can capture complex relationships between features.

Hyperparameter Tuning: Utilize techniques like grid search or random search to systematically explore different hyperparameter configurations and find the optimal combination for improved performance.

Feature Engineering: Feature engineering can be crucial for improving model performance. Analyze the data further to create new features or transform existing ones to better represent patterns in the data.

Model Interpretability: Consider using interpretable models like decision trees or logistic regression, which offer transparency and insights into the decision-making process, especially if model interpretability is important for the application.
By employing these strategies and potentially exploring different types of models, it's possible to achieve better performance in the classification problem.

Note: Tyler helped with a fair amount of the preprocessing coding. I also did research on Keras.io to get other optimizers. The improvement ideas came from a variety of websites and youtube videos.
