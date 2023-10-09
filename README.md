# python-api-challenge

# WeatherPy with Python APIs

This project uses Python requests,APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

## Dependencies and Setup

- matplotlib
- pandas
- numpy
- requests
- time
- scipy.stats
- citipy

## Data

The data used in this project is stored in a CSV filed named `cities.csv` located in the `output_data` directory.

## Description

The script first generates a list of random latitude and longitude combinations. It then uses the citipy library to find the nearest city for each combination.

The script then makes API calls to OpenWeatherMap to fetch weather data for each city. The data includes latitude, longitude, maximum temperature, humidity, cloudiness, wind speed, country, and date.

The script then creates a DataFrame from the fetched data and saves it to a CSV file.

The sript it reads the saved data from the CSV file and creates a scatter plot for latitude vs. temperature, latitude vs. humidity, latitude vs. cloudiness,and latitude vs. wind speedd.

Finally, it creates a linear regression model to analyze the relationship between latitude vs. temperature, latitude vs. humidity, latitude vs. cloudiness,and  latitude vs. wind speed.


# VacationPy with Python APIs
# Overview

The WeatherPy project uses Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?" It demonstrates the ability to use Python scripts to visualize weather of 500+ cities across the world of varying distance from the equator.

## Dependencies and Setup

- matplotlib.pyplot as plt
- pandas as pd
- numpy as np
- scipy.stats import linregress

## Data

The data used in this projecty is stored in a CSV file named `cities.csv` located in the `output_data` directory.

## Description

The script first reads the `cities.csv` file into a pandas DataFrame and displays the first few rows of the DataFrame.

It then creates a map that displays a point for every city in the DataFrame. The size of each point represents the humidity in each city.

The script then narrows down the DataFrame to find cities with ideal weather conditions. It drops any cities that do not meet these conditions or have null values.

A new DataFrame called `hotel_df` is created to store the city, country, coordinates, and humidity. An empty column, "Hotel Name," is added to this DataFrame.

For each city in `hotel_df`, the script uses the Geoapify API to find the first hotel located within 10,000 metres of the city's coordinates. If no hotel is found within this radius, "No hotel found" is stored in the "Hotel Name" column.

Finally, it adds the hotel name and country as additional information in the hover message for each city on the map.
