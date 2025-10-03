
# Gold Price Prediction using Random Forest Regressor

This project aims to forecast the price of gold using a machine learning model. The script utilizes a `RandomForestRegressor` to predict the price of GLD (a Gold ETF) based on other related financial market features.

## 📊 Table of Contents

  - [Project Overview](https://www.google.com/search?q=%23-project-overview)
  - [Dataset](https://www.google.com/search?q=%23-dataset)
  - [Methodology](https://www.google.com/search?q=%23-methodology)
  - [Results](https://www.google.com/search?q=%23-results)
  - [Technologies Used](https://www.google.com/search?q=%23-technologies-used)
  - [How to Run](https://www.google.com/search?q=%23-how-to-run)

## 📜 Project Overview

The main objective of this project is to build a regression model that can accurately predict gold prices. The project involves data collection, exploratory data analysis to understand the relationships between different market variables, model training, and evaluation.

## 💾 Dataset

The model is trained on a dataset named `gold price dataset.csv`. This dataset contains daily price information for several financial instruments.

The features used for prediction are:

  - `SPX`: S\&P 500 index price.
  - `USO`: United States Oil Fund price.
  - `SLV`: Silver ETF price.
  - `EUR/USD`: Currency exchange rate for Euro to US Dollar.

The target variable is:

  - `GLD`: Gold ETF price.

## ⚙️ Methodology

The project follows a standard machine learning workflow:

1.  **Data Loading and Preprocessing**: The dataset is loaded using the Pandas library. The script checks for basic information, statistical measures, and missing values.
2.  **Exploratory Data Analysis (EDA)**:
      - A **correlation matrix** is computed to understand the linear relationships between the variables.
      - A **heatmap** is generated to visualize these correlations. It was observed that `GLD` has a strong positive correlation with `SLV` and `SPX`.
      - The **distribution of the `GLD` price** is plotted to understand its statistical distribution.
3.  **Feature Selection**: The `Date` and `GLD` columns are dropped from the feature set (`X`), and `GLD` is selected as the target variable (`Y`).
4.  **Data Splitting**: The dataset is split into training and testing sets, with 80% of the data used for training and 20% for testing.
5.  **Model Training**: A `RandomForestRegressor` with 100 estimators is instantiated and trained on the training data.
6.  **Model Evaluation**: The trained model's performance is evaluated on the test set using the **R-squared error** metric.

## 📈 Results

The model performs exceptionally well on the test data.

  - **R-squared Score**: The model achieves a high R-squared value (typically around **0.98**), which indicates that it can explain approximately 98% of the variance in the gold price.

A comparison plot of the actual vs. predicted `GLD` prices shows that the model's predictions closely follow the actual price trends.

  
*(Note: You would need to run the script, save the generated plot as an image, upload it to your repository or an image hosting service, and replace the URL above.)*

## 💻 Technologies Used

  - Python
  - NumPy
  - Pandas
  - Matplotlib
  - Seaborn
  - Scikit-learn

## 🚀 How to Run

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/your-repository-name.git
    cd your-repository-name
    ```

2.  **Install the required libraries:**

    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn
    ```

3.  **Ensure the dataset is present:**
    Make sure the `gold price dataset.csv` file is in the same directory as the Python script.

4.  **Execute the script:**

    ```bash
    python forecasting_gold_market_trends.py
    ```

    The script will print the R-squared error and display a plot comparing the actual and predicted gold prices.
