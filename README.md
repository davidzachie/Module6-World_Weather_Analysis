# **Module6-World_Weather_Analysis**

## **Purpose of the Project**

### The purpose of this projects is to create a travel itinerary map that allows users to apply weather criteria to identify potential travel destinations and nearby hotels. By utilizing Google MAP Directions API, we also created a travel route between their four destinations and a marker layer map with pop-up markers that provide them with information of cities, nearby hotels, and current weather condition in the areas.

## **Overview of the Project and Analysis**

### The first step in the analysis is to create a list of cities and their weather condition by:
    1.  Generating 2,000 random latitudes and longitudes and get the nearest cities using the citipy module.
    2.  Perform API call with the OpenWeatherMap to obtain locations and their weather condition and created a WeatherPy_Database.csv file.

### [Weather_Database.ipynb](https://github.com/davidzachie/Module6-World_Weather_Analysis/blob/413e02bd830a716f567f01b8afb84a6bb31da820/Weather_Database/Weather_Database.ipynb)

### The second step is to create a travel destinations map based on customer weather preferences:
    1.  Obtain customer's minimum and maximum temperature preferences using input statements and use the values to filter the WeatherPy_Database.csv and create the city_data_df DataFrame.
    2.  Next we setup parameters and use the Google API to make API request call and retrieve the JSON data to obtain nearby hotels' names and add them to the city_data_df DataFrame, store it as hotel_df, and export it as WeatherPy_vacation.csv
    3.  Create a marker layer map with pop-up markers for each city on the map.

### [Vacation_Search.ipynb](https://github.com/davidzachie/Module6-World_Weather_Analysis/blob/413e02bd830a716f567f01b8afb84a6bb31da820/Vacation_Search/Vacation_Search.ipynb)
    
### [WeatherPy Vacation Map](Vacation_Search/WeatherPy_vacation_map.png)
    
### The last step is to create a travel itinerary map for our customer:
    1.  First, we enable Google's Directions API.
    2.  We use the WeatherPy_vacation.csv containing cities, hotel locations, and weather condition to customize a travel itinerary by selecting cities that our customer wants to visit.
    3.  Finally, we created a travel routes map with driving direction and a marker layer map with pop-up markers for each city showing hotel name, city, country, current weather description, and maximum temperature.

### [Vacation_Itinerary](https://github.com/davidzachie/Module6-World_Weather_Analysis/blob/413e02bd830a716f567f01b8afb84a6bb31da820/Vacation_Itinerary/Vacation_Itinerary.ipynb)
    
### [WeatherPy Travel Map](Vacation_Itinerary/WeatherPy_travel_map.png)

### [WeatherPy Travel Map with Markers](Vacation_Itinerary/WeatherPy_travel_map_markers.png)


