# Introduction

Vancouver is one of the Top 10 cities to live in around the world, according to The Economist Intelligence Unit’s 2019 Global Liveability Index. One of my friends would like to move there and open a gym there, but is unsure of where he should open it. He has learned that I am doing a Data Science Certificate program, and is wondering if I could help him do some analysis and see which location in Vancouver may be the best. He wants to make sure there are not too many other gyms/indoor sports facilities located closeby already.

# Data

I downloaded the Vancouver neighborhood data from the [Wikipedia site](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_V). This website contains the list of postal codes in British Columbia, Canada, with the borough and neighborhood(s) data under each postal code. I also downloaded the latitude and longitude coordinates for each postal code using the CA.zip file under the [GeoNames.org website](http://download.geonames.org/export/zip/). I scraped the data and combined these together to get the Borough, Neighborhood, Latitude and Longitude data by Postal Code. Since this data contains postal codes/boroughs that are in the British Columbia province, I further narrowed it to only include postal codes that are in the Vancouver Borough. This forms the basis for the neighborhood data 
