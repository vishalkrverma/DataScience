-```
Artificial Intelligence:A machine or system capable of making decisions and performing tasks in a manner similar to human intelligence.

How is AI made ?
By training/teaching the machine.

The process of training /teaching to machine to make it intelligent is known as Machine learning.

Ways to Trend the Machine:
Supervised:Labelled Data(Input and Output data are defined)
Unsupervised:Only data is Given but no label...(Output is not defined)..
Reinforecement:No initial data or Labelled..(Learning with their past experiences).
Semi-Supervised:Combination of Un-Supervised + Reinenforcement

This is called the semi-supervised because its learns from feedback and the first the output are defined then we give the feedback that why it is known as semi-supervised.
Reinforcement learning is based on the Rewards and Penality..

WHy should we do Predictive analysis after the Descriptive and Prescriptive..?

✅ The Two Main Types of Predictive Analysis:
1. Regression (Regressive Prediction)
Definition: Predicts continuous numeric values.
Output: Real numbers (not random integers, but values that can range across a spectrum).
Example: Predicting the price of a house, temperature, or someone's salary based on input features.

➤ Correct interpretation:
"Regression predicts continuous values (not necessarily random integers)."
2. Classification (Classified Prediction)
Definition: Predicts categorical labels.
Output: Discrete categories (e.g., class A, B, or C).

Example: Spam vs. Not Spam, predicting if a patient has a disease (Yes/No), or recognizing digits in an image (0–9).

➤ Correct interpretation:
"Classification predicts categories or classes, not numeric values.".

                                       Supervised Learning
                                     /                    \
                               Regression                  SVM(Support Vector Machine)
                               /         \                         /           \
                         Linear       Logistic

Regression:Both input and output are numerical in nature  and  the values must be continuos.
Liner Regression : Car Price Prediction    House Price Prediction         Marks Predictions    Salary Prediction      Stock Price Prediction(Time Series Algorithm are used)

Logistic Classification : Binary Classification of the data fist converted into the numeric form (0,1) and then applied on the algorithm.
Logistic Regression is a statistical algorithm used for binary classification — i.e., it predicts one of two possible outcomes.

🔢 How It Works:
Input Features: The input data (which may include text, categories, etc.) is preprocessed and converted into numeric form.

Example: "Yes" = 1, "No" = 0

Categorical features may be one-hot encoded or label encoded.
Prediction Output: The algorithm calculates the probability that a given input belongs to a class (e.g., 1 or 0).
Output is a value between 0 and 1.

This is done using the sigmoid function: 
Decision Rule: Based on the output probability:
If probability ≥ 0.5 → class 1
If probability < 0.5 → class 0


LINEAR REGRESSION:
📌 Definition:
Linear Regression is a supervised machine learning algorithm used to predict a continuous numeric value based on the relationship between input (independent) variables and output (dependent) variable.
It assumes that there is a linear relationship between the inputs and the output.
y=mx+b

y: Predicted value/Labelled (dependent variable)

𝑥: Feature (independent variable)
M: Coefficients/weights
b: Bias/intercept

The model finds the best-fitting line by minimizing error (usually using Mean Squared Error)

FEATURES---> INPUT COLUMN
TARGET COLUMN -->OUTPUT


PROCESS FOR CODING:
Import libraires
Load DataSet
Understanding Requirement
Select Algorightm
Import Modules related to the Algorithm
Data Visualization.
Data Evaluation.
Preprocess and Prepare the data.
Feature Selection
Data Division(Trainig and Testing)
Model Preparation/Training
Model Fitting.
Model Evaluation.
Model Prediction.

                          DATA  VALIDATION
                        /                  \
              Train Test Split          Cross Validation

The Ratio of the Training and Testing of the Data are Generally in 7:3 .

Cross Validation is Used When data amount is less and are being used to complex algorithm.

              


How to Select the column to determine the which are features and which are Labelled..
By using the co-relation which helps to determine the which column will show the relations..

What is Collinearity ?


