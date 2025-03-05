# 2019 Bay Wheels or Ford GoBike Data Exploration and Visualization


## Dataset

I have selected the 2019 Bay Wheels historical trip data for Data analysis and Visualization for this project.  The dataset consists of 2,506,983 rows and 15 columns and was downloaded as CSV files from the Lyft website. The dataset contains information such as the trip duration, the start and end times of the trip, the start and end stations, user type etc. The dataset as such is pretty clean however, I investigated it further and performed some cleaning on the rows and columns to help with better analysis.


## Summary of Findings

During the exploration, I have checked for duplicate rows and there weren’t any. I created a column to store the trip duration in minutes so it would be easier and precise for analysis (the duration was provided in seconds). I also converted the start time of the trip from string type to datetime object and split this one column into 4 additional columns - date, time, day of the week and month respectively. This enabled me to study the variation of the trip duration on a Daily, Hourly, Weekly and Monthly basis.

As part of the Univariate analysis, I generated different plots to understand which hour/day/month had the highest number of trips. When the trip durations were plotted, it was evident that there were some outliers with really high durations and the corresponding rows were dropped (24,415 rows which is about 0.97% of data). I also plotted a pie chart to understand the types of users and their distribution. There are basically two types of users - Subscribers (members) and Customers (casual or non-member users). I would like to study the trip duration further while also taking into account the user type and how other factors affect it.

Outside of the main variables of interest, I have analyzed which stations were frequently used as the origins and destinations of the trips, the types of rental access methods, the usage of "bike share for all" option etc.

## Key insights for Presentation

 I am interested in further understanding the trends in the trip duration and how the user type, time of the trip affect this for the presentation. Therefore in the bivariate analysis, I plotted a clustered bar chart depicting trip duration for all the days of the week for both Subscribers and Users. It looked like the Subscribers’ trip durations were pretty consistent on a daily basis. This was further confirmed from the Violin plots for average trip duration for each User across all trips. The Violin plot for Subscribers was relatively narrow whereas the Customer’s plot had a longer tail implying outliers. I wanted to further dig into the hourly variation of trip duration for each user type. Therefore, I added a categorical variable to the trip duration and User Type parameters and generated a heat map. From the heatmap, it was interesting to see that although the Subscribers’ trip durations are pretty consistent on a daily basis, they are not so constant throughout a given day. The trip durations gradually increased, reached a maximum and dropped again. This can be verified from the deeper shades of the heatmap for Subscribers. The increase isn’t as high for Customers. 


## Resouces Used
- Lyft page for data download and terminology (https://www.lyft.com/bikes/bay-wheels/system-data)
- Stack Overflow for some errors (https://stackoverflow.com/)
- Pandas Documentation (https://pandas.pydata.org/docs/)
- Matplotlib Documentation (https://matplotlib.org/3.3.2/contents.html)
- Seaborn Documentation (https://seaborn.pydata.org/tutorial.html)
