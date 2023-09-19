## Netflix data Wrangling - Python

A detailed wrangling of Netflix data from 2008 - 2021 using pandas and seaborn in python.
N.B : Refer the jupyter notebook to understand better. This README file is just a description of the project.
File Wrangling_Netflix_titles.ipynb contains initial data cleaning and wrangling using which I export the data to a csv file.

#### Motivation

Netflix is a popular streaming service with a vast selection of movies, TV episodes, and original material. The original dataset, which can be accessed here, has been cleaned up and made available in this dataset. The data consists of the content that Netflix added between 2008 and 2021. The aim of this project is to clean the Netflix data and find some interesting trends and how it has changed over time.

## Table of Contents
1. [Importing Libraries ](#Importing_Libraries)
2. [Collecting Data](#Collecting_Data)
3. [Cleaning Data](#Cleaning_Data)
4. [Export to CSV](#Export_to_CSV)

## Importing Libraries
Before you import libraries, install them with the folloeing command:
pip install library_name 

##### Important libraries :
1. [pandas](#pandas)
2. [matplotlib](#matplotlib)
3. [seaborn](#seaborn)

## Collecting Data
This dataset is a cleaned version of the original version which can be found [here](https://www.kaggle.com/datasets/shivamb/netflix-shows).
The Netflix_titles.csv file contains the following columns (as per the Cover Sheet provided by Netflix):
* show_id
* type
* tittle
* director
* cast
* country
* date_added
* release_year
* rating
* duration
* listed_in
* description
Understanding the meaning of the data, particularly the meaning of the columns, is a crucial first step since without understanding the data, our analysis won't be accurate.

Now that we have moved forward, we can begin importing the data into our project.
## Reading Data
I will be using Jupyter notebooks for this project. If you want to quickly analyze your data and share the result with others, Jupyter notebooks are a wonderful option.
* ##### Import libraries
* Use pd.read_csv()  to read the file as a dataframe to help us clean the data and manipulate it easily. 
* Copy the dataframe using df.copy() so that if you make any mistake during analysis, you can always roll back to the original data without losing any information.
* Print the columns of the dataframe using df.columns and use the df.info() to see the data type of each column.

## Cleaning Data
Refer to the Wrangling_Netflix_titles.ipynb notebook to understand the data cleaning process better. 
Workflow:
* Identify Missing Values
* Deal with missing data
  * Drop unwanted rows (when few rows are empty)
  * Populate coloumns if most entries are empty such as director, cast and country
* Check and Correct data format

## Exporting the Data
Finally, after cleaning and altering the data as needed, the data may be exported to a csv file so that you don't have to run the cells over and over again. You may accomplish this with df.to_csv(filename).

