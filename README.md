# Household Electricity Consumption Forecasting Using LSTM

## Project Overview

This project aims to forecast household electricity consumption using a Long Short-Term Memory (LSTM) recurrent neural network. The model learns patterns from historical electricity measurements to predict future consumption.

## Problem Statement

An electricity provider wants to forecast household electricity consumption to improve energy distribution and planning. This project uses 10,000 consecutive minute-level records to train and evaluate a time-series forecasting model.

## Objectives

- Load and preprocess household electricity consumption data.
- Handle missing values and normalize numerical features.
- Generate sequences from historical electricity measurements.
- Build and train an LSTM model.
- Evaluate predictions using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
- Visualize actual versus predicted consumption.
- Demonstrate predictions on unseen test records.

## Dataset

**Dataset Name:** Household Electric Power Consumption

**Source:** [Kaggle — Household Electric Power Consumption](https://www.kaggle.com/datasets/uciml/electric-power-consumption-data-set)

The dataset contains household electricity measurements recorded at one-minute intervals.

**Target Variable:** `Global_active_power`

**Measurement Unit:** Kilowatts (kW)

The project uses a selected subset of 10,000 consecutive minute-level records.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- TensorFlow
- Keras
- GitHub

## Methodology

### 1. Data Preprocessing
- Load the dataset using Pandas.
- Convert missing-value markers into proper missing values.
- Combine date and time into a timestamp.
- Handle missing measurements using time interpolation and forward/backward filling.
- Select 10,000 consecutive records.

### 2. Feature Normalization
Use MinMaxScaler to normalize numerical features. Fit the scalers on training data to prevent data leakage.

### 3. Sequence Generation
Use the previous 60 minutes of electricity measurements to predict consumption for the next minute.

### 4. Model Selection
Use an LSTM (Long Short-Term Memory) recurrent neural network because it can learn temporal dependencies in sequential data.

### 5. Model Training
- Chronological training/testing split: 80% training and 20% testing.
- Optimizer: Adam.
- Loss function: Mean Squared Error (MSE).
- Dropout for regularization.
- Early stopping to reduce overfitting.

### 6. Model Evaluation
Evaluate the trained model using:
- **MAE:** Mean Absolute Error.
- **RMSE:** Root Mean Squared Error.

Both metrics are reported in kilowatts after converting predictions back to the original measurement scale.

### 7. Visualization
Plot actual versus predicted electricity consumption and display predictions on unseen test records.

## Results

The model's performance is evaluated on held-out test records.

- **MAE:** Replace with the actual MAE value from the notebook.
- **RMSE:** Replace with the actual RMSE value from the notebook.

The notebook contains the evaluation metrics, training history, comparison graph, and prediction results.

## Repository Structure

```text
household-electricity-forecasting/
│
├── Household_Electricity_Forecasting.ipynb
├── electricity_sample.csv
├── electricity_predictions.csv
└── README.md
```

## How to Run the Project

1. Clone or download this GitHub repository.
2. Open `Household_Electricity_Forecasting.ipynb` in Google Colab.
3. Download the original dataset from Kaggle.
4. Upload `household_power_consumption.txt` when prompted.
5. Run the notebook cells in order.
6. Review the MAE, RMSE, graphs, and unseen-record predictions.

## Conclusion

This project demonstrates the use of an LSTM recurrent neural network for household electricity consumption forecasting. It covers data preprocessing, normalization, sequence generation, model training, evaluation, and visualization. The results can help assess the model's potential for supporting electricity consumption analysis and energy distribution planning.

## Author

Nithish R.

B.Tech Artificial Intelligence and Data Science
