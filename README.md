# House Price Prediction Using Simple Linear Regression

## Project Overview

This project implements a **Simple Linear Regression** machine learning model to predict house prices based on the living area of a property (measured in square feet).

The project uses the King County House Sales dataset, which contains historical house sale records from King County, Washington, USA.

The main objective is to understand how living area influences house prices and build a regression model that can predict house prices using a single independent variable.

## Objectives

- Understand and explore a real-world housing dataset.
- Perform basic data cleaning and preprocessing.
- Explore the relationship between living area and house prices.
- Build a Simple Linear Regression model.
- Make predictions using unseen test data.
- Evaluate model performance using regression metrics.
- Visualize the regression line and prediction results.

## Dataset

**Dataset:** King County House Sales Dataset

**Source:** [Kaggle - House Sales in King County, USA](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)

The dataset contains approximately 21,613 house sale records.

For this project, only two columns are selected:

| Feature | Description | Role |
|---|---|---|
| `sqft_living` | Interior living area in square feet | Independent Variable (X) |
| `price` | House selling price in USD | Dependent Variable (y) |

## Technologies and Libraries

- Python
- Google Colab
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

## Machine Learning Algorithm

**Simple Linear Regression**

Simple Linear Regression is a supervised machine learning algorithm used to model the relationship between one independent variable and one dependent variable.

The model uses the following equation:

\[
\hat{y} = b_0 + b_1x
\]

Where:

- \(\hat{y}\) = Predicted house price
- \(b_0\) = Intercept
- \(b_1\) = Slope (coefficient)
- \(x\) = Living area in square feet

In this project, `sqft_living` is used to predict `price`.

## Project Workflow

1. **Import Libraries** – Import the required Python libraries.
2. **Load Dataset** – Load the house sales CSV dataset using Pandas.
3. **Data Exploration** – Examine the dataset using `head()`, `info()` and `describe()`.
4. **Data Cleaning** – Check and handle missing values.
5. **Feature Selection** – Select `sqft_living` and `price`.
6. **Exploratory Data Analysis (EDA)** – Visualize the relationship using scatter plots and calculate correlation.
7. **Train-Test Split** – Divide the dataset into 80% training data and 20% testing data.
8. **Model Training** – Create and train the Simple Linear Regression model using Scikit-learn.
9. **Prediction** – Predict house prices using the testing dataset.
10. **Model Evaluation** – Evaluate predictions using MAE, RMSE and R².
11. **Visualization** – Plot the regression line against the actual training data.
12. **New Predictions** – Predict the price of a new house using its living area.

## Model Evaluation Metrics

The model is evaluated using the following regression metrics:

| Metric | Purpose |
|---|---|
| MAE (Mean Absolute Error) | Measures the average absolute prediction error. |
| RMSE (Root Mean Squared Error) | Measures prediction error while penalizing larger errors. |
| R² Score | Measures the proportion of target variation explained by the model. |

## Example Prediction

The trained model can be used to predict the selling price of a house with a living area of 2,000 square feet.

```python
new_house = pd.DataFrame({
    "sqft_living": [2000]
})

predicted_price = model.predict(new_house)

print("Predicted House Price: $", predicted_price[0])
```

## Key Learning Outcomes

Through this project, I practiced:

- Loading and exploring real-world CSV datasets using Pandas.
- Data cleaning and preprocessing.
- Understanding independent and dependent variables.
- Exploring correlations between numerical variables.
- Understanding Simple Linear Regression.
- Training a machine learning model using Scikit-learn.
- Making predictions using a trained model.
- Evaluating regression models using MAE, RMSE and R².
- Visualizing regression lines using Matplotlib.

## Limitations

- The model uses only one feature (`sqft_living`) to predict house prices.
- Other factors such as location, number of bedrooms, property condition and age are not considered.
- House prices can vary significantly even when properties have similar living areas.
- The dataset contains historical sales from 2014–2015 and should not be used to estimate current market prices.

## Project Environment

This project was developed using Google Colab.

**Notebook:** `House_Price_Prediction_Simple_Linear_Regression.ipynb`

## Author
Chalani Fernando
Computer Science Undergraduate

## License

This project is intended for educational and learning purposes.
