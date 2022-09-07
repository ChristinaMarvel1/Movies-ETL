## Deliverable 1: Write an ETL Function to Read Three Data Files
Deliverable 1 Instructions
Using your knowledge of Python, Pandas, the ETL process, and code refactoring, write a function that reads in the three data files and creates three separate DataFrames.


Lesson 8.2.1: Load and extract the Wikipedia data
Lesson 8.2.2: Extract the Kaggle Data
Download the ETL_Deliverable1_starter_code.ipynb file, add it to your Movies-ETL GitHub folder, and rename the file ETL_function_test.ipynb. Follow the instructions below to refactor the code from this module as indicated by the numbered comments in the starter code file.

1. In Step 1, create a function to read in the three files and give it a name.
2. In Step 2, read in the Kaggle metadata and MovieLens ratings CSV files as Pandas DataFrames.
![1-1 2](https://user-images.githubusercontent.com/107659667/188772363-8391920e-0d00-4b08-bafd-d7c789cc603b.jpg)


3. In Step 3, open the Wikipedia JSON file and use the json.load() function to convert the JSON data to raw data.
![1-3](https://user-images.githubusercontent.com/107659667/188772384-2f4920b0-010b-47df-8fa9-f929da5eb458.jpg)


4. In Step 4, read in the raw Wikipedia movie data as a Pandas DataFrame.
![1-4](https://user-images.githubusercontent.com/107659667/188772412-7de5a4c0-fe9c-42b3-ab25-6bd4ea76b520.jpg)


5. In Step 5, use the code provided to return the three DataFrames.
![1-5](https://user-images.githubusercontent.com/107659667/188772419-d72729a3-a11c-477f-8f73-0b77dd249f25.jpg)


6. In Step 6, use the variables provided to create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
7. In Step 7, set the three variables in Step 6 equal to the function created in Step 1.
![1-6 7](https://user-images.githubusercontent.com/107659667/188772438-b0a3f3b8-f253-4a93-932d-2b960658069c.jpg)


8. In Step 8, set the DataFrames from the return statement equal to the file names in Step 6. In this step, you are reassigning the variables created in Step 6 to the variables in the return statement.
![1-8](https://user-images.githubusercontent.com/107659667/188772456-90088385-420e-4ffd-815a-23e8567de381.jpg)


In Steps 9-11, check that all three files are converted to a DataFrame. See the images below for confirmation:
The wiki_movies_df DataFrame
 The first five rows of the wiki_movies_df DataFrame.

The kaggle_metadata DataFrame
 The first five rows of the kaggle_metadata DataFrame.

The ratings DataFrame
The ratings DataFrame.
![1-9](https://user-images.githubusercontent.com/107659667/188772526-c7e07fcc-8086-450e-928e-89d2f7aeb97a.jpg)
![1-10](https://user-images.githubusercontent.com/107659667/188772530-020ca50c-cfe0-4161-8724-196b7a3418b3.png)
![1-11](https://user-images.githubusercontent.com/107659667/188772534-73e22d66-2771-4a58-aa23-639a62576bd4.jpg)


## Deliverable 2 Instructions
Using your knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Wikipedia data so you can merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, use a try-except block to catch errors.


1. In Step 1, add the code from this module for the clean movie function that takes in the argument "movie".
![2-1](https://user-images.githubusercontent.com/107659667/188772811-23c12c46-de8c-47a4-a2c3-75d61c9c4be2.jpg)

2. In Step 2, add the function you created in Deliverable 1 that reads in the three data files.
![2-2](https://user-images.githubusercontent.com/107659667/188772816-1050efd7-9fe3-4c02-9cbb-6576e2f14791.jpg)

3. In Step 3, inside the function you created in Deliverable 1, remove the code that creates the wiki_movies_df DataFrame from the wiki_movies_raw file, then write a list comprehension that filters out TV shows from the wiki_movies_raw file.
![2-3](https://user-images.githubusercontent.com/107659667/188772824-54b3523a-ac3f-49b6-93bc-34f584dcc207.jpg)

4. In Step 4, write a list comprehension to iterate through the cleaned wiki movies list that you created in Step 3.
![2-4](https://user-images.githubusercontent.com/107659667/188772832-033f74e8-770d-4e94-b913-5d8cd2b2acfe.jpg)

5. In Step 5, read in the cleaned movies list from Step 4 as a DataFrame.
![2-5](https://user-images.githubusercontent.com/107659667/188772839-4adcfea3-248d-4659-a62e-dca73208a3c4.jpg)

6. In Step 6, write a try-except block that will catch errors while extracting the IMDb IDs with a regular expression string and dropping any imdb_id duplicates. If there is an error, capture and print the exception.
![2-6](https://user-images.githubusercontent.com/107659667/188772862-9b328af3-3c62-435e-b3b4-0ef9e9053898.jpg)

7. In Step 7, write a list comprehension to keep the columns that have non-null values from the DataFrame created in Step 5, then create a wiki_movies_df DataFrame from the list.
![2-7](https://user-images.githubusercontent.com/107659667/188772869-0bd354b8-b0ec-405f-bef8-111ed3da1d73.jpg)

8. In Step 8, create a variable that will hold all the non-null values from the "Box office" column.
![2-8](https://user-images.githubusercontent.com/107659667/188772879-16c819da-9102-4263-bb56-5644bb9ed30d.jpg)

9. In Step 9, convert the box office data created in Step 8 to string values using the lambda and join functions.
![2-9](https://user-images.githubusercontent.com/107659667/188772884-e398e889-5255-4f21-b70e-e9337473a39b.jpg)

10. In Step 10, write a regular expression to match the six elements of form_one of the box office data.

11. In Step 11, write a regular expression to match the three elements of form_two of the box office data.
![2-10 11](https://user-images.githubusercontent.com/107659667/188772887-cdeadf8a-754f-4665-8fbe-6be6970f43c6.jpg)

12. In Step 12, add the parse_dollars() function.
![2-12](https://user-images.githubusercontent.com/107659667/188772896-3be546ce-52ed-4cca-a9ba-2c44f26a8a21.jpg)

13. In Step 13, add the code that cleans the box office column in the wiki_movies_df DataFrame using the form_one and form_two lists created in Steps 10 and 11, respectively.
![2-13](https://user-images.githubusercontent.com/107659667/188772905-86a11005-1f86-473c-ae8f-72e909844eea.jpg)

14. In Step 14, add code that cleans the budget column in the wiki_movies_df DataFrame.
![2-14](https://user-images.githubusercontent.com/107659667/188772918-dac1560a-8783-4633-9328-7830aaf73b47.jpg)

15. In Step 15, add code that cleans the release date column in the wiki_movies_df DataFrame.
![2-15](https://user-images.githubusercontent.com/107659667/188772931-5f990e63-d587-46d4-a419-f35b7040e9f2.jpg)

16. In Step 16, add code that cleans the running time column in the wiki_movies_df DataFrame.
![2-16](https://user-images.githubusercontent.com/107659667/188772936-d7288cc3-1bad-4349-86d3-50751589650d.jpg)

17. In Step 17, use the variables provided to create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
![2-17](https://user-images.githubusercontent.com/107659667/188772939-bd7fb190-d6aa-4ba6-ac00-05ea22a6a1a7.jpg)

18. In Step 18, set the three variables in Step 17 equal to the function created in Deliverable 1.
![2-18](https://user-images.githubusercontent.com/107659667/188772944-8d655b5b-34ad-4017-bcea-87eb0ac8c754.jpg)

19. In Step 19, set the wiki_movies_df equal to the wiki_file variable.
![2-19](https://user-images.githubusercontent.com/107659667/188772950-82d76af7-58d6-41df-968c-b8d94bb157e3.jpg)

20. In Step 20, check that your wiki_movies_df DataFrame looks like this image:
The ratings DataFrame.
![2-20](https://user-images.githubusercontent.com/107659667/188772953-a39c80f6-f2b0-417f-b0d4-b78e7bc12847.jpg)

21. In Step 21, add the columns from wiki_movies_df DataFrame to a list, and confirm that they are the same as this image:
 The columns of the wiki_movies_df DataFrame.
![2-21](https://user-images.githubusercontent.com/107659667/188772963-46248e41-2599-4213-b4da-c5697f73c507.jpg)

## Deliverable 3: Extract and Transform the Kaggle Data (30 points)
Deliverable 3 Instructions
Using your knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Then, you’ll merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, you’ll merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.


![3-0](https://user-images.githubusercontent.com/107659667/188772995-f6dc85ac-cb4b-454c-99d5-d9390c830821.jpg)

1. In Step 1, add the function you created in Deliverable 1 that reads in the three data files and creates the kaggle_metadata and ratings DataFrames.
![3-1](https://user-images.githubusercontent.com/107659667/188773176-b746dc5f-12c6-4f90-ac5b-bcdb0a929302.jpg)

Before Step 2, add all the code you wrote for Deliverable 2.
![3-1-1](https://user-images.githubusercontent.com/107659667/188773187-063adf2a-65d0-4bda-b545-ef53afbdbda3.jpg)
![3-1-2](https://user-images.githubusercontent.com/107659667/188773200-3287943c-a0f8-47dc-b4d7-9c5845ac0fce.jpg)

2. In Step 2, below the code that cleans the running time column in the wiki_movies_df DataFrame from Deliverable 2, add the code that cleans the Kaggle metadata.
![3-2](https://user-images.githubusercontent.com/107659667/188773205-209b1db5-4ad5-4317-acf1-e849e711870a.jpg)

3. In Step 3, merge the wiki_movies_df DataFrame and the kaggle_metadata DataFrames, then name the new DataFrame, movies_df.
![3-3](https://user-images.githubusercontent.com/107659667/188773212-421a1a99-c286-49dc-8389-76b03d442828.jpg)

4. In Step 4, drop unnecessary columns from the movies_df DataFrame.

5. In Step 5, add the fill_missing_kaggle_data() function that fills in the missing Kaggle data on the movies_df DataFrame.
![3-5](https://user-images.githubusercontent.com/107659667/188773227-0024a219-be76-49a6-bac6-d824452708b7.jpg)

6. In Step 6, call the fill_missing_kaggle_data() function with the movies_df DataFrame and the Kaggle and Wikipedia columns to be cleaned as the arguments.

7. In Step 7, filter the movies_df DataFrame to keep the necessary columns.
![3-7](https://user-images.githubusercontent.com/107659667/188773273-b3c83285-6ede-47e9-8db2-3cc2c8d30589.jpg)

8. In Step 8, rename the columns in the movies_df DataFrame.
![3-8](https://user-images.githubusercontent.com/107659667/188773290-eaa2d27d-b87a-4e10-ac84-91f82551c900.jpg)

9. In Step 9, transform and merge the ratings DataFrame with the movies_df DataFrame, name the new DataFrame movies_with_ratings_df, then clean the movies_with_ratings_df DataFrame.
![3-9](https://user-images.githubusercontent.com/107659667/188773302-84ec365f-fe8d-426e-8e9e-875295e85c6e.jpg)

10. In Step 10, use the variables provided to create a path to the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
![3-10](https://user-images.githubusercontent.com/107659667/188773313-b448abac-b061-467f-8763-a8777b5d47ef.jpg)

11. In Step 11, set the three variables from Step 17 of Deliverable 2 equal to the function created in Deliverable 1.
![3-11](https://user-images.githubusercontent.com/107659667/188773319-0a6a4844-0e4b-4170-87ff-c5257ce750f6.jpg)

12. In Step 12, set the DataFrames from the return statement after Step 9 equal to the file names in Step 11.
![3-12](https://user-images.githubusercontent.com/107659667/188773330-6aee1b39-12eb-4eb8-abb9-e4c0b45ed782.jpg)

13. In Step 13, check that your wiki_movies_df DataFrame is the same as in Deliverable 2.
![3-13](https://user-images.githubusercontent.com/107659667/188773341-7de777d1-8dea-494c-898e-e34d47e40fd2.jpg)

14. In Step 14, check that your movies_with_ratings_df DataFrame looks like this image:
The first five rows of the movies_with_ratings_df DataFrame.
![3-14](https://user-images.githubusercontent.com/107659667/188773349-9a94bd29-ddd8-4280-98a4-bb8a8fcdd69a.jpg)

15. In Step 15, check that your movies_df DataFrame looks like this image:
The first five![3-15](https://user-images.githubusercontent.com/107659667/188773360-c84d4706-a40a-4e97-b2bf-10d6096eac42.jpg)
 rows of the movies_df DataFrame.


Deliverable 4 Instructions
Use your knowledge of Python, Pandas, the ETL process, code refactoring, and PostgreSQL to add the movies_df DataFrame and MovieLens rating CSV data to a SQL database.



In the first cell, uncomment the # from config import db_password so this code is working.
Remove the return statement, return wiki_movies_df, movies_with_ratings_df, movies_df.
After Step 9, Transform and merge the ratings DataFrame, add the code to create the connection to the PostgreSQL database, then add the movies_df DataFrame to a SQL database.
Hint: Use 'replace' for the if_exists parameter so that the movies_df DataFrame data won't be added to the table again.

Before reading in the MovieLens rating CSV data, drop the ratings table in pgAdmin.
Add the code that prints out the elapsed time to import each row.
Refactor Step 11 of Deliverable 3 so that you pass in the variables for the files created in Step 10 of Deliverable 3 in the function created in Deliverable 1.
Run the program.
After the program has finished, run a query on the PostgreSQL database that retreives the number of rows for the movies and ratings tables.
After you confirm that the movies table has 6,052 rows and the ratings table has 26,024,289 rows, take a screenshot of each query and the output, then save them as movies_query.png and ratings_query.png, respectively.
Save the ETL_create_database.ipynb file in your Movies-ETL GitHub folder.
Save the movies_query.png and ratings_query.png files in the Resources folder.

![4-1](https://user-images.githubusercontent.com/107659667/188773457-89970bb2-999d-4164-9056-60b803feb37a.jpg)
![4-2](https://user-images.githubusercontent.com/107659667/188773463-f288d972-d3f6-490e-86e6-c828bf3b260a.jpg)
![4-3](https://user-images.githubusercontent.com/107659667/188773471-3b8c02a1-e4d4-4323-88f6-e0f522733a75.jpg)
![4-5](https://user-images.githubusercontent.com/107659667/188773477-09205dc4-e18a-435d-89ce-708e778c34e9.jpg)
![4-6](https://user-images.githubusercontent.com/107659667/188773482-c174cc4a-3847-4b25-a407-539ae5266bc0.jpg)
![4-7](https://user-images.githubusercontent.com/107659667/188773494-d45b29df-1338-43d1-a384-34930d55576f.jpg)
![4-8](https://user-images.githubusercontent.com/107659667/188773537-dfa093b8-a80f-4e64-aa62-fc544aba9192.jpg)
![4-9](https://user-images.githubusercontent.com/107659667/188773542-bb6239e2-32b2-4b9e-baca-466f3899a694.jpg)
![4-10](https://user-images.githubusercontent.com/107659667/188773547-c567ffd7-6f66-4b06-b33b-bda69e9189b0.jpg)
![4-11](https://user-images.githubusercontent.com/107659667/188773550-a13a92d0-ae11-4de7-99ef-4cb437b55c2d.jpg)
![4-12](https://user-images.githubusercontent.com/107659667/188773556-de8e8ce7-74a0-41ef-9a78-6c5ebd5d71ad.jpg)
![4-13](https://user-images.githubusercontent.com/107659667/188773563-27ee269a-7f4d-480e-8101-e290aa343ad1.jpg)
![4-14](https://user-images.githubusercontent.com/107659667/188773569-22092d0c-9794-48b0-bc40-29403e7c32e2.jpg)
![4-15](https://user-images.githubusercontent.com/107659667/188773573-176ea479-04db-4018-8ca2-70fd48440eab.jpg)



As a reminder, the deliverables for this Challenge are as follows:

Deliverable 1: Write an ETL function to read three data files
Deliverable 2: Extract and Transform the Wikipedia Data
Deliverable 3: Extract and Transform the Kaggle Data
Deliverable 4: Create the Movie Database
IMPORTANT
Don’t clear the output of your Jupyter Notebook files. Doing so will result in a lower score.

Upload the following to your Movies-ETL GitHub repository:

The ETL_function_test.ipynb file
The ETL_clean_wiki_movies.ipynb file
The ETL_clean_kaggle_data.ipynb file
The ETL_create_database.ipynb file
The Resources folder with the wikipedia_movies.json, movies_metadata.csv, movies_query.png, and ratings_query.png files.
A README.md that describes the purpose of the repository. Although there is no graded written analysis for this Challenge, it is encouraged and good practice to add a brief description of your project.
