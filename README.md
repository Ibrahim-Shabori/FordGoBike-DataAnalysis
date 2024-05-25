# Ford GoBike System Data Exploration.

## By Ibrahim Mohamed


## Dataset

This dataset consists of information regarding 1.8M individual rides made in a bike-sharing system covering the greater San Francisco Bay area between (1/1/2018) => (31/12/2018). It includes start and end time, some information about start and end stations ( id, longitude, latitude, name), also there is a column for user type and bike id.

## Summary of Findings

In the exploration, I created two new columns, one to determine the month and the second to determine the day, I used both of them to see how numbers of bike rides differ from month to month and from day to day. For days, I found that at (Sat - Sun) there are the least number of bike rides over the week. For months, I found that at mid-year months (May - October) there are the most number of bike rides across the year. To ensure that, when I seperated each month by user type, both of user types followed the same curve that I previously concluded.

Next, I decide to find the correlation between user type and duration. at the begenning I found that the number of subscribers are 7 times the customers' number. When I plot the relationship between user type and duration, duration scale had a very long tail, so I decided to create a new column to measure duration but in minutes, then I put the duration(min) on a logarithmic scale, I found that customers  have average minutes greater than average minutes for subscribers. Also I found that about 99% of bike rides spent less than 160 minutes.

Outside of the main variables of interest, I found a very strong relationship between start and end stations' longitudes and latitudes, which strongly proved my previous result when I made a column for distance and found out that 99.5% of users, park their bike in a station less than 6km away from start station.

## Key Insights for Presentation

For the presentation, at the begenning I made two bar plots one for months and the second for days to see how numbers of bike rides differ from month to month and from day to day. Next, I wand to see the same plot for months but seperated for each month by user type, to see if there is a difference between the two types or they follow the same trend across the year.
I remove outliers who spent more than 160 min in their trips, then I made a violin plot between user type and duration(min) which was on a logarithmic scale to see how minutes spent in bike trips differ by user type. Also I made a pointplot to see how minutes spent in bike trips differ by user type for each month.
At the end, I made two groups of top stations for each user type, and made a point plot for each group to see the difference in average minutes across the year for each station in both groups.