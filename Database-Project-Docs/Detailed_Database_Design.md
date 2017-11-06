# Detailed Database Design

### Project Description

###### Engine Used

###### Potential Users

###### Other Stuff

### Data Dictionary

###### Parents

| Column              | Description                              |
| :------------------ | ---------------------------------------- |
| Parent_ID           | Unique ID designated automatically by DBMS Firebase |
| First_Name          | First name given to the parent at birth (i.e. Ross) |
| Last_Name           | Last name (aka family name) of the parent (i.e Geller) |
| Gender              | Male, female or other                    |
| Phone_Number        | Mobile phone number for nannie to be able to contact. |
| Email               | Preferred email for all communication related to the app |
| Address_Street      | Street of the house where the parent expects nannie to work |
| Address_City        | City where the parent needs the nannie (i.e. where the children live) |
| Address_Zip         | zip code corresponding to the provided address (nannie relevance is ordered based on proximity to the parent) |
| General_Description | Personal description of the parent. Used by the nannies to asses if she would be a good fit for that family. Parents might include: number of children, thinks they like to do around the house, etc. |
| Rating              | Contains the average of the ratings given by nannies to this parent in the past |

###### Nannies

| Column              | Description                              |
| :------------------ | ---------------------------------------- |
| Nanny_ID            | Unique ID designated automatically by DBMS Firebase |
| First_Name          | First name of the nanny (i.e. Phoebe)    |
| Last_Name           | Last name of the nanny (i.e Buffay)      |
| Gender              | Male, female or other                    |
| Age                 | Time elapsed since birth rounded to nearest year |
| Phone_Number        | Mobile phone number for parent to be able to contact |
| Email               | Preferred email for all communication related to the app |
| Address_Street      | Street of the house where he/she is most likelly to commute |
| Address_City        | City corresponding to the provided address |
| Address_Zip         | zip code corresponding to the provided address |
| General_Description | Personal description of the nanny. Used by the parents to asses if he/she would be a good fit for that family. Nannies might include: Talents, prefered children age, etc. |
| Rating              | Contains the average of the ratings given by parents to this nanny in the past |
| Occupation          | Nannies full time occupation (i.e. Student at LMU) |
| Availability        | Days and time of the week where nanny would be available to work |

### Entity Relationship Diagram