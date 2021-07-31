## Purspose of the Database

The Purpose of this database is to organise the data in a more managable format but moreover, it is to derive business value from the data. The data is available to us in multiple batches of JSON files and JSON is semi-structured data. Feeding all this data into RDBMS gives us the power and flexibility to manange, join, group and query the data to find more direct and actionable budiness insights.

Sparkify is a song music streaming app. Having its data in this form will help it to get information from the data in a way it can improve the user experience and also allow it to predict what the user might or might not like.

## Database Schema Design 

The database is arranged in a star format design, it has four dimension tables and one fact table. This schema makes life easier for Sparkify as the merics impacting the business data can easily be extracted from the songplays table and the related attributes can easily be accessed throught the dimension table. This schema design improves the time and efficiency of the data analytics team to query the database.

## ETL design 

First we export the song data and log data from the JSON files next we transform the required data fields into the form defined in the database, finally we load this data into the tables that we have created through the insert statements. Our ETL pipeliine works nicely as all the data can simply be loaded in the data folders and that data can be easily read and inserted into the respective tables.

## Running Scripts 

While the .ipynb can easily be run using shift + enter, the files `create_tables.py` and `etl.py` have to be run using the terminal. You first have to create the tables using the `create_tables.py` for this you can `cd` into the project directory and use the command `python create_tables.py`. Now, you can run the `etl.py` using `python etl.py` and that should do it.

## File Description 

* sql_queries.py - This file containes all the commands to create, delete the tables and commands to insert data into the tables.

* create_tables.py - This is a file used to create all the tables which are required as per our defined database schema.

* etl.py - This file executed our etl process loading the data from the JSON files parsing them, combining them, transforming the data as reqiured by the tables defined in the create_tables.py and finally, inserting the correct data into their respective tables.