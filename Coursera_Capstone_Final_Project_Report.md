# Introduction

Vancouver is one of the Top 10 cities to live in around the world, according to The Economist Intelligence Unit’s 2019 Global Liveability Index. One of my friends would like to move there and open a gym there, but is unsure of where he should open it. He has learned that I am doing a Data Science Certificate program, and is wondering if I could help him do some analysis and see which location in Vancouver may be the best. He wants to make sure there are not too many other gyms/indoor sports facilities located close by already.

# Data

I downloaded the Vancouver neighborhood data from the [Wikipedia site](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_V). This website contains the list of postal codes in British Columbia, Canada, with the borough and neighborhood(s) data under each postal code. I also downloaded the latitude and longitude coordinates for each postal code using the CA.zip file under the [GeoNames.org website](http://download.geonames.org/export/zip/). I scraped the data and combined these together to get the Borough, Neighborhood, Latitude and Longitude data by Postal Code. Since this data contains postal codes/boroughs that are in the British Columbia province, I further narrowed it to only include postal codes that are in the Vancouver Borough. This forms the basis of the Vancouver neighborhood data for the analysis.

![Capstone Course Data](https://user-images.githubusercontent.com/75646781/117221162-9418a780-adbd-11eb-936f-f478776767d9.PNG)

I also used the data from Foursquare to get the nearby venues data for each postal code in the Vancouver neighborhood data. This data is used to determine the most common venue category in each postal code, which helps in the clustering of the neighborhoods.

# Methodology

I explored the Vancouver neighborhoods using Foursquare to get the Top 100 nearby venues data (within 500 meters radius) for each postal code in the Vancouver neighborhood data. I then grouped the results by neighborhood and by taking the mean of the frequency of the occurrence of each venue category. Then I used the Top 10 most common venue categories in each neighborhood for clustering.

I used the k-means model to do the neighborhood clustering. I selected 5 clusters for the analysis.

# Results

![Capstone Course Cluster Map](https://user-images.githubusercontent.com/75646781/117220708-9e867180-adbc-11eb-8387-c2a0c0f7c9d3.PNG)

5 clusters were created from the k-means model. Cluster 0 contains most of the neighborhoods. Cluster 1 has 4 neighborhoods, while Cluster 2 and Cluster 4 only have 1 neighborhood. Cluster 3 has 2 neighborhoods.

# Discussion

I observed that most of the neighborhoods are clustered in Cluster 0. There are a lot of restaurants/coffee shops in that cluster. Sports opportunities, e.g. gyms, yoga studios, parks and trails, are quite common in that cluster. Cluster 1 has 4 neighborhoods, and the most common venue categories are also restaurants. Gyms are not listed in the Top 10 most common venues, and only one neighborhood has yoga studio as the 7th most common venue. Cluster 2 and Cluster 4 only have 1 neighborhood each, and has yoga studio as the Top 3rd and Top 4th most common venue respectively. Cluster 3 has 2 neighborhoods, but it has more sports facilities, e.g. park, yoga studio and field.

Based on the clustering result, I would recommend my friend to look at the neighborhoods in Cluster 1 as the potential location to open his gym, since there doesn't seem to be many others in these neighborhoods.

# Conclusion

Based on the data analysis, I would recommend my friend to look at the neighborhoods in Cluster 1 (postal codes: V6M, V6P, V5W and V5Y) in Vancouver as the potential location to open his gym.
