# Python APIs
Used APIs to analyze weather data from different cities and pick and map a vacation spot based on this weather data.

## Part I - Weather Data
Created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. Used the [OpenWeatherMap API](https://openweathermap.org/api) to create a representative model of weather across world cities.

Created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude


Next, I ran linear regression on each relationship. I separated the plots into Northern Hemisphere and Southern Hemisphere:

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

The final notebook included:

* 500 randomly selected, unique (non-repeat) cities based on latitude and longitude.
* A weather check on each of the cities using a series of successive API calls.
* A print log of each city as it's being processed with the city number and city name.
* A saved CSV of all retrieved data and a PNG image for each scatter plot.

## Part II - Vacation Spot

Next we used our weather data to plan future vacations. Using jupyter-gmaps and the Google Places API, I did the following:

* Created a heat map that displays the humidity for every city from Part I.

* Narrowed down the DataFrame to find my ideal weather condition.

  *  I dropped any rows that didn't contain all of my conditions

* Using Google Places API, I found the first hotel for each city located within 5000 meters of your coordinates.

* Plotted the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)


© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.

