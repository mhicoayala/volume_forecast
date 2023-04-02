# Seasonal Volume Forecasting: Seasonal ARIMA, Holt-Winter, & Complex Exponential Smoothing


### About the data
This dataset is from an unnamed contact center company who wishes to forecast their incoming volume to assist in their workforce planning, and to maximize their productivity. It contains the daily received volume from October 2020 to March 2021, excluding the holidays and weekends. Saturday, Sunday and holiday data is set to 0.

![image](https://user-images.githubusercontent.com/65124323/229362506-d2be3242-95db-472e-9a45-08ace0b45ce0.png)

From visual inspection, data has little to no trend and with strong seasonality from it having values only on weekdays.

A sample of the dataset is shown below; a total of 175 rows (days) are found in this data.

```python
# Load dataset using Pandas library

df = pd.read_csv('volume_dataset.csv', parse_dates=['date'])
df.head()
df.shape

```

|    | date                |   calls_received |
|---:|:--------------------|-----------------:|
|  0 | 2020-10-02 00:00:00 |                0 |
|  1 | 2020-10-03 00:00:00 |             2698 |
|  2 | 2020-10-04 00:00:00 |             3105 |
|  3 | 2020-10-05 00:00:00 |             2996 |
|  4 | 2020-10-06 00:00:00 |             3033 |

(175, 2)

Essentially, data is cleaned. No duplicates nor date errors are present.

***

### References

* StatsForecast Documentation - https://nixtla.github.io/statsforecast/examples/getting_started_complete.html
