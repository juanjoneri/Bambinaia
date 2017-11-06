# Preliminary Database Design

## Database Description
A few months ago, we were watching an episode of the famous TV show "Friends", where Rachel and Ross where trying to find a nanny who could take care of their baby while they where at work. The scene showed them scheduling interviews with different nannies and having a hard time finding the perfect one for their child. In that moment we realized how that task could have been much easier for the characters had there been an app that could find the perfect nannny for them. This is how the idea of Bambinaia started. 

Our aim is to develop a website for matching parents with nannies. We know and value all the hard work that parents put into raising their children, but we understand as well that, as every human being, we all need some time off to focus on something else such as get work done, meeting an old friend or getting that deserved massage. Bambinia allows parents to take some time off  while having the ease of mind that their children are taken good care of. This app is perfect both for parents that need a nanny, as well as nannies that want to get some hands on experience with children, or that would like to spend their free time earning extra cash. We know all families are different, and that all parents have different preferences on the qualifications of their nannies, that's why Bambinaia helps them find the perfect nanny to match their needs. 

The website will be developed using Google's Polymer 2.0, a JavaScript library that helps you create custom reusable HTML elements *(web components)*, and use them to build performant, maintainable apps. Authentication, data storage and hosting will be done through Google's Firebase. The data is managed as JSON files and allows real time changes to occur on the connected client side. 

## Data Description

The data to be stored will be divided in three different entities: Parent information, Nanny Information and Log Entry. As described in the Entity Relationship Diagram available below, the Mother and Nanny tables will hold information about the users, such as contact information and location. The following screen shows  and example of a Parent called Juan Neri signing up for the service. On the right hand side we can see how the back end stores the data as a javascript object to be sent to the Firebase servers.

![json_sample](screens/json_sample.png)



## Examples of Database
When a parent requests a nanny, a date and time of when the service will be needed should be selected.  Bambinaia will then return a list of different nannies that are a good fit for the specified needs; time, location and parent preferences, are some of the things the algorithm takes into account.

For example, if the parent lives in Venice Beach and prefers a nanny that can read to his children, then the following could be a recommended nanny:

![usercard](./screens/usercard.png)

The paper card will show the nanny's availability, as well as information about her, such as name, rating, location, general description, occupation, and a nice picture. 

These are other examples that might have been retrieved from the database from this query and presented as a card to this parent:

| First Name | Last Name | General Description           | Availability | Occupation                             | Rating | Location       |
| ---------- | --------- | ----------------------------- | ------------ | -------------------------------------- | ------ | -------------- |
| Florencia  | Gomez     | Florencia speciality is in... | M W 4-10 pm  | Student at Loyola Marymount University | 4.5    | Venice Beach   |
| Victoria   | Neri      | Vic loves kids of all ages... | M W 12-6pm   | Student at Loyola Marymount University | 5.0    | Playa Vista    |
| Camila     | Garcia    | Cami has experience in...     | M W 2-11pm   | Student at UCLA                        | 4.2    | Marina Del Rey |
| Valeria    | Rodriguez | Vale enjoys children...       | M W 3-10pm   | Elementary teacher                     | 4.8    | Playa Vista    |
| Alejandra  | Rosales   | Ale has been a nanny for...   | M W 4-9 pm   | Nurse                                  | 4.9    | Santa Monica   |

If the parent wishes to select this nanny then he/she can send a request with a description of the requirements for the service (date and time, number of kids need to be taken care of, etc). Now the nanny will recieve a similar card with the parent's request, and she can decide whether she accepts or not. Once the request is accepted, the platform will allow the parent and nanny to exchange their contact information. 

## Schema

The following tables represent the entities in Bambinaia's database and with its respective attributes. We also added all the parts required for an accepted and completed "request" transaction.

### Nanny

| Nanny ID   | First Name | Last Name | General Description           | Availability | Occupation                             | Rating | Age  | Street Address     | ZIP   | Phone      | Email                |
| ---------- | ---------- | --------- | ----------------------------- | ------------ | -------------------------------------- | ------ | ---- | ------------------ | ----- | ---------- | -------------------- |
| 9595866898 | Florencia  | Gomez     | Florencia speciality is in... | M W 4-10 pm  | Student at Loyola Marymount University | 4.5    | 19   | 1336 Imaginary St. | 94400 | 3531315131 | fgomez3@lion.lmu.edu |

### Parent

| Parent ID   | First Name | Last Name | General Description | Rating | Age  | Street Address         | ZIP   | Phone       | Email               |
| ----------- | ---------- | --------- | ------------------- | ------ | ---- | ---------------------- | ----- | ----------- | ------------------- |
| 96964565773 | Maria      | Carrera   | I have two kids...  | 4.5    | 32   | 7270 W. Manchester AV. | 90045 | 12453151641 | m.carrera@gmail.com |

### Log Book

| Date       | Start    | End       | Number of Children | Mother review | Nanny review | Parent ID   | Nanny ID   | Location              |
| ---------- | -------- | --------- | ------------------ | ------------- | ------------ | ----------- | ---------- | --------------------- |
| 01/01/2016 | 8: 00 pm | 11: 00 pm | 2                  | 5.0           | 4.0          | 96964565773 | 9595866898 | 7270 W Manchester Ave |



## ERD
The following picture represnets our Entity-Relationship Diagram for Bambinaia's database:



![Bambinaia_ERD](../screens/Bambinaia_ERD.png)
