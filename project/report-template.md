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

- **Initial Model**: RMSE = 3.89352 (as per `submission.csv`).
- **After Feature Engineering**: RMSE = 3.89352 (as per `submission_new_features.csv`).
- **After Hyperparameter Tuning**: RMSE = 1.50177 (as per `submission_new_hpo.csv`).
- Achieved a competitive score on the Kaggle leaderboard.

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/clencyc/bike-sharing-demand.git
   cd bike-sharing-demand
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the Jupyter Notebook:
   ```bash
   jupyter notebook project/project-template.ipynb
   ```

4. Follow the instructions in the notebook to train the model and generate predictions.

---

## Submission Scores

| File Name                  | Date                        | Description                              | Public Score | Private Score |
|----------------------------|-----------------------------|------------------------------------------|--------------|---------------|
| `submission.csv`           | 2025-06-02 20:17:32.973000 | Initial submission with raw predictions | 3.89352      | 3.89352       |
| `submission_new_features.csv` | 2025-06-02 20:29:59.187000 | New features                             | 3.89352      | 3.89352       |
| `submission_new_hpo.csv`   | 2025-06-02 20:35:05         | New features with hyperparameters        | 1.96445      | 1.96445       |
| `submission_new_hpo.csv`   | 2025-06-04 20:02:48.137000 | New features with hyperparameters        | 1.50177      | 1.50177       |

---

## License

This project is licensed under the terms of the [License](LICENSE.txt).