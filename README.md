# Food Delivery Time Predictor -- Linear Regression

A beginner-friendly end-to-end Machine Learning project that predicts
the estimated time required to deliver a food order using **Linear
Regression**.

The project uses Python to generate and explore sample delivery data,
train and evaluate a regression model, save the trained model with
Pickle, and provide predictions through both a terminal program and a
Streamlit web application.

## Project Overview

Delivery time can be influenced by: - Distance between the restaurant
and customer - Food preparation time - Traffic level - Weather
severity - Rider experience

The model uses these five inputs to estimate delivery duration in
minutes.

## Technologies Used

-   Python
-   Pandas
-   NumPy
-   Matplotlib
-   Scikit-learn
-   Pickle
-   Streamlit

## Project Files

This project contains five Python files:

- create_data.py- Creates sample delivery data.
- eda_inspect_data.py- Explores and visualizes the dataset.
- train_model.py- Trains and evaluates the Linear Regression model.
- predict_data.py-  Predicts delivery time using terminal input.
- streamlit_app.py - Runs the Streamlit web application.
  

The following files are generated when you run the programs: -
`delivery_data.csv` -- the sample dataset. - `delivery_model.pkl` -- the
trained model and its feature names.

## Input Features

  Feature                    Description
  
  `distance_km`              Distance from restaurant to customer in kilometres
  `preparation_time_min`     Food preparation time in minutes
  `traffic_level`            Traffic level: 1 (Low) to 4 (Severe)
  `weather_severity`         Weather severity: 0 (Clear) to 3 (Severe)
  `rider_experience_years`   Rider's experience in years

**Target variable:** `delivery_time_min` -- estimated delivery duration
in minutes.

## Installation

1.  Clone this repository:

    git clone <your-repository-url>
    

2.  Open the project folder in VS Code or a terminal.

3.  (Optional) Create and activate a virtual environment:

    python -m venv venv
    
    On Windows Command Prompt:

    
    venv\Scripts\activate
    

4.  Install the required libraries:

    
    pip install pandas numpy scikit-learn matplotlib seaborn streamlit
    

## How to Run the Project

Run the five Python programs in the following order from the project
folder.

### 1. Generate the dataset
 
python create_data.py

This creates `delivery_data.csv` containing 1,500 sample delivery
records.

### 2. Explore the dataset

python eda_inspect_data.py

This displays the dataset preview, shape, data types, missing values,
statistical summary, correlations, and a scatter plot.

### 3. Train and evaluate the model

python train_model.py

This trains the Linear Regression model, displays evaluation metrics and
learned coefficients, and creates `delivery_model.pkl`.

The dataset is split into: - 80% training data - 20% testing data

The model is evaluated using: - **MAE** -- Mean Absolute Error - **MSE**
-- Mean Squared Error - **RMSE** -- Root Mean Squared Error - **R²
Score** -- Coefficient of determination

### 4. Predict through the terminal

python predict_data.py

Enter the delivery details when prompted. The program displays the
estimated delivery time.

### 5. Run the Streamlit web application

streamlit run streamlit_app.py

If the `streamlit` command is not recognised, try:

python -m streamlit run streamlit_app.py

Open the local URL shown in the terminal (usually
`http://localhost:8501`). Enter the delivery details and click **Predict
Delivery Time**.

## Machine Learning Workflow

1.  Data generation
2.  Exploratory Data Analysis (EDA)
3.  Feature and target selection
4.  Train-test split
5.  Linear Regression model training
6.  Model evaluation
7.  Model saving using Pickle
8.  Prediction on new input
9.  Streamlit web application

## Important Note

The dataset in this project is **synthetic (artificially generated)**
and is intended for learning and demonstration. It is not real data from
a food delivery company.

The application provides an immediate estimate based on the values
entered by the user. It does **not** connect to live GPS, traffic,
weather, or company delivery databases. Predictions are estimates, not
guaranteed arrival times.

## Future Improvements

-   Train the model using real historical delivery data.
-   Add stronger input validation.
-   Integrate live traffic and weather data where appropriate.
-   Compare Linear Regression with other regression algorithms.
-   Improve model evaluation using realistic unseen data.
