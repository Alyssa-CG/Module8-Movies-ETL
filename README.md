# Movies ETL

## Project Overview

"Amazing Prime" is hosting a hackathon and needs clean datasets to provide to its contestants. Using the Extract, Transform and Load (ETL) method, data from several sources was processed and prepared. Now, the process must be streamlined into a function for future use.

## Resources

* Data: JSON and .csv files:
    * Wikipedia Movies JSON (from class files)
    * [Movies Metadata from Kaggle](https://www.kaggle.com/rounakbanik/the-movies-dataset/data?select=movies_metadata.csv)
    * [Movies Ratings data from Kaggle](https://www.kaggle.com/rounakbanik/the-movies-dataset/data?select=ratings.csv)

* Software:
    * macOS Catalina v 10.15.5
    * PostgreSQL 12
    * pgAdmin [v4.14](https://www.postgresql.org/ftp/pgadmin/pgadmin4/)
    * Python 3.7.7
    * Jupyter Notebook 6.0.3
    
## Assumptions

Several assumptions are being made in automating this process, including the following:
1. That the individual deploying the code in the future reads the comment at the beginning of the script providing SQL to 
"DELETE FROM table_name;"
before running the function to transform and load the new data.
2. That all loaded data files will be saved in the same location and named the exact name as the previous iteration.
3. That data sources will remain reasonably unchanged over future iterations or they make break the function.
4. That data sources will retain the identical column headers in the future.
5. That the strange outlier such as the badly merged 2006 movie will be caught if present in future iterations, but other kinds of badly merged outlier data likely not be caught by the function.
6. That Kaggle will remain the source of more consistent and accurate information- the function is set to prioritise Kaggle data and use Wikipedia data if Kaggle data is missing for ALL duplicated columns.
