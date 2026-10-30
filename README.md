# Deep Learning and Transformer for Malaysian Stock Price Prediction

**Author:** MD. ZIHADUL AHSAN RATUL  
**Problem type:** Multivariate time-series forecasting  
**Platform:** Google Colab / Python

## Overview

This project explores historical stock-price forecasting for four Bursa Malaysia-listed companies. It compares three deep-learning architectures:

- Long Short-Term Memory (LSTM)
- Gated Recurrent Unit (GRU)
- Transformer

The notebook downloads historical market data with `yfinance`, performs exploratory data analysis, engineers technical indicators, creates sliding-window sequences, trains the models, and compares their predictions.

## Companies and tickers

| Company | Sector | Yahoo Finance ticker |
|---|---|---|
| Maybank | Banking | `1155.KL` |
| Petronas Gas | Energy | `6033.KL` |
| IHH Healthcare | Healthcare | `5225.KL` |
| Mr. D.I.Y. Group | Consumer retail | `5296.KL` |

**Study period specified in the notebook:** 1 January 2015 – 30 June 2026.

## Project objectives

1. Collect and preprocess historical Bursa Malaysia stock-market data.
2. Explore price and volume behaviour and engineer technical indicators.
3. Develop LSTM, GRU, and Transformer forecasting models.
4. Compare model performance using MAE, RMSE, MAPE, R², and Directional Accuracy.
5. Examine model performance across Bull, Bear, and Sideways market regimes.
6. Identify the best-performing model according to the notebook's evaluation procedure.

## Repository contents

```text
.
├── malaysian_stock_price_prediction.ipynb
├── README.md
├── requirements.txt
├── DATA_SOURCE.md
├── .gitignore
└── LICENSE
```

## Run the notebook

### Option 1: Google Colab

1. Upload `malaysian_stock_price_prediction.ipynb` to Google Colab.
2. Run the cells from top to bottom.
3. Allow the notebook to download the historical data from Yahoo Finance.
4. Review the generated charts, model metrics, comparisons, and CSV output.

### Option 2: Local Python environment

Use Python 3.10 or 3.11 in a virtual environment:

```bash
python -m venv .venv
```

Activate it, then install the dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open `malaysian_stock_price_prediction.ipynb` and run the cells sequentially.

TensorFlow may require platform-specific installation support. If installation fails, use Google Colab, where TensorFlow is generally available.

## Data

The notebook retrieves price history at runtime using the `yfinance` Python package. No downloaded stock-price CSV files are required to start the notebook. See [DATA_SOURCE.md](DATA_SOURCE.md) for details.

## Outputs

The notebook generates exploratory charts, actual-versus-predicted plots, training-history plots, model-comparison charts, market-regime analysis, and an `Overall_Model_Performance.csv` summary.

## Evaluation

The models are compared using:

- **MAE:** Mean Absolute Error
- **RMSE:** Root Mean Squared Error
- **MAPE:** Mean Absolute Percentage Error
- **R²:** Coefficient of determination
- **Directional Accuracy:** Percentage of correctly predicted price directions

Results depend on the data returned by Yahoo Finance, the execution environment, and model training randomness. Run the notebook to reproduce the current results; do not assume results from a previous run will be identical.

## Limitations and responsible use

This is an educational and experimental project, not an investment recommendation or a trading system. Historical price patterns do not guarantee future performance. Market data may be revised or unavailable, and model metrics should not be interpreted as evidence of guaranteed predictive ability.

The repository contains the original notebook as supplied. Its modelling choices and experimental results have not been independently revalidated as part of this documentation package.
