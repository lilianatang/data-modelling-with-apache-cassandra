# INTRODUCTION
### Purpose of the project:
This project is to create an Apache Cassandra database which can create queries on song play data to answer the questions by the analytics team from Sparkify. 
### What is Sparkify?
Sparkify is a startup that just launched a music streaming application. The application has collected events data in CSV format. Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.
### How this project is going to help Sparkify
This project will help the analytics team at Sparkify easily run SQL queries to understand their end users more.
# DATABASE SCHEMA DESIGN & ETL PROCESS
### Modeling NoSQL Apache Cassandra database
1. Design tables to answer the queries provided by the analytics team
##### Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4
##### Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182
##### Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'
2. Write Apache Cassandra CREATE KEYSPACE and SET KEYSPACE statements
3. Develop CREATE statements for each of the tables to address each question
4. Load the data with INSERT statement for each of the tables
5. Include IF NOT EXISTS clauses in CREATE statements to create tables only if the tables do not already exist. 
6. Test by running the proper select statements with the correct WHERE clause
### Building ETL Pipeline
1. Iterate through each event file in event_data to process and create a new CSV file in Python
2. Load processed records into relevant tables in your data model
3. Test by running SELECT statements after running the queries on the database
# FILES IN REPOSITORY
* Project_1B_ Project_Template.ipynb reads and processes CSV files from event_data folder, and built the ETL pipeline to answer the queries provided by the analytics team.
