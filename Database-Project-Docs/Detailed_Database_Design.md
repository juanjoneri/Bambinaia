# Detailed Database Design

### Project Description

###### Engine Used

data storage and hosting will be done through Google's Firebase we API. The data is managed as JSON files and synced in real time on the connected client side.

###### Potential Users

Our aim is to develop a website for matching parents with nannies. We know and value all the hard work that parents put into raising their children, but we understand as well that, as every human being, we all need some time off to focus on something else such as get work done, meeting an old friend or getting that deserved massage. Bambinaia allows parents to take some time off while having the ease of mind that their children are taken good care of. This app is perfect both for parents that need a nanny, as well as nannies that want to get some hands on experience with children, or that would like to spend their free time earning extra cash. We know all families are different, and that all parents have different preferences on the qualifications of their nannies, that's why Bambinaia helps them find the perfect nanny to match their needs.

###### Other Stuff

The website will be developed using Google's Polymer 2.0, a JavaScript library that helps you create custom reusable HTML elements *(web components)*, and use them to build performant, maintainable apps. Authentication, data storage and hosting will be done through Google's Firebase. The data is managed as JSON files and allows real time changes to occur on the connected client side.

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

###### Log_Book

| Column          | Data Type    | Description                              |
| --------------- | ------------ | ---------------------------------------- |
| Date            | TIMESTAMP    | Date when work started.                  |
| Start           | TIME         | Start time, when nanny started working   |
| End             | TIME         | End time, when nanny left the house      |
| Number_Children | SMALLINT     | Number of children that the nanny had to take care of |
| Parent_Review   | SMALLINT     | Number 1-5 describing the general satisfaction level of the parent with the nannie's job |
| Nanny_Review    | SMALLINT     | Number 1-5 describing the general satisfaction level of the nanny with the children, house, and overall job. |
| Parent_ID       | INT IDENTITY | Identifying attribute of the parent who requested the nanny. |
| Nanny_ID        | INT IDENTITY | Identifying attribute for the nanny that was assigned the job. |



### Entity Relationship Diagram

![Bambinaia_ERD.png](../screens/Bambinaia_ERD.png)