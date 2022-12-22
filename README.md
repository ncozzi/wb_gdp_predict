# Predicting next-year GDP using Machine Learning algorithms and World Bank data

This project comes out as part of the work done in my Master thesis. Here ML algorithms are used - using World Bank data - to obtain models with higher performance - measured in MAE and MSE - than standard econometric models - such as those used by the IMF. Years 2002 to 2021 are selected.

Some caveats:
* Annual data is utilized, which might heavily decrease the accuracy; research has shown better results when using quarterly data
* Quarterly GDP growth is available in the OECD dataset, which would restrict the scope of countries
* Different data collection methodologies and standards of quality across governments might introduce extra bias in some observations and groups
* For neural networks, only basic multi-layer perceptrons were built; an extension for the future is assessing extensions of LTSM and RNN for corss-sectional data

This project is inspired by my MSc Statistics and Data Science thesis research; what you see here is part of the resulting work - in this notebook I am focusing exclusively on the development of supervised learning models


## Overview of process:
The following steps are taken into consideration:
- **Data downloading:** using the World Bank API
- **Data preparation:** cleaning data, selecting years, etcetera
- **Exploratory analysis:** initial plots
- **Outlier detection:** to assess whether certain countries may have data quality issues
- **Training ML models:** different models are attempted and trained, using walk forward CV for time series to tune hyperparameters
- **Forecast combination**
-------------------
## Notebooks:
- *wb1_api_data.ipynb*: querying and downloading data from the World Bank dataset API
- *wb2_data_manipulation.ipynb*: data preparation (cleaning data, selecting countries, removing outliers, etcetera), downloading benchmark, exploratory analysis
- *wb3_gdp_predict.ipynb*: building ML regression models, assessing best performer

----------------------

## Results
Best performing algorithm is the **Random Forest regression** using the scikit-learn library

| Model | MAE    |  MSE   |
| :---:   | :---: | :---: |
| RF regression | 0.5703   | 0.8681   |
| WEO (spring report) | 0.6955   | 0.9915   |
| WEO (fall report) | 0.6504   | 0.9364   |
