# 📈 FundFlow Forecaster: Predictive Analytics for Investment Flows

[![License](https://img.shields.io/github/license/SimengLi1998/FundFlow-Forecaster)](https://github.com/SimengLi1998/FundFlow-Forecaster/blob/master/LICENSE)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SimengLi1998/FundFlow-Forecaster/blob/master/notebook.ipynb)
![Python](https://img.shields.io/badge/python-3.8+-blue.svg)

![Project Logo](logo.jpg)

FundFlow Forecaster is an advanced predictive analytics tool designed to identify tradable signals in investment fund flows. Leveraging time series analysis and multi-class classification techniques, this project aims to forecast fund flow trends and provide actionable insights for investors and fund managers.

## Overview

FundFlow Forecaster analyzes historical data from three types of investment funds in the US market:

1. Institutional Mutual Fund Holdings (IMF)
2. Retail Mutual Fund Holdings (RMF)
3. Exchange Traded Funds (ETF)

The project employs sophisticated time series models and machine learning classifiers to predict fund flow trends and generate trading signals. This tool is valuable for investors seeking to optimize their portfolio strategies and for fund managers aiming to anticipate market movements.

## Key Features

- Comprehensive Exploratory Data Analysis (EDA) of fund flow patterns
- Time Series Analysis with multiple forecasting models:
  - Moving Average
  - Simple Exponential Smoothing
  - Autoregressive Moving Average
  - Long Short-Term Memory (LSTM) Neural Networks
- Multi-class Classification for global optimization and long-term forecasting
- Customizable trading signal generation (Buy, Hold, Sell)
- Performance evaluation metrics for model comparison

## Dataset

The dataset represents 60-70% of activity in the overall asset classes, containing weekly records from 2006 to early 2017. It includes the following key fields:

- ReportDate: Weekly data aggregated and released every Wednesday
- AssetClass: Industry/Sector/Asset Class
- Flow: Amount of positive (inflow) or negative (outflow) in Millions of USD
- FlowPct: Flows as a percent of assets at beginning of the week
- AssetsEnd: Assets at end of the week in Millions of USD
- PortfolioChangePct: Percent change in the overall portfolio during the week

## Methodology

### Time Series Analysis

We implement four time series models for short-term forecasting:

1. Moving Average
2. Simple Exponential Smoothing
3. Autoregressive Moving Average
4. Long Short-Term Memory (LSTM)

Each model is applied to individual industry-fund type combinations after ensuring stationarity.

### Multi-Class Classification

For long-term forecasting and global optimization, we employ a multi-class classification approach:

1. Data preprocessing and feature engineering
2. Implementation of 10 classifier models
3. Selection of Gradient Boosting Decision Tree (GBDT) as the best-performing classifier
4. Generation of tradable signals (Sell, Hold, Buy) based on predicted flow intervals

## Results

- Time Series Analysis: LSTM models demonstrated superior performance in capturing flow value fluctuations.
- Multi-Class Classification: Achieved an overall accuracy of 67.2% with the GBDT classifier.
- Identified distinct characteristics of different fund types and industries, enabling tailored investment strategies.

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/SimengLi1998/FundFlow-Forecaster.git
   ```

2. Install required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open and run the Jupyter notebook:

   ```bash
   jupyter notebook notebook.ipynb
   ```

4. Optionally, run the notebook in Google Colab by clicking the "Open in Colab" badge.

## Documentation

- **[Final Report](report.pdf)**: Provides an in-depth analysis of the project's findings and methodologies.
- **[Final Poster](poster.pdf)**: Offers a visual summary of the project's objectives and results.

## Future Work

- Incorporate more external factors like market indices and economic indicators.
- Experiment with ensemble methods combining time series and classification approaches.
- Develop a user-friendly interface like Web UI for real-time predictions and recommendations.

## Contributors

- Simeng Li
- Kaiyu Wang
- Xiangshan Mu
- Yihan Jia
- Yinghao Wang

## Acknowledgements

We thank Spinnaker Analytics for providing the dataset and Boston University's Questrom School of Business for supporting this capstone project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
