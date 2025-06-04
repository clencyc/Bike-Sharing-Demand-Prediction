# Bike Sharing Demand Prediction with AutoGluon

This project aims to predict bike rental demand using historical data. The dataset includes features such as weather conditions, time, and season, which are used to train a machine learning model to forecast bike usage. The solution leverages **AutoGluon**, an automated machine learning (AutoML) framework, to simplify model training and optimization.

---

## Project Overview

- **Goal**: Predict the number of bike rentals for a given time period.
- **Dataset**: Provided by Kaggle's [Bike Sharing Demand competition](https://www.kaggle.com/c/bike-sharing-demand).
- **Tools Used**: Python, AutoGluon, Pandas, Matplotlib, and Scikit-learn.

---

## Key Steps

### 1. Initial Training
- Trained an initial model using AutoGluon's default settings.
- Submitted predictions to Kaggle and adjusted the output format to meet submission requirements.

### 2. Exploratory Data Analysis (EDA) and Feature Engineering
- Conducted EDA to identify trends and correlations in the data.
- Added new features such as:
  - `hour` (extracted from `datetime`).
  - `is_rush_hour` (binary feature for peak commuting times).
  - `temp_diff` (difference between `temp` and `atemp`).

### 3. Hyperparameter Tuning
- Fine-tuned hyperparameters like learning rate, number of estimators, and tree depth.
- Improved model performance by reducing RMSE on the validation set.

---

## Results

- **Initial Model**: RMSE = 0.45
- **After Feature Engineering**: RMSE = 0.40
- **After Hyperparameter Tuning**: RMSE = 0.38
- Achieved a competitive score on the Kaggle leaderboard.

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/bike-sharing-demand.git
   cd bike-sharing-demand