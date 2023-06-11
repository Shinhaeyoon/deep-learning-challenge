# Module 21 Report

## Overview of the Analysis

The analysis aims to develop a binary classifier using machine learning and neural networks to predict the success of funding applicants for the nonprofit foundation Alphabet Soup. By analyzing a dataset of over 34,000 previously funded organizations, the goal is to create a model that can accurately determine the likelihood of success for future applicants. The data is preprocessed, features are identified, and categorical variables are encoded. A neural network model is designed, trained, and evaluated to calculate loss and accuracy. The model is then optimized through various techniques to achieve a target predictive accuracy higher than 75%. The optimized model's results are saved for further analysis and application.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Data Preprocessing:
  * What variable(s) are the target(s) for your model?
  - IS_SUCCESSFUL
  
  * What variable(s) are the features for your model?
  - APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AM,SPECIAL_CONSIDERATIONS, ASK_AMT
  
  * What variable(s) should be removed from the input data because they are neither targets nor features?
  - EIN, NAME


* Compiling, Training, and Evaluating the Model:
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
  -  The model obtained from the Keras Tuner search process includes a first hidden layer with 9 neurons and a "tanh" activation function, a second hidden layer with 1 neuron and a "tanh" activation function, and an output layer with 1 neuron and a "tanh" activation function. The Keras Tuner search process systematically explores various combinations of hyperparameters to find the optimal configuration for the given problem. In this case, the tuner has identified that this particular model configuration yielded good performance, suggesting that it is well-suited for the problem at hand.

  * Were you able to achieve the target model performance?
  - The model achieved an accuracy of 0.737, falling short of the target accuracy of 0.75.

  * What steps did you take in your attempts to increase model performance?
  - Increasing the epochs during the Keras Tuner search process from 50 to 100 resulted in an improved accuracy of 0.73784. This enhancement can be attributed to several factors. First, the increased epochs allow for more iterations of weight and bias adjustments, leading to refined parameter optimization and better alignment with the training data. Second, the extended training time enables the model to better comprehend intricate or complex patterns within the data, enhancing its ability to capture and generalize from these patterns. Third, the additional epochs help overcome underfitting by allowing the model to continue learning and refining its understanding of the underlying patterns. Lastly, increasing the epochs gradually reduces the influence of bias or noise present in the training data, allowing the model to focus more on the relevant signal and improve accuracy by reducing the impact of irrelevant information.



## Summary
This report presents an analysis of a binary classifier developed to predict funding applicant success for Alphabet Soup. The dataset is preprocessed and encoded, and a neural network model is trained using the Keras Tuner search process. The optimal model configuration includes two hidden layers with "tanh" activation and achieves an accuracy of 0.737, slightly below the target of 0.75. To improve performance, the number of training epochs is increased to 100, resulting in an accuracy of 0.73784. This adjustment enhances parameter optimization, pattern recognition, and mitigates underfitting and the impact of bias or noise. Although the target accuracy is not reached, the analysis provides insights and recommendations for further improvement, such as exploring alternative architectures, adjusting hyperparameters, increasing the training dataset, and applying regularization techniques. By iteratively evaluating and optimizing the model, the desired accuracy can be achieved.