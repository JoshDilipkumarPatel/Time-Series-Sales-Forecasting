# 🛒 Time-Series Sales Forecasting

This project implements a **time-series forecasting pipeline** to predict product sales using **Python** and **LightGBM**.
It handles data cleaning, feature engineering (lags, rolling averages), and time-aware validation to generate reliable sales forecasts.

---

## 🚀 Features

* End-to-end pipeline: raw data → cleaned features → model training → forecasts
* Lag features and rolling means to capture sales patterns
* Time-based validation split (prevents look-ahead bias)
* Automated workflow that outputs a submission file (`submission.csv`)

---

## 🛠️ Technologies Used

* Python 3.x
* Pandas, NumPy
* Scikit-learn
* LightGBM

---

## 📂 Project Structure

```
|── README.md              # Project Documentation
├── Untitled7.ipynb        # Core Code
├── sample_datasets
    ├── california_housing_train.csv              # Training dataset
    ├── california_housing_test.csv               # Test dataset
    ├── california_housing_data_train_small.csv
    ├── mnist_test.csv
    └── anscombe.json
```

---

## ⚡ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/JoshDilipkumarPatel/Time-Series-Sales-Forecasting.git
cd Time-Series-Sales-Forecasting
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

`requirements.txt`:

```
pandas
numpy
scikit-learn
lightgbm
```

### 3. Add your data and Run

* Place your `train.csv` and `test.csv` in the root folder
* Or experiment with the **sample datasets** provided in `sample_datasets/`

### 4. Output

The script generates a **`submission.csv`** file with sales predictions:

```csv
ID,TARGET
100,42
101,37
...
```

---

## 📊 Example Validation Output

```
RMSE: 5.4732
✅ submission.csv created
```

---

## 📂 Sample Datasets

This directory includes a **sample datasets** :

*   `california_housing_data*.csv` is California housing data from the 1990 US
    Census; more information is available at:
    https://docs.google.com/document/d/e/2PACX-1vRhYtsvc5eOR2FWNCwaBiKL6suIOrxJig8LcSBbmCbyYsayia_DvPOOBlXZ4CAlQ5nlDD8kTaIDRwrN/pub

*   `mnist_*.csv` is a small sample of the
    [MNIST database](https://en.wikipedia.org/wiki/MNIST_database), which is
    described at: http://yann.lecun.com/exdb/mnist/

*   `anscombe.json` contains a copy of
    [Anscombe's quartet](https://en.wikipedia.org/wiki/Anscombe%27s_quartet); it
    was originally described in

---

## ✨ Future Improvements

* Hyperparameter tuning with Optuna
* Add holiday/events features
* Compare with ARIMA / Prophet baselines
    Anscombe, F. J. (1973). 'Graphs in Statistical Analysis'. American
    Statistician. 27 (1): 17-21. JSTOR 2682899.

    and our copy was prepared by the
    [vega_datasets library](https://github.com/altair-viz/vega_datasets/blob/4f67bdaad10f45e3549984e17e1b3088c731503d/vega_datasets/_data/anscombe.json).
