# Data

I downloaded the Vancouver neighborhood data from the [Wikipedia site](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_V). This website contains the list of postal codes in British Columbia, Canada, with the borough and neighborhood(s) data under each postal code. I had to scrape the data from the website to get it in the right format and put it in a dataframe.

![Data 1](https://user-images.githubusercontent.com/75646781/117233117-57f24080-add7-11eb-8392-bd5af3e29e87.PNG)

I also downloaded the latitude and longitude coordinates for each postal code using the CA.zip file under the [GeoNames.org website](http://download.geonames.org/export/zip/). I needed the coordinates to explore the neighborhoods in Foursquare later, and this data is not included in the above Wiki data. 

![Data 2](https://user-images.githubusercontent.com/75646781/117233419-f2eb1a80-add7-11eb-8950-944d2e674026.PNG)

Since I only needed the PostalCode and coordinates data from the CA.zip file, I extracted only the data necessary and made another dataframe.

![Data 3](https://user-images.githubusercontent.com/75646781/117233600-49585900-add8-11eb-9143-13f0f78e11bb.PNG)

Then, I combined these two dataframes together to get the Borough, Neighborhood, Latitude and Longitude data by Postal Code. 

![Data 4](https://user-images.githubusercontent.com/75646781/117233703-802e6f00-add8-11eb-8aed-70e482dd4249.PNG)

Since this data contains postal codes/boroughs that are in the British Columbia province, I further narrowed it to only include postal codes that are in the Vancouver Borough. This forms the basis of the Vancouver neighborhood data for the analysis.

![Capstone Course Data](https://user-images.githubusercontent.com/75646781/117221162-9418a780-adbd-11eb-936f-f478776767d9.PNG)

I also used the data from Foursquare to get the nearby venues data for each postal code in the Vancouver neighborhood data. This data is used to determine the most common venue category in each postal code, which helps in the clustering of the neighborhoods. Below is the first 5 rows of the venues dataframe when I ran the request to get the Top 100 venues within 500 meters of each of the Vancouver neighborhoods. 

![Data 5](https://user-images.githubusercontent.com/75646781/117233877-ce437280-add8-11eb-8715-d000765fec0b.PNG)
