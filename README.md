# data-sourcing-challenge
Module 6 Challenge - Data Sourcing

## Overview
This program prepares data for a recommendation system to help people find movie reviews and related movies. The code extracts data from two different sources: The New York Times API and The Movie Database, then merges the data together. 

### Detail
1. Access the New York Times API.
    - Create URL for data request
    - Create an empty list to store the reviews retrieved
    - Preview the first five results in JSON format using json.dumps with the argument indent=4 to format the data.
    - Convert list to a Pandas DataFrame using json_normalize()
    - Use the Pandas apply() method and the lambda function
    - Convert column data type from dictionary to string
    - Create list of movie titles to query The Movie Database
2. Access The Movie Databse API.
    - Use titles list created in Part 1 to perform queries with The Movie Database
    - Loop through titles and perform a GET request that sends the title to The Movie Database search and retrieves the JSON results
    - Use the try clause to print out the name of the movie and a message to indicate that the title was found
    - Use the except clause to print out a statement if a movie is not found
    - Preview the first five results in JSON format using json.dumps with the argument indent=4 to format the data
    - Convert the results to a DataFrame with pd.DataFrame()
3. Merge and Clean the Data for Export.
    - Merge the New York Times reviews and TMDB DataFrames on the title column
    - Convert list to string data type and drop certain characters
    - Delete any duplicate rows and reset the index
    - Export data to a CSV file without the DataFrame's index
