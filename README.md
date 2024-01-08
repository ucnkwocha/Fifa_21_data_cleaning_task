# Fifa_21_data_cleaning_task
![image](https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/25fcb3f1-9f19-4c32-ab7b-f1580c11d339)

# Introduction

 Welcome to the Data Cleaning repository! This project is dedicated to streamlining and enhancing the process of cleaning and preparing datasets for analysis. As a data analyst , the quality of your data significantly influences the accuracy and reliability of your insights.

![image](https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/cfa76119-e9e5-4655-9156-0a81bc331c1f)

This data cleaning task demostrates the process of fixing the FIFA_21 messy data set and this was done using Power BI.

# Objective and Problem Statement
The objective of the data cleaning is to eliminate the listed below

+ Correcting Inaccuracies and Errors
* Standardizing and Transforming Data
- Handling Special Characters and Encoding Issues
* Handling Inconsistent Formats

# Description of dataset
This data set was sourced from [kaggle](https://www.kaggle.com/datasets/yagunnersya/fifa-21-messy-raw-dataset-for-cleaning-exploring)

The dataset contains 18,979 rows and 77 columns which includes details of the player's names, clubs,photo_url, height, weight, their overall perfomance and so on. 

Walk with me as i take you through the data cleaning process 

# Data Cleaning Process
The dataset was successfully imported from the excel workbook ribbon on Power BI which allows files to be access directly from the desktop.

<img width="617" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/8e8cc35c-545b-4c1b-8852-0166e73d1d6c">

Below is the FIFA 21 dataset in the power query editor showing the quality of each columns, however this captured the first four columns. The first four columns displays  100% valid, 0% error and 0% empty cell.

<img width="758" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/733e4890-f300-4a2f-95a7-36821f39784a">

# ID, name, longname, photourl,  playerurl
The ID column contains the unique number assigned to every player.The ‘Name’ column contains the player's short name, while the ‘Long Name’ column contains' the player's full name. The photourl and Player_url Column consists of photograph and players web page. The 'Name' column will be eliminated while the 'Long name' will be retained as 'Full name'

<img width="757" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/f081c018-eec4-473e-9cdb-b3b076462695">

<img width="678" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/449b3675-9187-475a-afc2-cc12aabe6c01">

# The Nationality, Age, OVA, POT and Club 

The Nationality columns shows the player's country of origin. 
Age indicates the Players age.
OVA(Over Rating)is a numerical representation of a player's overall skill and performance level. POT(Potential) refers to the estimated future skill level or rating a player can achieve overtime. 
The Nationality,Age,OVA,and POT columns are consitent with no error or empty cell. 

<img width="737" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/327bf3d0-0357-4120-b1b5-5358debec8bf">

The Abbreviated OVA column with a special character and the POT column has been renamed as OverRating and Potential.
The Club column consists of inconsistent data entry. Some of the club’s names had numerical prefixes like 1.FC Koln. The prefix was removed from the data using the replace values option.

<img width="559" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/bf14e0da-5ce3-479f-8783-1f3a7f3f107d">
<img width="257" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/984f0054-4ebb-431e-8cd5-1a5021abaac0">













