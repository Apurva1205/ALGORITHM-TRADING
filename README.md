# ALGORITHM-TRADING

TASK 1:
The code defines a Python class called ScriptData, which is used to fetch and store intraday stock price data for a given stock symbol using the Alpha Vantage API with the necessary libraries.
The ScriptData class has an __init__ method which initializes the object with an API key for Alpha Vantage, a base URL for the API, and an empty Pandas DataFrame with columns for timestamp, open, high, low, close, and volume.
The fetch_intraday_data method takes a stock symbol as a parameter and uses the Alpha Vantage API to fetch intraday stock price data for that symbol, which is stored in a class variable called intraday_data.
The convert_intraday_data method takes a stock symbol as a parameter and converts the fetched intraday stock price data from the intraday_data class variable into a Pandas DataFrame with columns for timestamp, open, high, low, close, and volume. This DataFrame is concatenated with the existing df DataFrame of the object, which stores all the intraday data for all the symbols requested.
These are the Python methods that enable indexing, assignment, and containment checking of the df DataFrame of the object.
lines of code create an instance of the ScriptData class with an Alpha Vantage API key, fetch and convert intraday stock price data for the AAPL symbol, and print the first and last 10 rows of the resulting DataFrame.



TASK 2:
The requests and pandas modules are imported, along with the datetime module.
The ScriptData class is defined, which has an __init__ method that takes an API key as an argument and sets up the base URL for API requests, as well as an empty DataFrame with columns for timestamp, open, high, low, close, and volume.
The fetch_intraday_data method takes a stock symbol as an argument and uses it to construct a URL to fetch intraday stock data from the Alpha Vantage API using the requests module.
The response is converted to JSON and stored in the intraday_data attribute of the ScriptData instance.
The convert_intraday_data method takes a stock symbol as an argument and converts the intraday data from JSON format into a DataFrame.
The method loops through each timestamp in the data, converts the timestamp to a datetime object, and creates a dictionary of row data containing the open, high, low, close, and volume values.
These dictionaries are appended to a list, which is then used to create a new DataFrame with the appropriate column names.
Finally, this new DataFrame is concatenated with the existing DataFrame for the ScriptData instance using the concat method.
The indicator1 method takes a time period as an argument and calculates a moving average of the close column of the ScriptData instance's DataFrame.
The moving average is calculated using the rolling method, which takes the window argument set to the time period, and then calling mean() on the close column.
The moving average is returned as a new DataFrame with columns for timestamp andthe moving average is calculated and returned as a new DataFrame with columns for timestamp and indicator, it is printed to the console using the print function.
The first 10 rows of the moving average DataFrame are printed to the console using the head method, which displays the top n (in this case, n=10) rows of the DataFrame. The last 10 rows of the moving average DataFrame are also printed to the console using the tail method, which displays the bottom n (in this case, n=10) rows of the DataFrame.
So, the code is calculating and printing the moving average of the closing prices for AAPL stock using a 5-period window. The moving average is a commonly used technical indicator in financial analysis, which smooths out the price data by averaging the prices over a specified time period, and can help identify trends in the data.


TASK 3:
The code fetches intraday stock price data for a given stock, calculates a moving average of the close price, and computes signals to buy, sell, or hold based on the difference between the close price and the moving average. The code then filters the signals DataFrame to only show rows where the signal is 'BUY' or 'SELL', and creates a plot of the buy and sell signals over time.
The ScriptData class is used to fetch and store the intraday data for a given stock. It contains an __init__ method that takes an API key and sets up the base URL for API requests, as well as a fetch_intraday_data method that makes a request to the Alpha Vantage API and stores the response in a dictionary. The convert_intraday_data method converts the intraday data from the dictionary into a pandas DataFrame and appends it to the df attribute of the ScriptData object.

The Strategy class contains a compute_signals method that takes a stock symbol and computes buy, sell, or hold signals based on the difference between the close price and a moving average of the close price. The moving average is calculated using the indicator1 method, which takes a pandas DataFrame and a time period as input and returns a DataFrame containing the moving average values. The compute_signals method also filters the signals DataFrame to only show rows where the signal is 'BUY' or 'SELL'.

The code creates an instance of the Strategy class with an API key and a time period, and calls the compute_signals method to compute the signals for a given stock. The code then filters the signals DataFrame to only show rows where the signal is 'BUY' or 'SELL', and creates a plot of the buy and sell signals over time.




