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

## Results

### Checkout Time for Users - line graph

![checkout time by users](https://user-images.githubusercontent.com/111299372/206586094-4fc6c594-3c64-4370-ab6a-ee4bfdd73088.png)

In the Checkout Time for Users line graph we plot the number of bikes on the y-axis and the minutes elapsed per hour on the x-axis. In August 2019 there were 35,135 rides that had a checkout time of 1 minute, which is the shortest checkout time in this dataset. At minute 5 on the x-axis the graph peaks with 146,752 rides that had a checkout time of 5 minutes. After minute 5 the number of users decreases significantly as the checkout time increases. By minute 25 there are only 33,854 rides lasting for 25 minutes.

### Checkout Time by Gender - multiple line graph

![checkout time by gender](https://user-images.githubusercontent.com/111299372/206587990-b8b83e2c-de0e-4a46-8755-1b39921d45b5.png)


## Summary
