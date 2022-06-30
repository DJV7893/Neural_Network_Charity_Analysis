# Neural_Network_Charity_Analysis
---
## Overview:
---

For our analysis we have been tasked by Alphabet Soup's business team to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. In order to complete our analysis we will use a CSV file containing metadata from more than 34,000 organizations that received funding from Alphabet Soup over the years in order to create a deep-learning neural network with the TensorFlow platform in Python. The steps required to produce our final model involve: preprocessing the data for the neural network model, compiling, training and evaluating the model and finally optimizing the model. 

---
## Results:
---

   1. Data Preprocessing:

      - The column IS_SUCCESSFUL contains binary data classifying wether or not the charity donation was used effectively. Accordingly, this variable is           considered as the target for our deep learning neural network.
      - The columns; APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the             features for our model.
      - The columns EIN and NAME are identification information and are therefore considered neither features nor target(s) and are removed from the input         data.
      
   2. Compiling, Training, and Evaluating the Model
      
      - Our neural network model is made of two hidden layers with 80 and 30 neurons respectively. The output layer is made of a unique neuron as it's a           binary classification. To speed up the training process the activation function ReLU is used for the hidden layers. As our output is a                     binary classification, Sigmoid is used on the output layer. For the compilation, the optimizer is adam and the loss function is                             binary_crossentropy.
      - The target performance for the model was 75% but the best the model could achieve was 72.8%.
      - To try to surpass the target performance we: applied bucketing to the feature ASK_AMT and the different values were organized by intervals, We             increased the number of neurons on one of the hidden layers and then added layers to have three hidden layers and finally used a different                 activation function (tanh). In the end, none of these steps helped to push the model past the 75% threshold.

---
## Summary:
---

Our deep learning neural-network model did not reach our target performance of 75% accuracy, only reach at it's peak performance 72.8% while using various numbers of neurons, hidden layers, and different activation functions. Since our present constraints involve binary classification, we should use a supervised machine learning model specifically a Random Forest Classifier because it's less influenced by outliers and could improve our accuracy performance. With a multitude of decision tress we can generate a classified output and evaluate its performance against our deep learning model.

---

Data Source: 

Software: Jupyter Notebook 6.4.8, Python 3.7.13
