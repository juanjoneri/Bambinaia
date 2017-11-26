# Bambinaia
## Website for pairing nannies and mothers in real time

A few months ago, we were watching an episode of the famous TV show "Friends", where Rachel and Ross where trying to find a nanny who could take care of their baby while they where at work. The scene showed them scheduling interviews with different nannies and having a hard time finding the perfect one for their child. In that moment we realized how that task could have been much easier for the characters had there been an app that could find the perfect nanny for them. This is how the idea of Bambinaia started.

Our aim is to develop a website for matching parents with nannies. We know and value all the hard work that parents put into raising their children, but we understand as well that, as every human being, we all need some time off to focus on something else such as get work done, meeting an old friend or getting that deserved massage. Bambinaia allows parents to take some time off  while having the ease of mind that their children are taken good care of. This app is perfect both for parents that need a nanny, as well as nannies that want to get some hands on experience with children, or that would like to spend their free time earning extra cash. We know all families are different, and that all parents have different preferences on the qualifications of their nannies, that's why Bambinaia helps them find the perfect nanny to match their needs.

The website will be developed using Google's Polymer 2.0, a JavaScript library that helps you create custom reusable HTML elements *(web components)*, and use them to build performant, maintainable apps. Authentication, data storage and hosting will be done through Google's Firebase. The data is managed as JSON files and allows real time changes to occur on the connected client side.

### Download the Project

#### Run the app locally

```bash
cd Bambinaia/
bower install
polymer serve --open
```

#### Add new components

https://www.polymer-project.org/1.0/start/toolbox/add-elements

```bash
bower install --save PolymerElements/paper-radio-button
```

#### Deploy using firebase

https://www.polymer-project.org/1.0/start/toolbox/deploy

```bash
polymer build
firebase deploy
```

### Available live at

[firebase.com](https://polymer-project3.firebaseapp.com/add-nanny)

#### Add User  view

#### ![adduser](https://github.com/juanjoneri/LMU-CMSI486-Fall17/blob/master/screens/adduser.png)

### Retreive User view

![retreiveuser](https://github.com/juanjoneri/LMU-CMSI486-Fall17/blob/master/screens/usercard.png)
