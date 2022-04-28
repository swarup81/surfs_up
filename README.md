# surfs_up
# Overview of the analysis:
## purpose:

The project analyzes weather conditions in June and December and draws summary statistics to determine if the surf and ice cream shop business is sustainable year-round.

# Results:

* When we look at the minimum temperatures of June (64) and Dec (56), the dec month has a lower temperature, which may not be suitable for surfing and ice cream.

* There is little more variation in December regarding the standard deviation of June(3.26) and Dec(3.75)months. The temperature range of June is small; hence, it is warmer than dec as the range is large and gets colder.

* The temperatures recorded in Dec (1517) are less when compared to June(1700); still, Dec has a good weather conditions for both surfing and ice cream.

 

#summary:
The weather in June and December are pretty similar; however, December has the lowest temperature compared to June. The range of temperatures in June is warmer than the range of colder temperatures in Dec. Based on June and Dec., Oahu may be a good place for surfing and ice cream shop.

* I want to perform an additional query to gather more weather data for June and December would be the level of precipitation for each month and compare how the precipitation level in the summer and winter impact the surfing and ice cream business.

*Another query would be on temperatures recorded by the station for each month. They can analyze min and max temperature of the nearby station where they want to open the shop. 

<img width="636" alt="Screen Shot 2022-04-28 at 10 54 05 AM" src="https://user-images.githubusercontent.com/100738688/165781829-d07388d3-9dc0-4d21-a531-950f73623775.png">

june_station = session.query(Measurement.tobs, Measurement.station).\
    filter(extract('month',Measurement.date)== 6).all()
    
june_station_df = pd.DataFrame(june_station, columns=['june Temps', 'Station'])
june_station_df

dec_station = session.query(Measurement.tobs, Measurement.station).\
    filter(extract('month',Measurement.date)== 12).all()
    
dec_station_df = pd.DataFrame(june_station, columns=['june Temps', 'Station'])
dec_station_df

<img width="810" alt="Screen Shot 2022-04-28 at 11 11 59 AM" src="https://user-images.githubusercontent.com/100738688/165785250-b1186db5-119c-4006-8413-f7399b5d3b65.png">





