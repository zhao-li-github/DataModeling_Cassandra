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
> Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4      

To perform query 1, table `songplays1` is created with the following columns:    
> Column 1 = artist_name    
> Column 2 = song_title    
> Column 3 = song_length    
> Column 4 = session_id    
> Column 5 = item_session    
> Primary key = (session_id, item_session)    

#### Query 2
> Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182    
To perform query 2, table `songplays2` is created with the following columns:
> Column 1 = artist_name
> Column 2 = song_title
> Column 3 = user_id
> Column 4 = user_fname
> Column 5 = user_lname
> Column 6 = session_id
> Column 7 = item_session
> Primary key = ((user_id, session_id), item_session)
#### Query 3
> Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'     
To perform query 3, table `songplays3` is created with the following columns:
> Column 1 = song_title
> Column 2 = user_id
> Column 3 = user_fname
> Column 4 = user_lname
> Primary key = (song_title, user_id)
