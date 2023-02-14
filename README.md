# ALGORITHM-TRADING

PART1:
The code defines a Python class called ScriptData, which is used to fetch and store intraday stock price data for a given stock symbol using the Alpha Vantage API with the necessary libraries.
The ScriptData class has an __init__ method which initializes the object with an API key for Alpha Vantage, a base URL for the API, and an empty Pandas DataFrame with columns for timestamp, open, high, low, close, and volume.
The fetch_intraday_data method takes a stock symbol as a parameter and uses the Alpha Vantage API to fetch intraday stock price data for that symbol, which is stored in a class variable called intraday_data.
The convert_intraday_data method takes a stock symbol as a parameter and converts the fetched intraday stock price data from the intraday_data class variable into a Pandas DataFrame with columns for timestamp, open, high, low, close, and volume. This DataFrame is concatenated with the existing df DataFrame of the object, which stores all the intraday data for all the symbols requested.
These are the Python methods that enable indexing, assignment, and containment checking of the df DataFrame of the object.
lines of code create an instance of the ScriptData class with an Alpha Vantage API key, fetch and convert intraday stock price data for the AAPL symbol, and print the first and last 10 rows of the resulting DataFrame.



PART2:
