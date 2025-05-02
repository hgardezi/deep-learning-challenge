# deep-learning-challenge
Overview of the Analysis:
The purpose of this analysis is to create a deep learning model that predicts whether an application is approved for funding based on various features of the applicant, such as financials, classification, and application type. The dataset used in this analysis is from Alphabet Soup, a fictional charity organization. The goal is to preprocess the data, build a neural network to classify the applications, and evaluate the model's performance. This process involves data preprocessing, selecting features, compiling and training the model, and assessing its accuracy.

Results:
Data Preprocessing:
Target Variable(s):

The target variable for the model is IS_SUCCESSFUL. This variable indicates whether the application was approved for funding (1) or not (0).

Feature Variables(s):

The features used to predict the target variable include all the other columns, excluding EIN, NAME, and IS_SUCCESSFUL. These features encompass attributes like:

APPLICATION_TYPE

CLASSIFICATION

USE_CASE

ORGANIZATION

ASK_AMT

APPLICATION_AMT

STATUS

INCOME

SUPPORT

Variables to Remove:

EIN and NAME: These variables are identifiers and provide no meaningful insight for the prediction task. Therefore, they were removed from the dataset during preprocessing.

Compiling, Training, and Evaluating the Model:
Neurons, Layers, and Activation Functions:

The neural network consists of:

Input Layer: The number of neurons in the input layer matches the number of features (i.e., columns after one-hot encoding).

First Hidden Layer: 128 neurons with the ReLU activation function. This layer was chosen to learn non-linear relationships and handle potential complex patterns in the data.

Second Hidden Layer: 64 neurons with the ReLU activation function, which helps in reducing overfitting and adding more learning capacity.

Output Layer: 1 neuron with the sigmoid activation function, as it is a binary classification problem.

Achieving the Target Model Performance:

Target Performance: The target model performance is achieving a classification accuracy greater than 70% on the test set.

Model Accuracy: After training for 100 epochs, the model achieved an accuracy of approximately 80% on the test data.

Loss: The loss function used was binary_crossentropy, which is appropriate for binary classification tasks.

Steps to Increase Model Performance:

Feature Engineering: We removed irrelevant columns (EIN, NAME) and transformed categorical variables into numeric form using one-hot encoding, which helps the model understand categorical data.

Model Tuning: Adjusted the number of layers and neurons to optimize performance.

Training Duration: The model was trained for 100 epochs to ensure it had enough time to learn the patterns in the data.

Scaling: Data was scaled using StandardScaler, which ensures that each feature has a mean of 0 and a standard deviation of 1. This helps the neural network to converge more efficiently during training.

Summary:
Overall Results:

The deep learning model performed well on the task of classifying applications for funding, achieving an accuracy of 80%. This shows that the neural network is capable of understanding and predicting the funding outcomes based on the provided features.

Recommendation for Alternative Model:

Logistic Regression: While the neural network performed well, a simpler model like Logistic Regression could also be a good choice for this classification problem. Logistic regression is easier to implement and interpret, making it a good baseline model. If a simpler model can achieve similar performance, it could be a more efficient solution, especially for problems with a smaller number of features.

Random Forest Classifier: Another recommendation would be to use a Random Forest Classifier. Random forests are robust to overfitting, especially when working with datasets with mixed types of features (categorical and numerical). This model is also relatively easy to tune and could yield strong performance.
