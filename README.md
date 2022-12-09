# Bikesharing Analysis
## Overview of the analysis
### Purpose
Analyzes NYC Citibike data to help determine if a bike-sharing program in Des Moines is a viable business proposal. Project produced a set of visualizations that:
* Show the length of time that bikes are checked out for all riders and genders.
* Show the number of bike trips for all riders and genders for each hour of each day of the week.
* Show the number of bike trips for each type of user and gender for each day of the week. 

### Resources
The data used in this project was downloaded from the Citi Bike System Data page (https://ride.citibikenyc.com/system-data). This project used data from August 2019. The Citi Bike Trip Histories data includes:
* Trip Duration (seconds)
* Start Time and Date
* Stop Time and Date
* Start Station Name
* End Station Name
* Station ID
* Station Lat/Long
* Bike ID
* User Type (Customer = 24-hour pass or 3-day pass user; Subscriber = Annual Member)
* Gender (Zero = unknown; 1 = male; 2 = female)
* Year of Birth

The raw dataset was imported into Jupyter notebooks for inspection and cleaning. The tripduration column in the dataset was converted from an integer to a datetime datatype to get the time in hours, minutes, seconds using Python and Pandas functions. The DataFrame was then exported as a new csv file without the index. This new csv file was called trip_duration.csv.

## Link to Tableau Dashboard

https://public.tableau.com/app/profile/margo.merritt/viz/BikesharingVisualizationandAnalysis/NYCCitibikeAnalysis?publish=yes

## Results

### Checkout Time for Users - line graph

![checkout time by users](https://user-images.githubusercontent.com/111299372/206586094-4fc6c594-3c64-4370-ab6a-ee4bfdd73088.png)

In the Checkout Time for Users line graph we plot the minutes elapsed per hour on the x-axis and the number of bikes on the y-axis. In August 2019 there were 35,135 rides that had a checkout time of 1 minute, which is the shortest checkout time in this dataset. At minute 5 on the x-axis the graph peaks with 146,752 rides that had a checkout time of 5 minutes. After minute 5 the number of users decreases significantly as the checkout time increases. By minute 25 there are only 33,854 rides lasting for 25 minutes.

### Gender Breakdown - pie chart

![gender breakdown pie chart](https://user-images.githubusercontent.com/111299372/206595000-fc22d283-484e-44d5-8776-8c454063ecd6.png)

This piechart helps us visualize the breakdown of the genders of the CitiBike riders. We can see that the CitiBike riders are clearly male dominated. 

### Checkout Time by Gender - multiple line graph

![checkout time by gender](https://user-images.githubusercontent.com/111299372/206587990-b8b83e2c-de0e-4a46-8755-1b39921d45b5.png)

The Checkout Time by Gender graph the x-axis represents the minutes elapsed per hour and the y-axis represents the number of bikes, similar to 
the Checkout Time by User graph. This graph breaks the users down into three categories based on gender. The three gender categories are male, female, and unknown. For the male category the graph peaks at minute 5 with 108,087 rides. The female category has 34,151 rides at its peak at minute 6. The unkown gender category has 7,389 at its peak at minute 11. 

### Trips by Weekday for Each Hour - heatmap

![trips by weekday for each hour](https://user-images.githubusercontent.com/111299372/206594874-03e1e796-deb8-4418-98a8-756f56fd3e94.png)

The Trips by Weekday for Each Hour displays the weekday stoptime on the columns and the hour stoptime on the rows. A lighter orange color represents the least popular start times. The darkest orange colors represent the most popular start times. From this heatmap we see that there is a peak in activity in the early evening hours starting at 5:00 pm on Monday, Tuesday, Thursday, and Friday. 

### Trips by Gender (Weekday per Hour) - heatmap

![trips by gender (weekday per hour)](https://user-images.githubusercontent.com/111299372/206594888-435fccaf-c226-4733-a5ad-768b25cd88c3.png)

In this heatmap the rows display the hour of the start time. The columns are broken down into the three gender categories by weekday. This visualization shows us at a glance which times are peak times for bike rentals and by which gender. The male category has high usage rates during morning and evening weekdays. This could indicated that men are utilizing bike rentals during their daily commutes. The female category has a peak in usage during weekday commute times as well, but not near as much bike usage as men do. This unequal usage between men and female riders could indicate that women do not feel comfortable riding a bike by themselves during their daily commute. Women could be opting for a transportation option they feel is safer, such as a car ride sharing service for their daily commute. 



### User Trips by Gender by Weekday - heatmap

![user trips by gender by weekday](https://user-images.githubusercontent.com/111299372/206594966-021ed2b9-ebac-4240-9882-27b4f623aafd.png)

This heatmap further drills down the data by displaying the usertype per gender type. There are two usertypes: customer and subscribers. Customers refer to short-term customers with either a 24-hour pass or a 3-day pass. Subscribers are riders who have an annual subscription to the Citi Bike Service. From this visualization we see that the highest usage rate comes from male subscribers. Within the male subscriber sub-category we see that their highest usage rates are during the weekdays, with the weekends having lower usage rates. This could indicate that male subscribers are using their citibike subscription as their primary form of transportation for their weekday commutes, but sometimes utilize the service on the weekdays as well for other reasons. 


## Summary

These 7 visualizations helped us see the current demographics of CitiBike users in NYC. From these different graphs we were able to determine that peak times for CitiBike usage is weekday mornings and evenings. This indicates that these riders are likely using these bikes for their daily commute to and from work. In "User Trips by Gender by Weekday" graph we were able to further determine that the largest sub-category of riders are male subscribers. 

There are more visualizations that can be made to help us draw more conclusions on our given dataset. The graph "Checkout Time for Users" displayed the length of the checkout time for all users: short-term customers and annual subscibers. Recreating this graph and filtering it for short-term customers or annual subscribers will give more insight into the two different usertypes. 

### Checkout Times for Short-Term Customers 

![checkout times short-term customers](https://user-images.githubusercontent.com/111299372/206786935-cadc29ff-9cf6-498d-9ad6-7425c2610c8c.png)

### Checkout Times for Annual Subscribers

![checkout times annual subscribers](https://user-images.githubusercontent.com/111299372/206786978-6fc8fd32-5886-4123-a433-823b8c7d23da.png)

