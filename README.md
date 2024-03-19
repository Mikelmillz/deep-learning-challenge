# deep-learning-challenge
Module 21 Challenge Due Tuesday 3/19 by 11:59pm


# **Report on the Neural Network Model**

## **Overview:**

-The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With my knowledge of machine learning and neural networks, I’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## **Results:**

### Data Preprocessing

-The columns 'EIN' and 'NAME' were dropped.  

-The column 'IS_SUCCESSFUL'; this feature is the one that is going to be predicted and determine the success rate of the data.  

-'pd.get_dummies()' is how it was encoded for the categorical variables.  

-The columns 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT' are feature values for this activity. We had the option to remove one of these columns to get a higher accuracy but I opted to change other things instead.  

### Compiling, Training, and Evaluating the Model

-Model Evaluation 1

![image](https://github.com/Mikelmillz/deep-learning-challenge/assets/145722846/49d0e0a9-5c53-4414-924b-f011579f1650)
![image](https://github.com/Mikelmillz/deep-learning-challenge/assets/145722846/1c93dba6-be77-44cb-9804-ae88b55b2194)



The attempt at compiling a neural network consisted of layers of 80 neurons and the second one of 30. Both layers had relu activation functions. In addition, the output layer had a sigmoid activation function. The assembled model had the Adam optimization algorithm, and the fitting model had a validation split of 0.15 and 100 epochs.
The results for this model were:
Loss: 0.5701
Accuracy: 0.7284

-Model Evaluation 2

![image](https://github.com/Mikelmillz/deep-learning-challenge/assets/145722846/16c5beec-99a6-4985-8215-fe5fd8de248a)
![image](https://github.com/Mikelmillz/deep-learning-challenge/assets/145722846/506e3924-8c05-444d-bffe-2298a5792bf6)



This attempt at compiling a neural network consisted of layers of 80 neurons, the second one of 30 and I added a third one of 10. I swapped the activation and had the first layer be sigmoid and the second, third, and activation of relu. The assembled model had the Adam optimization algorithm, and the fitting model had a validation split of 0.15 and 100 epochs.
Loss: 0.5684
Accuracy: 0.7285

-Model Evaluation 3

![image](https://github.com/Mikelmillz/deep-learning-challenge/assets/145722846/670a081c-4d95-4ed5-9aaf-20a9501e500d)
![image](https://github.com/Mikelmillz/deep-learning-challenge/assets/145722846/3747766f-0262-4ac9-b17a-9004dceb40e0)



This attempt at compiling a neural network consisted of those same 3 layers but with all neurons at 50. All layers had different activation functions. The first had sigmoid, second had relu, third had tanh and the activation had elu. The assembled model had the Adam optimization algorithm, and the fitting model had a validation split of 0.15 and 100 epochs.
Loss: 0.5730
Accuracy: 0.7254

## **Summary:**

Unfortunately I did not find a model with an accuracy of 75 percent, so I went with the other method of showing three different attempts. They were all close, around 72 percent though. They all lost around 57% as well.

I believe if I played around with adding/subtracting features and finding a better number for the bins, I could have gotten above 75 percent as I mainly changed the activations and then added another hidden layer.
