# Causal Inference in Portfolio Management: Master's Thesis Research

This repository houses the Python-based implementation for my master's thesis research. The core objective is to explore and effectively leverage causal inference techniques within portfolio management strategies, aiming to build more robust and insightful investment approaches.

## Experimental Implementation (Python)

This project implements a complete pipeline for applying causal inference to portfolio management:

1.  **Financial Data Handling:** Download and standardization of financial returns from Yahoo Finance.
2.  **Causal Discovery:** Application of the PC algorithm for causal discovery, with options for Pearson and HSIC independence tests.
3.  **Graph-Aware Covariance:** Construction of a covariance matrix that incorporates the discovered causal graph through analytical shrinkage techniques.
4.  **Portfolio Optimization:** Mean-variance optimization based on the graph-aware covariance, with a comparative analysis against the traditional mean-variance approach.

## Key Features

* **Flexible Independence Tests:** Interchangeable independence tests are supported, including `partial_correlation_test` and `kernel_independence_test`.
* **Temporal Modeling:** Integrated handling of temporal constraints using node suffixes like `_t`, `_t-1`, etc., to capture time-lagged relationships.
* **Visualizable Causal Structures:** The discovered Directed Acyclic Graph (DAG) can be exported to Graphviz for visualization and in-depth relationship analysis.
* **Robust Hyperparameter Tuning:** Hyper-parameter β is tuned using validation data, and the final models are evaluated using key performance metrics such as Sharpe ratio, Sortino ratio, and volatility.
* **Thesis-Ready Visualizations:** The repository includes scripts to generate publication-quality visualizations, including the DAG structure, Sharpe ratio vs. γ curves, and stacked asset weights.