# Forecasting-Stock-Market-Prices
A time series is simply a series of data points ordered in time. In a time series, time is often the independent variable and the goal is usually to make a forecast for the future. Our Aim is to create a model that can forecast the future stock price based on the model training and provided dataset.


### Data
We will be using a [Huge stock market dataset]from the Kaggle platform which has a very good collection of datasets.The file we will be using is present in following directory in the dataset 'D:\Datasets\gs.us.txt'
  
The data is presented in CSV format as follows : Date, Open, High, Low, Close, Volume, OpenInt.

Features:
  - Date
  - Open
  - High
  - Low
  - Close
  - Volume
  - OpenInt
  
Note that prices have been adjusted for dividends and splits.

## Task 1 : Import the Libraries
Libraries we imported:

1. NumPy
2. Pandas
3. matplotlib
4. scikit-learn
5. statsmodels

## Task 2 : Preprocessing
Here we will process the time series data and preprocessing dates. We wil use date parsing which converts the date in a format using Lambda to create a function.

Data is processed and well organized.

## Task 3 : Exploratory Data Analysis (EDA)
Here we will see how data changes during time.
We will plot a graph with lenght and breadth of 16 : 8 and give x axis as dates and y axis as open prices.

Price increases from 2000 to 2018, from 2017 it higher.

## Task 4 : Autocorrelation plot
Autocorrelation is similarity between observations as a function of time lag between them, if we shift the values and find relation i.e., autocorrelation.

Here seasonality is plotted by autocorrelation.

All the values open will be stored in pandas dataframe, we created dataframe variable and concatenated all the values.

After that we will shift the values by 1, 5, 10 and 30.

Here we got the correlation values

## Task 5 : Dickey-Fuller Method to check stationary and seasonality
Stationary Data: the time series data which is constant over time.

Seasonality: it is periodic fluctuation.

Dickey-Fuller is used to check the stationary and seasonality. It tests the null hypothesis if unit root is present or not. So if p value is > 0 then process is not stationary if p is o it is stationary.

- Here time series data is not stationary
- No Seasonality as autocorrelation is high

Here we will copy the data so original data does not change and if we want to change the original data then we use deep.

p value is 0 so it is stationary and seasonality is there. After this we can do modelling.

## Task 6 : Modelling
Here we will split the data into test and train because of overfitting of data which will not be good.

Green is the train data from 2015 to 2017 with 600n values and blue is the test data for 73 values.

## Task 7 : Mean Value plot
 Here we will check if predicted value has a mean of datasets. we will check what value mean sqaure error, mean average error and Root Mean Square error.
 
- red color line is shown from 2015 and above
- mean value is statioanary in both the graphs
 
#### Now we will for Mean square error, Mean Average Error and Root Mean Square error.
Here we will find out the error between true values and mean values

- MSE:6.614792639144097
- MAE:1.9907383591040042
- RMSE:2.571923917837403

## Task 8 : Model Building and Validation
Once data is analyzed and normalised we build the model with different models: Autoregressive model and moving average model.

### 8.1 : Autoregressive model
We forecast variable of interest using linear combination of past values of that variable.
Autoregressive is a regression of variable against itself.
Observation from previous time as an input to the regression equation.

Plotting graph for close price, Test close price and predicted close price

Here lag is 31 and prices are moving accordingly

### Now we will check for Mean square error, Mean Average Error and Root Mean Square error.
Here we will find out the error between true values and mean values

- MMSE:6.614792639144097
- MAE:1.9907383591040042
- RMSE:2.571923917837403

## 8.2 : Moving Average Model
Moving average model is the common approach to model time series.
Output variable depends linearly on current and past values.

Plotting graph for train stock price, real stock price and predicted stock price

Prices are moving accordingly

### Now we will check for Mean square error, Mean Average Error and Root Mean Square error.
Here we will find out the error between true values and mean values

- MSE:6.5848601233841375
- MAE:2.001128903067832
- RMSE:2.566098229488524

# Conclusion:
In this forecasting stock price project which is a time series project, time is often the independent variable and the goal is usually to make a forecast for the future. we created a model that can forecast the future stock price based on the model training and provided dataset.
From both the models autoregressive and moving average model we got the values that are very close.
Here we got to predict the ups and downs of the price over the years that how much difference is there between the price and what we can do accordingly.








