# Predicting next-year GDP using Machine Learning and World Bank data

This project comes out as part of the work done in my Master thesis. Here ML algorithms are used - using World Bank data - to obtain models with higher performance - measured in MAE and MSE - than standard econometric models - such as those used by the IMF. Years 2010 to 2019 are selected to exclude crisis in 2009 and 2020.

## Overview of process:
The following steps are taken into consideration:
- **Data downloading:** using the World Bank API
- **Data preparation:** cleaning data, selecting years, etcetera
- **Exploratory analysis:** initial plots
- **Outlier detection:** to assess whether certain countries may have data quality issues
- **Training ML models:** different models are attempted and trained, using walk forward CV for time series to tune hyperparameters
- **Forecast combination**
