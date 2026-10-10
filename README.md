# Hourly PM10 Forecasting: Time-Series Model Comparison

This project investigates hourly PM10 forecasting at the Gucheng monitoring station in Beijing, China. It compares classical machine learning and deep learning approaches across multiple forecast horizons, with additional experiments focused on predicting high-pollution events.

## Project Objectives

- Analyze hourly air-quality data and prepare it for time-series forecasting.
- Compare model performance across 1-hour, 24-hour, and 72-hour forecast horizons.
- Evaluate classical machine learning models against recurrent and convolutional neural networks.
- Explore a peak-aware modeling approach designed to improve predictions during high-PM10 periods.

## Methods

The project explores the following approaches:

- **Classical machine learning:** Persistence baseline, Ridge Regression, Support Vector Regression (SVR), Random Forest, and XGBoost.
- **Deep learning:** Simple RNN, LSTM, GRU, and CNN-LSTM architectures.
- **Peak-aware forecasting:** A CNN-GRU-based approach that incorporates peak-event detection and additional prediction adjustments.

The notebooks use time-ordered data splits to evaluate forecasting performance. Model evaluation includes metrics such as MAE, RMSE, and R², alongside additional analyses of high-pollution periods.

## Repository Structure

```text
Air-Quality-Data-Analysis/
├── data/
│   └── Gucheng.csv
├── Classical_ML_1H_24H_72H.ipynb
├── RNN_LSTM_GRU.ipynb
├── CNN_LSTM_24H.ipynb
├── 24H_Peak_Aware.ipynb
└── README.md
```

## How to Run

1. Open a notebook in Google Colab or Jupyter Notebook.
2. Make sure the dataset is accessible and update the file path if necessary.
3. Install any missing dependencies.
4. Run the notebook cells in order.

**Main dependencies:** Python, pandas, NumPy, Matplotlib, scikit-learn, XGBoost, and TensorFlow/Keras.

## Limitations

- The analysis focuses on a single monitoring station and a limited evaluation setup.
- Forecasting performance may vary across time periods, locations, and data conditions.
- Missing-value handling and model-selection decisions can affect the results.
- The peak-aware approach is experimental and should not be assumed to outperform other models in every evaluation setting.

## Data Source

This project uses hourly air-quality data for the Gucheng monitoring station in Beijing, based on the **[Beijing Multi-Site Air Quality Dataset](https://archive.ics.uci.edu/dataset/501/beijing)** available through the UCI Machine Learning Repository.

**Dataset citation:**

Chen, S. (2017). *Beijing Multi-Site Air Quality* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5RK5G

**License:** The UCI dataset page specifies a Creative Commons Attribution 4.0 International (CC BY 4.0) license. The provenance of the local `Gucheng.csv` file should be checked against the original dataset before redistribution.

## Scope

This project demonstrates a time-series data analysis workflow, including data preprocessing, feature preparation, forecasting, model comparison, and performance evaluation, with an emphasis on air-quality prediction.
