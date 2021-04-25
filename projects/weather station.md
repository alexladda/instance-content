# Weather Station

*This could be the seen as the MVP for [this whole project](/architecture). Realtime data is just about extracted, stored, slightly analysed and then displayed.*

<img alt='plot of the temp in the last 24hrs' src='/plots/plot.svg'/>

So where does this Graph come from? And why does it load so slowly? It is actually generated in realtime and does not exist as a physical image file on the server:

1. The http request for the image file triggers a function to fetch data from the database.
2. The database returns temperature Data from the last 24 hrs.
3. The function then generates a simple plot of the local temperature

Since the database and this web server are running on two different machines, so it does take some time. So for once I do enjoy when it takes a while to load.

## So what does the ETL look like?

You can find it [here on GitHub](https://github.com/alexladda/airflow-etl/blob/main/dags/weather_station.py) by the way

The API I'm using is from [Open Weather Map](https://openweathermap.org). It provides extensive Weather Data - past, current and prediction. While that would also be fun, I do want to access it's current live data.

I query the API every 5 minutes and usually get the same Dataset about two to three times before it updates to the next one. The JSON is varying and feels a bit messy, but that's just life isn't it?
