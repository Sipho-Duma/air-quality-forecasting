# air-quality-forecasting
Forecasting air pollutant levels using stacked LSTM networks and time-series modelling.


# Project Overview

This project focuses on forecasting air pollutant levels using Stacked Long Short-Term Memory (LSTM) networks. The goal was to capture temporal dependencies in environmental data and predict future air quality trends. By leveraging deep learning methods, this project demonstrates how time-series forecasting can support environmental monitoring and decision-making.

# About the Dataset
# Context
This dataset contains hourly averaged responses from a gas multisensor device deployed in a polluted area at road level within an Italian city. The measurements were recorded alongside gas concentration references from a certified analyzer. The dataset is publicly available via the UCI Machine Learning Repository: https://archive.ics.uci.edu/ml/index.php

It represents one of the longest freely available recordings of on-field air quality sensor responses, spanning from March 2004 to February 2005 (9357 hourly records). The data captures responses from an array of five metal oxide chemical sensors embedded in an Air Quality Chemical Multisensor Device.

# Content

The dataset includes:

Hourly averaged responses from five chemical sensors targeting CO, Non-Methanic Hydrocarbons (NMHC), Benzene, NOx, and NO₂.

True hourly averaged concentrations for CO (mg/m³), NMHC (µg/m³), Benzene (µg/m³), NOx (ppb), and NO₂ (µg/m³) from a reference certified analyzer.

Environmental variables: temperature (°C), relative humidity (%), and absolute humidity (AH).

Time-stamped records: Date and Time fields for each observation.

Note: Missing values are indicated with -200. Cross-sensitivities, sensor drift, and concept drift are present, affecting sensor concentration estimation capabilities (see De Vito et al., Sens. And Act. B, Vol. 129,2,2008).

| No. | Attribute             | Description                                                     |
| --- | --------------------- | --------------------------------------------------------------- |
| 0   | Date                  | DD/MM/YYYY                                                      |
| 1   | Time                  | HH.MM.SS                                                        |
| 2   | CO (mg/m³)            | True hourly averaged concentration of CO                        |
| 3   | PT08.S1               | Tin oxide sensor response (nominally CO-targeted)               |
| 4   | NMHC (µg/m³)          | True hourly averaged concentration of Non-Methanic Hydrocarbons |
| 5   | Benzene (µg/m³)       | True hourly averaged concentration of Benzene                   |
| 6   | PT08.S2               | Titania sensor response (nominally NMHC-targeted)               |
| 7   | NOx (ppb)             | True hourly averaged concentration of NOx                       |
| 8   | PT08.S3               | Tungsten oxide sensor response (nominally NOx-targeted)         |
| 9   | NO₂ (µg/m³)           | True hourly averaged concentration of NO₂                       |
| 10  | PT08.S4               | Tungsten oxide sensor response (nominally NO₂-targeted)         |
| 11  | PT08.S5               | Indium oxide sensor response (nominally O₃-targeted)            |
| 12  | Temperature (°C)      | Ambient temperature                                             |
| 13  | Relative Humidity (%) | Ambient relative humidity                                       |
| 14  | Absolute Humidity     | Absolute humidity                                               |


# Project Workflow

## Data Preprocessing

- Handled missing values and outliers

- Normalized features using Min-Max scaling

- Converted time-series data into supervised learning format

## Model Design

- Built Stacked LSTM architecture using TensorFlow/Keras

- Tuned hyperparameters (number of layers, units, batch size, learning rate)

- Used dropout regularization to prevent overfitting.

## Model Training & Evaluation

- Split dataset into training and testing sets (80/20).

- Evaluated model using Root Mean Squared Error (RMSE) and Mean Absolute Error (MAE).

- Visualized training performance and predicted vs. actual pollutant levels.

## Visualization & Insights

- Generated time-series plots of pollutant trends.
  
# Results

- Achieved low RMSE and MAE values, indicating accurate pollutant forecasting.

- Model successfully captured short-term temporal patterns in air quality trends.

- Visual analysis showed strong correlation between meteorological factors and pollutant concentrations.

# Key Insights

- Deep learning models like Stacked LSTMs effectively capture complex time dependencies in environmental data.

- Regularization and proper hyperparameter tuning significantly improve model performance.

- Data-driven forecasting can help environmental agencies and policy-makers anticipate poor air quality days.
