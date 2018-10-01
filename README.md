# Aggregating-SQL-

1: What was the hottest day in our data set? Where was that?

SELECT
   
   zip,
   date,
    
   MAX(maxtemperaturef) as max_temp
FROM
   
   weather

GROUP BY zip, date

ORDER BY max_temp DESC

Output : "2015-11-17"	"94063"	"134"


2:How many trips started at each station?

SELECT
   
   start_station,
    
   COUNT(*) AS trip_count

FROM
   
   trips

GROUP BY 1


Output: There were 80 unique stations, and the number of trips per station ranges from 1 to 23,591.


3:What's the shortest trip that happened?

SELECT
   
   MIN(duration) AS shortest_trip

FROM
    
   trips


Output: The shortest trip duration is 60 seconds
 
 
 4:What is the average trip duration, by end station?
 SELECT
    
   end_station,
    
   AVG(duration) as average_duration

FROM
   
   trips

GROUP BY 1
 

Output:The average trip duration, aggregated by end station, ranges from 257 to 4710.9.
