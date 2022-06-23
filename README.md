# Arrival Delays in Atlanta Flights
## by Micah Costello


## Dataset

The dataset consists of 440,000 domestic flights to and from Atlanta, Georgia, from 1987 to 2008. During cleaning, many rows were dropped because they corresponded to cancelled or diverted flights. After cleaning, 431,377 rows remained. Each entry contains information on the flight, such as origin, destination, departure and arrival times and dates, airplane and carrier information, and delay duration and types. 

The data is a sample from the larger dataset found here: https://community.amstat.org/jointscsg-section/dataexpo/dataexpo2009. Since the original dataset contains flights from all domestic destinations and origins, I had to perform preliminary wrangling to obtain a sample of flights to and from Atlanta. 

Due to the large file sizes for the original data zip and the csv files I created during cleaning, I have decided not to include these in the repository. However, since the data is readily available from the aforementioned link, there should be no problem for following along and recreating the cleaned and wrangled files.




## Summary of Findings

In my exploration, I found a strong linear relationship between departure delay and arrival delay, which lead me to theorize that most arrival delays are in part caused before takeoff. The linear shape is broken, however, when arrival delay is around 0. Further investigation showed that for all flights with a departure delay of 0 and a delay type recorded (some rows have no recorded explanation for delay), the only delay type is NAS. NAS delays also make up most of the rows where the departure delay was minimal.

I also found a relationship between month, or season, and arrival delays. Both the winter and summer months have higher median arrival delays, and higher occurrences of all delay types. Spring and fall, on the other hand, have less delay. This trend can't be attirbuted to there being more flights during those months. Aside from October, November and December, the months have virtually equal counts in the dataset. 

There were differences in arrival delay by carrier and airport, but in general, they were not practically significant. The fact that LAX had such a high median arrival delay as a destination, however, lead me to investigate more. I found that in general, that airport has a hihger proportion of delays caused by carrier and NAS than the dataset at large. Checking LAX's interaction with the carrier against arrival delay, however, yielded no interesting findings. I followed up by checking arrival delays in LAX as destination by season, and found that arrival delay spikes greatly in winter there, and not so much at the other airports with high arrival delays. 

I also wanted to see how Atlanta performed as a destination vs. as an origin in terms of arrival delay, and determined that the distribution is almost the same in both cases. 


## Key Insights for Presentation

In my presentation, I focus on the  strong relationships I found between arrival delays and the following variables: departure delay, NAS delay, and month. I also expound upon the high arrival delays that occur when the destination airport is LAX. The variables that do not correlate, as well as interesting findings that were not related to the arrival delay variable, have been left out. 

I begin by plotting the distribution of the arrival delay variable. The normal plot and the zoomed plot are placed side by side so that the reader can see the range of the variable as well as the bulk of the data. I then move onto to the relationship between departure delay and arrival delay. The rudimentary plot of the two variables allows me to segue into the multivariate plot that shows the relationship between departure delays, arrival delays and NAS delays. Then I look at how arrival delays differ across months, and finally, I show how arrival delays vary at LAX (and other airports) across seasons.

Other than juxtaposing the two graphs of arrival delay's distribution, I also modified the font size of certain graphs to make them more legible, and I added a more descriptive title to the multivariate NAS/departure/arrival delay graph to clarify its purpose. 
