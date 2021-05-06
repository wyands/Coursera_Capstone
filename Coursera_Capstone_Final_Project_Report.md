# Introduction

Vancouver is one of the Top 10 cities to live in around the world, according to The Economist Intelligence Unit’s 2019 Global Liveability Index. One of my friends would like to move there and open a gym there, but is unsure of where he should open it. He has learned that I am doing a Data Science Certificate program, and is wondering if I could help him do some analysis and see which location in Vancouver may be the best. He wants to make sure there are not too many other gyms/indoor sports facilities located close by already.

The target audience of this problem is my friend, who is looking to invest in opening a gym. He cares about this problem because if he picks a location that has too many other gyms already, he may not get enough customers for him gym, and may end up losing his money investing in the gym.

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

# Methodology

I explored the Vancouver neighborhoods using Foursquare to get the Top 100 nearby venues data (within 500 meters radius) for each postal code in the Vancouver neighborhood data.

![Data 5](https://user-images.githubusercontent.com/75646781/117233877-ce437280-add8-11eb-8715-d000765fec0b.PNG)

I then grouped the results by neighborhood and by taking the mean of the frequency of the occurrence of each venue category. 

![Data 6](https://user-images.githubusercontent.com/75646781/117240067-df927c00-ade4-11eb-9043-675fad221fbe.PNG)

Then I used the Top 10 most common venue categories in each neighborhood for clustering.

![Data 7](https://user-images.githubusercontent.com/75646781/117240114-fa64f080-ade4-11eb-92e6-1433706a24c2.PNG)

I used the k-means model to do the neighborhood clustering. I selected 5 clusters for the analysis.

![Data 8](https://user-images.githubusercontent.com/75646781/117240219-3435f700-ade5-11eb-9aa0-daabd40480cd.PNG)

# Results

![Capstone Course Cluster Map](https://user-images.githubusercontent.com/75646781/117220708-9e867180-adbc-11eb-8387-c2a0c0f7c9d3.PNG)

5 clusters were created from the k-means model. Cluster 0 contains most of the neighborhoods. Cluster 1 has 4 neighborhoods, while Cluster 2 and Cluster 4 only have 1 neighborhood. Cluster 3 has 2 neighborhoods.

# Discussion

I observed that most of the neighborhoods are clustered in Cluster 0. There are a lot of restaurants/coffee shops in that cluster. Sports opportunities, e.g. gyms, yoga studios, parks and trails, are quite common in that cluster. Cluster 1 has 4 neighborhoods, and the most common venue categories are also restaurants. Gyms are not listed in the Top 10 most common venues, and only one neighborhood has yoga studio as the 7th most common venue. Cluster 2 and Cluster 4 only have 1 neighborhood each, and has yoga studio as the Top 3rd and Top 4th most common venue respectively. Cluster 3 has 2 neighborhoods, but it has more sports facilities, e.g. park, yoga studio and field.

Based on the clustering result, I would recommend my friend to look at the neighborhoods in Cluster 1 as the potential location to open his gym, since there doesn't seem to be many others in these neighborhoods.

# Conclusion

Based on the data analysis, I would recommend my friend to look at the neighborhoods in Cluster 1 (postal codes: V6M, V6P, V5W and V5Y) in Vancouver as the potential location to open his gym.
