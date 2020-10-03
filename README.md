# World_Weather_Analysis
UofT Data Analytics project: PlanMyTrip app.

# Overview
The PlanMyTrip app creates a list of preferred destination based on the user's weather preference and finds the nearest hotel. In the beta tester the user will choose four cities to create a travel itinerary and the app will use Google Maps Jupyter API to display the travel route between the destinations as well as a marker with city, country, weather description, hotel and maximum temperature information for each city.

# Details

The PlanMyTrip app contains the following components

* `Weather_Database.ipynb`
    Creates a list of 2000 randomly chosen cities with weather information
* `Vacation_Search.ipynb`
    Creates a list of cities and closest hotels based on the user's preferred weather temperature range
* `Vacation_itineary.ipynb`
    Will show the route between 4 chosen cities as well as the information marker for each

## Weather_Database.ipynb

We first create a random list of 2000 latitudes and longitudes using numpy random function.<br>
We then Use the `citipy` module to determine the city based on latitude and longitude.<br>
Finally we save this list as `WeatherPy_Database.csv` file.

## Weather_Search.ipynb

We use the user's minimum and maximum temperature preferences to create a sub-list of cities.<br>
We then get the nearest hotel (within 5 kilometers) using Google maps `nearbysearch` API and discard the records where a hotel is not found. We save this list as a csv file.<br>
We provide the hotel and weather information for each city using Google maps Jupyter `markup_layer`.

## Weather_Search.ipynb

We choose 4 cities from the list created above.<br>
We then use the `(latitude,longitude)` of the cities to display the route between these cities using Google maps Jupyter API `directions_layer`<br>
We provide the hotel and weather information for each city as markup in the map

