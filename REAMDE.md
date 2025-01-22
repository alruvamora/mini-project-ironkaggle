# House Price Prediction

This project predicts house prices using multiple regression models, based on the features of a property. It uses data preprocessing, exploratory analysis, and a comparison of machine learning models to determine the best model for accurate predictions.

## Table of Contents

1. [Project Description](#project-description)
2. [Dataset](#dataset)
3. [Features](#features)
4. [Requirements](#requirements)
5. [Pipeline Overview](#pipeline-overview)
6. [Models Used](#models-used)
7. [Usage](#usage)
8. [Results](#results)
9. [Future Work](#future-work)
10. [Contact](#contact)

## Project Description

The goal of this project is to predict the price of houses based on features such as square footage, number of bedrooms, bathrooms, year built, and more. The project includes data preprocessing, exploratory analysis, model training, and a final prediction tool based on user input.

## Dataset

The dataset used is `king_country_houses_aa.csv`, containing details about houses in King County. The features include location, size, condition, and historical data on the houses.

## Features

The dataset contains the following key features:

- `bedrooms`: Number of bedrooms
- `bathrooms`: Number of bathrooms
- `sqft_living`: Square footage of the house
- `sqft_lot`: Square footage of the lot
- `floors`: Number of floors
- `waterfront`: Waterfront view (1 for yes, 0 for no)
- `view`: Number of times the house has been viewed
- `condition`: Condition of the house (1-5)
- `grade`: Overall grade of the house (1-13)
- `sqft_above`: Square footage excluding basement
- `sqft_basement`: Square footage of the basement
- `yr_built`: Year the house was built
- `yr_renovated`: Year the house was renovated
- `lat` and `long`: Latitude and longitude
- `price`: Price of the house (target variable)

## Requirements

Install the necessary Python libraries by running:

```bash
pip install -r requirements.txt
```

### Dependencies

- pandas
- numpy
- matplotlib
- scikit-learn
- lightgbm
- xgboost
- lazypredict

## Pipeline Overview

1. **Data Preprocessing**
    - Handle missing values and duplicates.
    - Convert date columns and scale numerical features.
    - Remove irrelevant columns (e.g., `id`, `zipcode`).

2. **Exploratory Analysis**
    - Visualize outliers using boxplots.
    - Evaluate feature ranges and distributions.

3. **Model Selection**
    - Use `LazyRegressor` to evaluate various models.
    - Identify the top-performing models based on metrics such as MSE, RMSE, and R².

4. **Model Training and Evaluation**
    - Train the selected models: LGBMRegressor, HistGradientBoostingRegressor, ExtraTreesRegressor, XGBRegressor, and RandomForestRegressor.
    - Compare their performance on test data.

5. **User Input Prediction**
    - Collect property details from the user.
    - Predict house prices using the trained models.

## Models Used

The following models were evaluated:

1. **LGBMRegressor** (Best model with R² = 0.90)
2. HistGradientBoostingRegressor
3. ExtraTreesRegressor
4. XGBRegressor
5. RandomForestRegressor

## Usage

### Run the Program

1. Prepare your dataset: `king_country_houses_aa.csv`.
2. Execute the script:

```bash
python house_price_prediction.py
```

3. Follow the prompts to input property details for price prediction.

### Example User Input

```bash
Enter number of bedrooms: 3
Enter number of bathrooms: 2
Enter square footage of living space: 2500
...
```

## Results

The models achieved high accuracy, with the LGBMRegressor performing the best:

- **LGBMRegressor**: R² = 0.90, RMSE = 116,213.73
- **HistGradientBoostingRegressor**: R² = 0.89, RMSE = 123,673.15
- **ExtraTreesRegressor**: R² = 0.89, RMSE = 126,942.72

## Future Work

- **Hyperparameter Optimization**: Use grid search or Bayesian optimization to fine-tune model parameters.
- **Feature Engineering**: Add new features like neighborhood trends and proximity to amenities.
- **Model Explainability**: Integrate tools like SHAP or LIME for better interpretability.
- **Deployment**: Deploy the model as a web app using Flask or FastAPI.

## Contact

For questions or suggestions about this project, please feel free to reach out.

Álvaro Ruedas Mora
    
- Data Scientist from **Ironhack**
- Industrial and Automation Electronics Engineer from **Polytechnic University of Madrid**
- MBA from **EAE Business School**
