# Implied-Volatality-prediction-using-Deep-Learning
This repository contains the code and resources for predicting changes in implied volatility using a deep learning model. The project leverages a dataset containing SPX Return, Time to Maturity in Year, and Delta as features to train a ReLU-based deep neural network. 


Here's a detailed description for your GitHub README file that includes information about options, implied volatility, the Black-Scholes model, and the methodology used in this project:

---

## Overview
This repository contains the code and resources for predicting changes in implied volatility using a deep learning model. The project leverages a dataset containing SPX Return, Time to Maturity in Year, and Delta as features to train a ReLU-based deep neural network. The aim is to accurately predict the implied volatility change, which is crucial in financial markets for options pricing.

## Table of Contents
- [Overview](#overview)
- [Options and Implied Volatility](#options-and-implied-volatility)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Acknowledgments](#acknowledgments)

## Options and Implied Volatility
### Options
Options are financial derivatives that provide the buyer the right, but not the obligation, to buy or sell an asset at a predetermined price before or at the expiration date. There are two main types of options:
- **Call Options**: Give the holder the right to buy an asset.
- **Put Options**: Give the holder the right to sell an asset.

### Implied Volatility
Implied volatility (IV) is a measure of the market's forecast of a likely movement in an asset's price. It is derived from the price of an option and reflects the market's view of the future volatility of the underlying asset. Higher implied volatility indicates that the market expects significant price movements, while lower implied volatility suggests more stability.

### Calculating Implied Volatility using the Black-Scholes Model
The Black-Scholes model is a mathematical model used for pricing European-style options. The formula requires several inputs: the current price of the underlying asset, the strike price of the option, the time to expiration, the risk-free interest rate, and the volatility of the underlying asset.

The Black-Scholes formula is given by:
![image](https://github.com/user-attachments/assets/053340ce-0d26-48d0-b5de-d4b2b1befa9e)


Implied volatility is not directly observed but is derived by inverting the Black-Scholes formula. This involves finding the volatility (\( \sigma \)) that, when input into the formula, returns the market price of the option.

### Methodology in This Project
In this project, we predict changes in implied volatility using a deep learning approach. The dataset includes features such as SPX Return, Time to Maturity in Year, and Delta. The following steps outline the process:

1. **Data Preparation**: Load the dataset, create feature columns, and split the data into training and test sets.
2. **Feature Scaling**: Standardize the features using Z-Score scaling.
3. **Model Building**: Use the `piml` library to build and train a ReLU-based deep neural network.
4. **Model Evaluation**: Evaluate the model's performance using metrics like Mean Squared Error (MSE).
5. **Visualization**: Visualize the model architecture and network diagram using TensorFlow, Keras, and Graphviz.

![image](https://github.com/user-attachments/assets/c05c7fa9-a85c-415c-a9ee-75408fa242cf)
The plot you’ve shared is a SHAP (SHapley Additive exPlanations) summary plot, which provides insights into the impact of each feature on the model’s output. SHAP values are a method to explain the output of machine learning models by attributing the contribution of each feature to the prediction.

![image](https://github.com/user-attachments/assets/a394c84d-44b4-4209-a4e0-1f202c8cfdc1)
Model Structure







## Results
- **Mean Squared Error**: The MSE metric is used to evaluate the model's performance on the test set.
- ![image](https://github.com/user-attachments/assets/a6a23534-d21d-4670-a726-597bdf409c64)

- **Model Architecture and Network Diagram**: Visualizations provide insights into the structure and connections of the deep learning model.

## Conclusion
This project demonstrates the process of building, training, and evaluating a deep learning model for predicting implied volatility changes. The approach includes comprehensive steps from data preparation to model diagnostics and visualization, providing a robust framework for financial predictions.

## Future Work
- Experiment with different model architectures and hyperparameters.
- Implement cross-validation for more robust model evaluation.
- Explore additional features that could improve prediction accuracy.

## Acknowledgments
Thanks to the open-source community for providing the tools and libraries used in this project.

---

This README file provides a comprehensive overview of the project, including essential background information on options and implied volatility, as well as detailed steps and code for data preparation, model building, evaluation, and visualization.
