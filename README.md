# Coursera_Capstone
Coursera Capstone Repository

# 1. Introduction
## 1.1 Background
Now a days it is becoming more frecuent to see people who cares about their health. A consecuence of this is the fact that places related with healthcare, like gyms, have much more attendance than past years. 

On the other hand Chicago is a very big city, plenty of people which spend mos of their time at work and do not have much time left for activities such as coking. Even though there are plenty of good restaurants in any city, most of this places are fast food or, at least, no so healthy food. So, if you want to open a new food bussines, a healthy restaurant sounds like a good idea of bussiness.

Opening a restaurant is a challenging project, so that in order to open such kind of restaurant in a big city like Chicago, one have to care about which is the best location to place it. Data science arises as the needed tool to answer this question. 

## 1.2 Problem
The first step will be to acquire useful data. The density of gyms in different parts of the city can be very valuable info, as the target of the restaurant is people who are likely to go to the this places. To use as location a region of the city where there is a high density of gyms can ensure a good visibility for the commerce.

Chicago is divided in a lot of small neighborhoods. To use one of those areas to choose a location can be too much restictive due to the size. Use instead a cluster of neighborhoods can be a much better option, because if offers a bigger area to search for a place to locate the restaurant.

# 2. Data description
## 2.1 Data sources
The first place to look for data of the city is the [Chicago Data Portal](https://data.cityofchicago.org), where there is plenty of data to work with. Inside this page one can find geospatial data of all the neighborhoods in the city, [link](https://data.cityofchicago.org/api/geospatial/bbvz-uum9?method=export&format=GeoJSON).

The [Foursquare](https://foursquare.com/developers/apps) API provides us of a source of information about any kind of venues in a lot of places around the world. A request to this service will give the location of the gyms around a given coordinates.

## 2.2 Data cleaning
The data of the neighborhoods downloaded from the Chicago portal is in a json file. Inside this file there are several properties of each neighborhood. I stracted the "primary neighborhood" wich is the borough, the " secondary neighborhood" which is the proper neighborhood and the geographical info. This data is in the format of points which delimitates the area of the neighborhood. I used a function which calculates the centroid of any polygon to get the coordinates of the neighborhood.



