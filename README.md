# IMDb Movie Rating Prediction

This repository contains a machine learning project focused on predicting IMDb movie ratings based on various movie attributes. The project employs data preprocessing techniques, feature engineering, and multiple machine learning models, including **Random Forest Regression** with hyperparameter tuning.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Models Implemented](#models-implemented)
- [Hyperparameter Tuning](#hyperparameter-tuning)
- [Performance Evaluation](#performance-evaluation)
- [Installation & Usage](#installation--usage)
- [Contributors](#contributors)

## Project Overview

The goal of this project is to predict IMDb **movie ratings** based on various movie attributes, including genre, director, actors, year, duration, and votes. The project follows a structured approach of data preprocessing, model selection, and performance evaluation to achieve an optimized prediction model.

## Dataset

The dataset includes information about movies and their ratings, with key features such as:

- **Genre** (Categorical)
- **Director** (Categorical)
- **Actor 1, Actor 2, Actor 3** (Categorical)
- **Year** (Numerical)
- **Duration** (Numerical - in minutes)
- **Votes** (Numerical - total votes)
- **Rating** (Numerical - Target Variable)

## Data Preprocessing

The dataset undergoes multiple preprocessing steps, including:

- **Encoding detection** for proper file reading
- **Handling missing values** (dropping missing target values, imputing categorical and numerical features)
- **Converting string-based numerical features** (e.g., converting "Votes" to float, extracting numeric duration)
- **Removing duplicates**
- **Feature scaling** (StandardScaler for numerical features)
- **One-Hot Encoding** for categorical features

## Feature Engineering

- Encoding categorical variables using **OneHotEncoder**
- Filling missing numerical values with **median imputation**
- Standardizing numerical features

## Models Implemented

The project uses multiple regression models, with a focus on **Random Forest Regression**. The workflow includes:

1. **Baseline Model**: Standard **Random Forest Regressor**
2. **Improved Model with Feature Engineering**
3. **Pipeline Implementation**: Combining preprocessing and modeling steps

## Hyperparameter Tuning

To improve model performance, **GridSearchCV** is used for hyperparameter tuning. The key parameters optimized include:

- **n_estimators**: [100, 200, 300]
- **max_depth**: [None, 10, 20, 30]
- **min_samples_split**: [2, 5, 10]
- **min_samples_leaf**: [1, 2, 4]

## Performance Evaluation

The models are evaluated using:

- **Mean Squared Error (MSE)**
- **R-squared Score (R²)**

The final optimized model achieved **higher accuracy and lower error rates**, indicating effective prediction of IMDb ratings.

## Installation & Usage

### Prerequisites

Ensure you have Python installed along with the required dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### Running the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/imdb-rating-prediction.git
   cd imdb-rating-prediction
   ```
2. Run the Jupyter Notebook or Python script:
   ```bash
   jupyter notebook
   # Open the notebook and execute the cells
   ```

## Contributors

- **Dawood M D** - Data Preprocessing, Model Implementation, Documentation
