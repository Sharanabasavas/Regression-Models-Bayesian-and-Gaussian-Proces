# Regression Models: Ridge, Bayesian, and Gaussian Process

This project demonstrates the implementation of Ridge Regression, Bayesian Ridge Regression, and Gaussian Process Regression models on a housing dataset, with a focus on understanding the effects of regularization (alpha values) on model performance. The goal is to explore how each model handles regularization and how they differ in terms of predictive accuracy and model behavior.

## Table of Contents
- [Introduction](#introduction)
- [Models Explained](#models-explained)
  - [Ridge Regression](#ridge-regression)
  - [Bayesian Ridge Regression](#bayesian-ridge-regression)
  - [Gaussian Process Regression](#gaussian-process-regression)
- [Effect of Regularization](#effect-of-regularization)
  - [Ridge Regularization](#ridge-regularization)
  - [Bayesian Regularization](#bayesian-regularization)
  - [Gaussian Regularization](#gaussian-regularization)
- [Graphs & Visualization](#graphs--visualization)
  - [Actual vs Predicted](#actual-vs-predicted)
  - [Residuals Plot](#residuals-plot)
  - [Prediction Distribution Comparison](#prediction-distribution-comparison)
- [Performance Evaluation](#performance-evaluation)
- [Installation and Requirements](#installation-and-requirements)
- [Conclusion](#conclusion)

## Introduction

This project focuses on understanding the effects of regularization on various regression models, specifically:
- **Ridge Regression**
- **Bayesian Ridge Regression**
- **Gaussian Process Regression**

The models are evaluated using a housing dataset, which contains features related to housing prices. The target variable is the median house value. The goal is to assess how different regularization strengths (alpha values) impact model performance.

## Models Explained

### Ridge Regression
Ridge Regression applies L2 regularization (Tikhonov regularization) to regression coefficients, penalizing large coefficient values. This helps prevent overfitting and improves generalization.

### Bayesian Ridge Regression
Bayesian Ridge Regression is a probabilistic model that estimates the posterior distribution of coefficients using Gaussian priors, making it robust to outliers. Regularization is controlled by:
- `alpha_1`: Prior precision on coefficients.
- `alpha_2`: Prior precision on noise.

### Gaussian Process Regression
Gaussian Process Regression is a non-parametric model that assumes the underlying function is drawn from a Gaussian Process. The kernel function defines the covariance, and regularization is controlled by `alpha`, which determines noise level.

## Effect of Regularization

### Ridge Regularization
- High `alpha` values: Strong regularization → underfitting.
- Low `alpha` values: Weak regularization → potential overfitting.

### Bayesian Regularization
- Higher `alpha_1`: Stronger regularization, smaller coefficients.
- Higher `alpha_2`: Reduces noise uncertainty, leading to smoother predictions.

### Gaussian Regularization
- High `alpha`: Smoother predictions but potential underfitting.
- Low `alpha`: Captures more noise, risking overfitting.

## Graphs & Visualization

### Actual vs Predicted
Graphs comparing actual vs predicted values illustrate model accuracy.

### Residuals Plot
Residuals should ideally scatter randomly around zero. Patterns indicate overfitting or underfitting.

### Prediction Distribution Comparison
Histograms show how models handle uncertainty and regularization, comparing prediction distributions.

## Performance Evaluation

Models are evaluated using:
- **Root Mean Squared Error (RMSE)**: Lower values are better.
- **R² Score**: Higher values indicate a better fit.

## Installation and Requirements

Ensure the following libraries are installed:
```bash
pip install numpy pandas matplotlib scikit-learn


