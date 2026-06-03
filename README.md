# Linear Regression from Scratch

[![Python 3.x](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Required-green.svg)](https://numpy.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains a lightweight educational implementation of **Simple Linear Regression** built completely from scratch using **NumPy**.

The goal of this project is to demonstrate how linear regression works under the hood, without relying on machine learning frameworks such as Scikit-Learn. It also shows how model parameters can be optimized using **Gradient Descent**.

---

## Overview

Linear regression is one of the most fundamental algorithms in machine learning. It models the relationship between an input variable \(x\) and an output variable \(y\) using a straight line:

$$
\hat{y} = ax + b
$$

Where:
- \(a\) is the slope
- \(b\) is the intercept
- \(\hat{y}\) is the predicted value

In this project, the model learns the best values of \(a\) and \(b\) by minimizing the prediction error.

---

## Features

- **From-scratch implementation** of simple linear regression
- **Gradient Descent optimization** for parameter learning
- **Custom evaluation metrics** including:
  - Mean Squared Error (MSE)
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - \(R^2\) Score
- **Normalization function** for feature scaling
- **Notebook-based workflow** for interactive experimentation

---

## Mathematical Background

The model used in this project is:

$$
\hat{y} = ax + b
$$

To train the model, the **Mean Squared Error (MSE)** is used as the loss function:

$$
MSE = \frac{1}{n} \sum_{i=1}^{n}(y_i - \hat{y}_i)^2
$$

The parameters are updated using gradient descent:

$$
a := a - \alpha \frac{\partial MSE}{\partial a}
$$

$$
b := b - \alpha \frac{\partial MSE}{\partial b}
$$

where \(\alpha\) is the learning rate.

---

## Code Structure

The notebook contains the following main parts:

### 1. Data Definition
A small test dataset is created manually using NumPy arrays.

### 2. Prediction Function
The `y_hat(x, a, b)` function generates predictions using the linear equation.

### 3. Evaluation Functions
The notebook includes functions for:
- `mse`
- `mae`
- `rmse`
- `r2_score`

### 4. Normalization
A custom `normalization(x)` function is included to standardize values.

### 5. Training Loop
A gradient descent loop updates the parameters `a` and `b` over multiple iterations and stores the MSE values in a list called `data`.

---

## How It Works

The training process follows these steps:

1. Initialize the parameters `a` and `b`
2. Predict outputs using the current line
3. Compute the error between predictions and true values
4. Calculate gradients for both parameters
5. Update the parameters using gradient descent
6. Repeat for a fixed number of iterations

After training, the list `data` contains the MSE values across epochs, which can be used to analyze convergence.

---

## Requirements

Install NumPy before running the notebook:

```bash
pip install numpy
```

---

## Usage

1. Clone or download this repository
2. Open `main.ipynb` in Jupyter Notebook, JupyterLab, or VS Code
3. Run the cells sequentially
4. Modify `data_test`, `a`, `b`, the learning rate, or the number of iterations to experiment with the model

---

## Example Output

The notebook produces a list of MSE values during training, which shows how the error changes over time and whether the model is converging.

---

## Possible Improvements

- Add visualizations for the regression line
- Plot the loss curve over epochs
- Support multiple features for multivariate linear regression
- Replace the manual gradient calculation with a more general implementation
- Add documentation and comments to each cell

---

## Future Work

This project can be extended into a more complete machine learning tutorial by adding:

- Data visualization with `matplotlib`
- Comparison with Scikit-Learn results
- Support for real-world datasets
- Mini-batch or stochastic gradient descent

---

## License

This project is released under the MIT License.

---

## Author

Created as an educational project to understand the fundamentals of linear regression and gradient descent.
