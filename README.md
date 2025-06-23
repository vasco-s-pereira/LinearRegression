# Boston Housing Price Predictor

A custom implementation of Linear Regression “from scratch” to predict house prices on the Boston Housing dataset, with a side-by-side comparison to scikit-learn’s `LinearRegression` model using common evaluation metrics.

## Table of Contents
- [Overview](#overview)  
- [Repository Structure](#repository-structure)  
- [Prerequisites](#prerequisites)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Methodology](#methodology)  
- [Results](#results)  
- [Author](#author)  
- [License](#license)  

## Overview  
This project demonstrates how Linear Regression works under the hood. It loads the Boston Housing dataset (`Boston.csv`), implements a `LinearRegressionScratch` class, and then benchmarks it against scikit-learn’s built-in model. Performance is measured by Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-Squared (R²).

## Repository Structure  
```

LinearRegression/
├── Boston.csv                   # Boston Housing dataset (features + target)
├── LinearRegression.ipynb       # Jupyter notebook with full implementation, plots, and analysis
└── README.md                    # This document

````

## Prerequisites  
- Python 3.8 or higher  
- Jupyter Notebook (or JupyterLab)  
- The following Python packages:
  - `numpy`
  - `pandas`
  - `scikit-learn`
  - `matplotlib`

## Installation  
1. Clone this repository:
   ```bash
   git clone https://github.com/vasco-s-pereira/LinearRegression.git
   cd LinearRegression

2. (Optional) Create and activate a virtual environment:

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:

   ```bash
   pip install numpy pandas scikit-learn matplotlib
   ```

## Usage

1. Launch Jupyter Notebook:

   ```bash
   jupyter notebook LinearRegression.ipynb
   ```
2. Step through the notebook to:

   * Load and explore the Boston Housing data
   * Implement and train `LinearRegressionScratch`
   * Compare against scikit-learn’s model
   * Visualize cost convergence (gradient descent)
   * Evaluate and report MSE, MAE, and R²

## Methodology

1. **Data Loading & Exploration**

   * Read `Boston.csv` into a DataFrame
   * Inspect feature distributions and correlations
2. **Model Implementation**

   * **Gradient Descent**

     * Learning rate α
     * Cost function $J(\theta) = \tfrac{1}{2m}\sum (h_\theta(x^{(i)}) - y^{(i)})^2$
     * Iteratively update $\theta := \theta - \tfrac{\alpha}{m} X^T (X\theta - y)$
3. **Benchmarking**

   * Fit scikit-learn’s `LinearRegression` on the same training split
   * Compute MSE, MAE, R² on the test set for both models
4. **Visualization**

   * Plot cost vs. iterations for gradient descent
   * Compare predicted vs. actual prices in a scatter plot

## Results

| Model                      | MSE   | MAE  | R²   |
| -------------------------- | ----- | ---- | ---- |
| Scratch                    | 22.04 | 3.22 | 0.70 |
| scikit-learn               | 21.97 | 3.21 | 0.71 |

*(Your exact numbers may vary slightly depending on random train/test splits.)*

## Author

Vasco Pereira
– Computer Science Student, IST
– 📧 [vasco.serpa.pereira@gmail.com](mailto:vasco.serpa.pereira@gmail.com)

## License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.

```
```
