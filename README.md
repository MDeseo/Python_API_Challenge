# Python_API_Challenge

This Assignment 6 was created in conda version 4.13.0 in "PythonData" environment using Jupyter Noteboook.

The folder contains the two scripts for the assignment (WeatherPy_solved and VacationPy_solved),  an "output_data" folder that contains the exported cities from the API call and four plots of latitude vs max temperature, humdity, cloudiness and wind speed from the script WeaherPy_solved, and an "Images" folder that contains the heatmap and hotel map generated with the script VacationPy_solved.

WeatherPy

A Python script was created to visualise the current weather of over 500 cities of varying distances from the equator using a simple Python library (https://pypi.org/project/citipy/) and the OpenWeatherMap API (https://openweathermap.org/api).  a print log was generated for each city as it was being processed,  with the city number and city name. The cities were exported into a csv file in the output_data folder (cities.csv).

To create a representative model of weather across cities, a series of scatter plots were generated:
- Temperature (C) vs. Latitude
- Humidity (%) vs. Latitude
- Cloudiness (%) vs. Latitude
- Wind Speed (m/s) vs. Latitude
The plots were saved as png files and saved in the output_data folder.

The cities were then categorised based on the cities'  latitude position: Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude).

A linear regression was determined for the relationship of:
- Northern Hemisphere: Temperature (C) vs. Latitude
- Southern Hemisphere: Temperature (C) vs. Latitude
- Northern Hemisphere: Humidity (%) vs. Latitude
- Southern Hemisphere: Humidity (%) vs. Latitude
- Northern Hemisphere: Cloudiness (%) vs. Latitude
- Southern Hemisphere: Cloudiness (%) vs. Latitude
- Northern Hemisphere: Wind Speed (kph) vs. Latitude
- Southern Hemisphere: Wind Speed (kph) vs. Latitude
A short explanation of the result of the linear regression modelling was given for each pair of plots for the Northern Hemisphere and Southern Hemisphere.

VacationPy
Using the csv file (cities.csv), a heatmap that displays the humidity for every city in the dataset was generated using py gmaps.  An ideal weather condition was used to narrow down the list with ALL the following conditions:
- A max temperature of < 27 degrees C and > 21 degrees C 
- Wind speed less than 4.5 kph
- Zero cloudiness
Using  the Google Places API, a list of hotels located within 5,000 metres of the coordinates was generated. The hotels were plotted on top of the humidity heatmap, with each pin or marker containing the Hotel Name, City, and Country.
