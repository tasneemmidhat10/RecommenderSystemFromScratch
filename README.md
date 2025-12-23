# 🎬 Recommender System From Scratch

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Libraries](https://img.shields.io/badge/Libraries-NumPy%20%7C%20Pandas-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Overview

This repository hosts a robust **Recommendation System built entirely from scratch**. Unlike standard implementations that rely on high-level libraries like `Surprise` or `scikit-surprise` to do the heavy lifting, this project implements the core algorithms using only fundamental linear algebra and data manipulation libraries (NumPy and Pandas).

The goal of this project is to demystify the "black box" of recommendation engines by manually implementing the mathematical formulas for similarity, matrix factorization, and prediction.

## 🚀 Key Accomplishments

Building a recommender system from the ground up requires a deep technical understanding. Key achievements in this repository include:

* **Mathematical Implementation**: Manual coding of similarity measures (Cosine Similarity, Pearson Correlation) without pre-built functions.
* **Algorithm Engineering**: "From scratch" implementation of **Collaborative Filtering** (User-User and Item-Item) and **Matrix Factorization**.
* **Vectorization**: Optimization of code using vector operations to handle large user-item interaction matrices efficiently.
* **Custom Evaluation**: Implementation of prediction accuracy metrics like **RMSE** (Root Mean Squared Error) and **MAE** (Mean Absolute Error) to benchmark performance.

## ⚙️ Features

* **Data Preprocessing**: Handling raw data and converting it into a structured User-Item Matrix.
* **Similarity Computation**: 
    * User-Based Collaborative Filtering (UBCF)
    * Item-Based Collaborative Filtering (IBCF)
* **Prediction Logic**: Weighted average scoring mechanisms to predict missing ratings.
* **Model Evaluation**: Statistical breakdown of model performance.

## 🛠️ Technologies Used

* **Python**: Core programming language.
* **NumPy**: For high-performance scientific computing and matrix operations.
* **Pandas**: For data manipulation and analysis.
* **Matplotlib**: For visualization

## 📊 Dataset

To benchmark the algorithms, I utilized the **[MovieLens Small Dataset](https://grouplens.org/datasets/movielens/)**. This dataset captures a realistic sparse matrix environment, suitable for testing collaborative filtering.

* **Source**: GroupLens Research
* **Content**: 100,000 ratings and 3,600 tag applications applied to 9,000 movies by 600 users.
* **Structure**:
    * `userId`: Unique identifier for the user.
    * `movieId`: Unique identifier for the movie.
    * `rating`: 5-star scale (0.5 - 5.0).
* **Preprocessing**: 
    The raw CSV log data (`userId`, `movieId`, `rating`) was transformed into a sparse **User-Item Matrix** using Pandas pivoting, where `NaN` values were imputed with `0.0` to represent missing interactions.

## 📂 Project Structure

```bash
RecommenderSystemFromScratch/
├── notebooks/             # Jupyter notebooks for experimentation
├── Graphs/             # Loss Graphs
└── README.md              # Project documentation
