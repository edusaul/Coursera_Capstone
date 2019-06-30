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
The data of the neighborhoods downloaded from the Chicago portal is in a json file. Inside this file there are several properties of each neighborhood. I stracted the "primary neighborhood" wich is the borough, the " secondary neighborhood", the proper name of the neighborhood, and the geographical info. This geographical data is in the format of points which delimitates the area of the neighborhood. I used a function to put into a pandas dataframe the borough, neighborhood, latitude and longitude of each element of the list in the json file. For the geographical info I used a function which calculates the centroid of any polygon to get the coordinates of the neighborhood.

To get the locations of the gyms close to a given coordinates I used the Foursquare API. We can obtain a json file as the result of doing a request to Foursquare, which contains a list of all the venues that we asked for. Form this file we can extract for each venue it's name, latitude and longitude. I modified a function from the previous notebooks on the course, to get a function which can do a request and extract the required info and put it into a pandas data frame.

Once I get the pandas data frames, using those tools, I am able to handle the data and merge it to get the final tables I need to get the results.


