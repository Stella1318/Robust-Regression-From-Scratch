## Overview

This repository contains a Jupyter notebook that demonstrates how to implement robust regression using Huber loss. Robust regression is an alternative to traditional ordinary least squares (OLS) regression, particularly useful in scenarios where the dataset contains outliers or when the assumptions of OLS are violated.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Implementation Details](#implementation-details)
- [Key Functions](#key-functions)
- [Results](#results)
- [Conclusion](#conclusion)
- [License](#license)

## Introduction

In this notebook, we build a robust regression model from scratch using NumPy. The model employs the Huber loss function, which combines the benefits of squared error loss for small residuals and linear loss for larger residuals. This approach mitigates the impact of outliers, leading to more reliable parameter estimates.

## Installation

To run this notebook, you will need the following libraries installed:

- Python 3.x
- NumPy

You can install the required libraries using pip:

```bash
pip install numpy
```

## Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/robust-regression-from-scratch.git
    cd robust-regression-from-scratch
    ```

2. Open the Jupyter notebook:
    ```bash
    jupyter notebook robust_regression.ipynb
    ```

3. Follow the instructions in the notebook to explore the implementation of robust regression.

## Implementation Details

The notebook consists of the following key components:

1. **Data Preparation**:
   - The dataset is split into training, validation, and test sets.
   - A dummy variable is added to the feature matrix for the intercept term.

2. **Loss Functions**:
   - Implemented functions for squared error and Huber loss.
   - Defined the gradient computation for robust regression using Huber loss.

3. **Optimization**:
   - Implemented an optimization function that iteratively updates the weights to minimize the Huber loss using gradient descent.

4. **Model Evaluation**:
   - Compared the validation loss of the robust regression model against that of a standard OLS regression model.

## Key Functions

- `squared_error(predictions, targets)`: Computes the squared error loss between predictions and actual targets.
- `huber_loss(predictions, targets, delta)`: Computes the Huber loss based on the given predictions and targets.
- `robust_regression_grad(X, t, w, delta)`: Computes the gradient of the Huber loss for robust regression.
- `optimization(X, t, delta, lr, num_iterations)`: Optimizes the weights for robust linear regression using the gradient descent method.

## Results

The notebook displays the validation squared error loss for both the standard linear regression and robust regression across various values of the parameter \( \delta \). Key insights include:

- The robust regression model shows lower validation loss in the presence of outliers compared to standard OLS regression.
- The optimal value for \( \delta \) can be determined based on validation performance, balancing bias and variance.

## Conclusion

This project demonstrates the implementation of robust regression from scratch using Huber loss. The techniques developed in this notebook can be applied to a wide range of regression problems, especially when dealing with datasets that contain outliers.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to modify any sections to better suit your project or preferences!
