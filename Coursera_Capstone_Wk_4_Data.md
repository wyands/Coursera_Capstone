# Data

I downloaded the Vancouver neighborhood data from the [Wikipedia site](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_V). This website contains the list of postal codes in British Columbia, Canada, with the borough and neighborhood(s) data under each postal code. I also downloaded the latitude and longitude coordinates for each postal code using the CA.zip file under the [GeoNames.org website](http://download.geonames.org/export/zip/). I scraped the data and combined these together to get the Borough, Neighborhood, Latitude and Longitude data by Postal Code. Since this data contains postal codes/boroughs that are in the British Columbia province, I further narrowed it to only include postal codes that are in the Vancouver Borough. This forms the basis of the Vancouver neighborhood data for the analysis.

![Capstone Course Data](https://user-images.githubusercontent.com/75646781/117221162-9418a780-adbd-11eb-936f-f478776767d9.PNG)

I also used the data from Foursquare to get the nearby venues data for each postal code in the Vancouver neighborhood data. This data is used to determine the most common venue category in each postal code, which helps in the clustering of the neighborhoods.
