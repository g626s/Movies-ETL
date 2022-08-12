# Movies-ETL

# Project Overiew 
From our previous project, our client Amazing Prime looked over the dataset and requested to keep it updated on a daily basis. Our client required our help to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. We refactored the code from our previous project to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.

# Resources
* Data Sources:
  - movies_metadata.csv
  - ratings.csv
  - wikipedia_movies.json

# Results
* Overview of the Movies and Ratings table created using PostgreSQL and pgAdmin:
  - ![movies_query_overview](https://user-images.githubusercontent.com/107281474/184280702-beedf4e3-6d6e-4e04-bdd2-91f3ed4f3bbc.png)
  - ![ratings_query_overview](https://user-images.githubusercontent.com/107281474/184280721-ab3d5c6a-137e-409d-916e-2533192ca7cb.png)

* Datasets
  - ![movies_query](https://user-images.githubusercontent.com/107281474/184280766-2ac8dfc2-2410-4da5-b68d-1c2bc98e476f.png)
  - ![ratings_query](https://user-images.githubusercontent.com/107281474/184280786-2d886791-cc3f-4342-9b82-921b36ec115c.png)

# Summary & ETL Methods
The ETL pipleine in this project was created by:
* With the knowledge and understanding of Python, Pandas, the ETL process, and code refactoring, we wrote a function that reads in the three data files and creates three separate DataFrames.
* Extract and transform the Wikipedia data so we could merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, use a try-except block to catch errors.
* Extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Then we merged the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, we merged the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.
* Add the movies_df DataFrame and MovieLens rating CSV data to a SQL database.
