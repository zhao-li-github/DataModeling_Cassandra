# DataModeling_Cassandra    
## Introduction    
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. They'd like a data engineer to create an Apache Cassandra database which can create queries on song play data to answer the questions. More specifically, we need to create tables to perform certain queries given by the analytics team from Sparkify to generate the results.    

## Dataset    
For this project, we will work with one dataset `event_data`. The directory of CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:    
> event_data/2018-11-08-events.csv    
> event_data/2018-11-09-events.csv    
These files will be first processed to create the data file `event_datafile_new.csv` that will be used for Apache Casssandra tables. Here's a screenshot of the first 10 rows in this csv data file:   
![image](https://user-images.githubusercontent.com/60242372/120720655-53c24d00-c481-11eb-9262-f55a66b3ffdd.png)

## Queries    
For each of the three given queries, I'll design tables accordingly to get the results.
#### Query 1 
Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4
#### Query 2
Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182
#### Query 3
Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'
