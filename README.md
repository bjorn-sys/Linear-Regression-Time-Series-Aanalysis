
# 📈 Linear Regression Time Series Analysis

# 🧠 Project Overview

* This project involves building a Linear Regression Time Series Model to predict air quality (PM2.5 readings) over time. By creating a time-shifted feature and analyzing timestamped sensor data, the model forecasts future PM2.5 levels based on historical patterns.


---

# 📦 Dataset Description

* The dataset consists of sensor data used to measure environmental variables. Below are the key columns:


---

# 🔧 Preprocessing Steps

* Imported all required Python libraries (pandas, numpy, matplotlib, sklearn, etc.)

* Converted timestamp to proper datetime format (initially read as string/object)

* Localized the timestamp to Nairobi, Africa time zone

* Resampled data to 1-hour intervals

* Used forward fill (ffill) to handle missing values, as using mean/median isn't appropriate for time series (future values shouldn't inform the past)

* Filtered out unrelated value_types to isolate PM2.5 (P2) readings



---

# 📉 Feature Engineering

* Created a time-shifted column (P2.LI) as a predictor — a lag of the PM2.5 values

* Calculated the correlation between the lagged feature and the target PM2.5 values:

* Correlation coefficient: 0.83 – indicating strong predictive strength




---

# 📊 Visualization

* Count plot of total measurements across sensors and locations

* Scatter plot between PM2.5 and its time-shifted version (P2.LI) to visualize linear relationship

* Rolling average (7-day window) to observe weekly trends in air quality

* Line plots to visualize predictions and actual values



---

# 🧪 Model Training & Evaluation

* Model: Linear Regression

**Dataset split:**

* 80% for training

* 20% for testing


**Evaluation Metrics:**

* Baseline MAE: Mean Absolute Error using simple mean as prediction

* Training MAE: MAE on training data

* Testing MAE: MAE on test data



# > ⚠️ Note: Testing MAE was higher than Training MAE due to limited test data, which is common when the test set is small or when overfitting may have occurred.




---

# 📌 Key Insights

* A simple linear regression model can yield useful results with a strong lagged feature

* PM2.5 values are highly correlated with their past values — suitable for time series forecasting

* Time-based resampling and proper handling of timestamps are critical for model accuracy

* Forward-filling is preferable over statistical imputation in time series tasks



---
