7-Day Passenger Demand Forecasting Using Prophet

This project predicts daily passenger demand for different public transport services such as Local Route, Light Rail, Rapid Route, Peak Service, and School transport. The objective is to generate a reliable 7-day forecast to support operational planning. Since the data is collected on a daily basis and changes over time, a time-series algorithm is used.


Algorithm Used-(Prophet):
The Prophet model (by Meta) is selected for forecasting because it works well with daily data, automatically captures weekly patterns, and handles sudden changes and missing values. The dataset showed strong weekday–weekend variations, especially for School and Peak services, making Prophet a suitable model for this problem.

Data Preparation :
The dataset was cleaned by-
Converting the Date column into proper date format
Removing duplicate dates
Converting passenger columns into numeric values
Filling missing values using linear interpolation
Enforcing daily frequency to avoid gaps
For modeling, the data was converted into Prophet’s required format (ds for date and y for passenger count). A log tr was applied to stabilize large values, and predictions were converted back using the exponential function.

Training and Evaluation:
The data was split into training data and the last 14 days as validation data. The model was evaluated using MAE and RMSE. To ensure that Prophet truly adds value, it was compared with a 7-day moving average baseline model. The Prophet showed 15–30% lower RMSE, proving better accuracy than the baseline.

Conclusion:
The Prophet model provides a reliable and accurate method for short-term public transport demand forecasting. The generated 7-day forecasts can help in better scheduling, capacity planning, and resource allocation.
