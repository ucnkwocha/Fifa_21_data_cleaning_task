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
<img width="252" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/f7105aa2-5096-49b9-84e8-d874f95920f7">


# Contract and Position Column
The contract column indicates the players duration. It contains inconsistent values which comprises of players on contract, free and on Loan.

<img width="375" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/6534d980-c130-46d8-a726-6eb3d8ce2af5">

I have used the replace value option to change the " ~ " character to "-"

![image](https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/0d5be09c-f9d5-4a57-aece-6764b7977571)

I also used conditional formatting to seperate each category of contract.
Using conditional column, Values are grouped into contract, Loan and free values. Column name is renamed to contract type. A condition is entered such that, IF contract column contains (-) return CONTRACT, Else if contract contains free return free Else return Loan. Enter ok

<img width="674" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/cc16d5f1-b168-464f-9511-7ae74a1b90d4">

<img width="252" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/b4e45cf5-ceb5-4bb2-86d1-9f9c8344f4f3">

To derive the contract duration,
I right clicked on the contract column and used split column option by delimiter to split the start year and end year.

<img width="241" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/bc92c154-e5b6-49de-825b-a9987aa0f78c">

After splitting, I observed that the split columns contained 5% error. I used the replace error option to replace error with null.
Furthermore, the custom column was used to derive the player's contract duration on the split columns by subtraction columns 1 from columns 2

<img width="506" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/4f0a4b01-b918-495c-ba4c-a70f2cd99378">

<img width="365" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/4f37d1e4-3421-48ca-b5b0-a9f283281cb8">



# Position and Best Position
The ‘Position’ column consists of one or more positions the player has ever played while the "Best postion"column indicates the best position for the player. 
For data visualization purpose it is best to retain the Best Position column in place of the Position column.
For both columns, the values are consistent with no empty cell or error cell. 

<img width="242" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/a655ca9a-94d9-4c94-aad7-c8be89b12528">

The Replace value option was used to replace the abbreviated values

<img width="504" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/bc958a9c-917c-4b82-9d85-63d7599efde6">

<img width="133" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/a0bbcf5a-98b6-47ab-a755-5ea8a4fdbad8">

# Height and Weight
The both columns contains inconsistent data. The height value was entered in two different formats (foot & inches), while the weight column had values entered in two different formats "kg" and "lbs".

<img width="244" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/2f26ff9b-1fa1-4af5-a297-4403a9be2bf6">

For the Height column the consistency was achieved using a formula to convert the "foot" and "inches" to cm.
New_height = 
    Table.AddColumn(
        Table.SelectRows(#"PreviousStep", each not Text.Contains([Height], "cm")),
        "New_height", 
        each Number.From(
            Text.Start(
                [Height], 
                Text.PositionOf([Height], "'") - 1
            )
        ) * 30.48 + Number.From(
            Text.Range(
                [Height], 
                Text.PositionOf([Height], "'") + 1, 
                Text.PositionOf([Height], """") - Text.PositionOf([Height], "'") - 1
            )
        ) * 2.54
    )
New_weight = Table.AddColumn(#"PreviousStep", "New_weight", each
    if Text.Contains([weight], "kg") then
        Number.From(Text.Start([weight], Text.PositionOf([weight], "kg") - 1)) * 2 - 20
    else
        Number.From(Text.Start([weight], Text.PositionOf([weight], "lbs") - 1))

<img width="154" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/6b408cbf-dfc9-47ca-affc-0872f80b4eff">

# Value, wage and release clause

<img width="362" alt="image" src="https://github.com/ucnkwocha/Fifa_21_data_cleaning_task/assets/155919216/14b13f10-a23e-48b6-9f25-0078e1e8cee0">

The value and wage columns are in string /text data type and needs to be converted to Number. The € was replaced with space(nothing), the custom column was used to multiply the 













