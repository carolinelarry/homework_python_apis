# Python APIs
Used APIs to analyze weather data from different cities and pick and map a vacation spot based on this weather data.

## Part I - Weather Data
Created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. Used the [OpenWeatherMap API](https://openweathermap.org/api) to create a representative model of weather across world cities.

Created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude


<img width="485" alt="Screen Shot 2021-09-12 at 10 47 06 AM" src="https://user-images.githubusercontent.com/79863465/132994159-c1116395-726a-49d4-9c8d-fea9734489c6.png">


Next, I ran linear regression on each relationship. I separated the plots into Northern Hemisphere and Southern Hemisphere:

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

<img width="468" alt="Screen Shot 2021-09-12 at 10 48 25 AM" src="https://user-images.githubusercontent.com/79863465/132994177-26ceb662-24a9-41fc-8d7e-b96853fbfaac.png">


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


<img width="858" alt="Screen Shot 2021-08-31 at 1 54 44 PM" src="https://user-images.githubusercontent.com/79863465/132994195-57ad9528-1c97-4ffb-b0c1-8f46d692e7b0.png">


## Contact
Email: cgrace1011@gmail.com



© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.

