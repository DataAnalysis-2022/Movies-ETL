# Movies-ETL



### Background

The movie dataset and the database need to be updated daily.  In order to do this, we will write a function to perform the data retrieval, data cleaning and transformation and data upload to a database.  We will create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.



### Results

1. ##### Write an ETL Function to Read Three Data Files

​		The function converts the Wikipedia JSON file to a Pandas DataFrame, shown as the following:

![image-20220803203056986](Resources\image-20220803203056986.png)



​		The function converts the Kaggle metadata file to a Pandas DataFrame, as shown below:

![image-20220803202831040](Resources\image-20220803202831040.png)



​		The function converts the MovieLens ratings data file to a Pandas DataFrame, as shown below:

![image-20220803203211226](Resources\image-20220803203211226.png)



2. ##### Extract and Transform the Wiki Data

   Cleaned wiki data is shown here:

   ![image-20220803203504652](Resources\image-20220803203504652.png)

​		The columns are shown below:

![image-20220803203616737](Resources\image-20220803203616737.png)



3. ####  Extract and Transform the Kaggle Data

​		The movie data is shown below:

![image-20220803203817656](Resources\image-20220803203817656.png)



​	The movie data with rating is here to show the ratings (the index and imdb_id was cut off from the screen capture):

![image-20220803204022335](Resources\image-20220803204022335.png)

4. #### Create the Movie Database

​		The movie and rating data was transferred into postgreSQL database.  The row counts are:

![movies_query](Resources\movies_query.png)

![ratings_query](Resources\ratings_query.png)



​	The time lapse for loading the data is:

![image-20220803211349671](Resources\image-20220803211349671.png)