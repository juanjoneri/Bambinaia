# Detailed Database Design

### Project Description

###### Engine Used

###### Potential Users

###### Other Stuff

### Data Dictionary

###### Parents

| Column              | Description                              |
| :------------------ | ---------------------------------------- |
| Nanny_ID            | Unique ID designated automatically by DBMS Firebase |
| First_Name          | First name of the parent (i.e. Juan)     |
| Last_Name           | Last name of the parent (i.e Neri)       |
| Gender              | Male, female or other                    |
| Phone_Number        | Mobile phone number for nannie to be able to contact. |
| Email               | Preferred email for all communication related to the app |
| Address_Street      | Street of the house where the parent expects nannie to work |
| Address_City        | City where the parent needs the nannie (i.e. where the children live) |
| Address_Zip         | zip code corresponding to the provided address (nannie relevance is ordered based on proximity to the parent) |
| General_Description | Personal description of the parent. Used by the nannies to asses if she would be a good fit for that family. Parents might include: number of children, thinks they like to do around the house, etc. |
| Rating              | Contains the average of the ratings given by nannies to this parent in the past |

###### Nannies

| Column | Description |
| ------ | ----------- |
|        |             |

### Entity Relationship Diagram