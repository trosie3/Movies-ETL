 Movies ETL

## Overview of Project
Create a function that cleans data from Wikipedia data, Kaggle metadata, and the MovieLens rating data, and performs the ETL process then adds the data to a PostgreSQL database. This is so others can be sent the final coding, and resources in order to participate in a ‘hackathon.’

### Dependencies used in Jupyter Notebook
- pandas
- numpy
- from SQLalchemy, create_engine
- psycopg2
- time
- re
- json
- from config

## Results 
ETL_clean_kaggle file includes the full function that cleans all the data needed.
ETL_create_database file adjusts the above function to create the PostgreSQL database for anyone’s usage.
Below images show the database built and counts of the two tables pulled in:
 - SELECT COUNT(*) FROM movies;
 ![image]
 - SELECT COUNT(*) FROM ratings;
 ![Imgae]

### Limitations
Some data dropped due to corruption, or less than 10% of column filled, or unable to reformat the data to match the rest of the column. Started with raw data for 7311 movies and ended with data for 6054, in total 83% of the data was kept. This means the analysis performed in the ‘hackathon’ by others would not be on the full dataset however, it is also expected that some data would need to be dropped in cleaning. Given more time, the percentage of kept data could be increased by finding missing data to fill in, fixing corrupted data, and more data in columns could be converted by more complex coding than done here.
