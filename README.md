# DataModeling_Cassandra    
## Introduction    
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. They'd like a data engineer to create an Apache Cassandra database which can create queries on song play data to answer the questions. More specifically, we need to create tables to perform certain queries given by the analytics team from Sparkify to generate the results.    

## Dataset    
For this project, we will work with one dataset `event_data`. The directory of CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:    
> event_data/2018-11-08-events.csv    
> event_data/2018-11-09-events.csv    
