# Movies_ETL

## Project Overview
This project consists of 4 deliverables:
- Deliverable 1: Write an ETL Function to Read Three Data Files
- Deliverable 2: Extract and Transform the Wikipedia Data
- Deliverable 3: Extract and Transform the Kaggle data
- Deliverable 4: Create the Movie Database

## Results

### Deliverable 1
This deliverable consists of a jupyter notebook labeled ETL_function.ipynb. In it a function is written to read inthe three raw data sources and the resulting Dataframes are displayed.

### Deliverable 2
This deliverable consists of a jupyter notebook labeled ETL_clean_wiki_movies.ipynb. In it the function from Deliverable 1 is used to read in the raw data sources. The resulting wiki_movies_df DataFrame is then transformed through the following steps:
- tv shows are filtered out
- IMDB ID's are extracted from links, and duplicates are dropped
- columns with no values are dropped
- the following columns are cleaned:
  - box office column
  - budget column
  - release date column
  - running time column
The final transformed wiki_movies_df DataFrame is then displayed.

### Deliverable 3
This deliverable consists of a jupyter notebook labeled ETL_clean_kaggle_data.ipynb. In it the function from Deliverable 1 is used to read in the raw data. The function from Delvierable 2 is copied over to transform the wiki_movies_df DataFrame. New code is added to clean the Kaggle data and merge it with the Wikipedia data. The resulting movies_df DataFrame is then cleaned. The MovieLen ratings data is extracted and cleaned, then merged with the movies_df DataFrame. The resutling mvies_with_ratings_df DataFrame as well as the movies_df DataFrame are displayed.

### Deliverable 4
This delvierable consists of a jupyter notebook labeled ETL_create_database.ipynb. IN it the functions from Deliverabel 3 are copied in to extract, transform, clean and merge the raw data sources. The movies_df DataFrame as well as the ratings.csv file are then imported into the movie_data DataBase of PostgresSQL. Queries onthe resutling tables are used to confirm that all the data was imported correctly. 

![Movie Query](/Resources/movies_query.png)

![Ratings Query](/Resources/ratings_query.png)
