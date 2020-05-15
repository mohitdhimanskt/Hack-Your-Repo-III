4. PROJECT: Hack Your Repo III

The final week's assignment consists of two parts.

In the first part you will update the homework from week 2 (in the homework folder). In the second part you will refactor your application to use ES6 classes. For this, you need to modify the files in the homework-classes folder.
PART 1: async/await & axios

In the first part you'll need to modify some parts of your code with what you've learned about. Implement the following:
OOP and ES6 classes

In this second part requires you'll work with a codebase that is build in the Object Oriented Programming paradigm (OOP). OOP is a vast topic and in this homework we can only scratch the surface. The approach we have taken here is for you, as aspiring junior developer, to complete an application for which the groundwork has been done by an experienced developer. You may find it difficult to understand the full details of the application, however this is not unlike a real world situation where you will be expected to make relative small modifications to a complex application, without breaking anything.
Getting an overview

The relevant files for this part of the homework can be found in the homework-classes folder. In the following table you'll find an outline (with explanations about their role in our application):
File 	Description
index.html 	The application's HTML file.
style.css 	CSS styling.
hyf.png 	The HYF logo.
App.js 	The App class is the main container class for the app.
Observable.js 	The Observable class is a base class implementing functionality of the Observer pattern.
Model.js 	The Model class is concerned with all data handling (e.g. fetching). Extends the Observable class.
HeaderView.js 	The HeaderView class renders the header with the select element.
RepoView.js 	The RepoView class renders the details for the selected repository.
ContributorsView.js 	The ContributorsView class renders the contributors for the selected repository.
ErrorView.js 	The ErrorView class renders an error, if present.
Util.js 	The Utility class provides (static) utility functions.

Like mentioned in the readings, the point of OOP is to split your application up into "entities". These entities then work together like a team in order to make an application work.

The image below illustrates the interrelationship between the various classes in the application using a UML Class Diagram.

JavaScript3_classes
A first examination

You can conclude the following from this diagram:

    The Model class extends (inherits from) the Observable class. Views (i.e., 'observers') can subscribe to the Model and get notified on data updates.

    There are four View classes that implement the IObservable interface, i.e. they implement the required update() method:
        HeaderView
        RepoView
        ContributorsView
        ErrorView.

    The SelectView class calls the fetchData() method from the Model class to request a data fetch.

    There are four View classes that implement the IObservable interface, i.e. they implement the required update() method:
        HeaderView
        RepoView
        ContributorsView
        ErrorView

Week 3 Assignment

PART 1: Modify your existing code base

In the homework folder, modify the following:

    Refactor all .then() and .catch() methods with async/await and try...catch.
    Make sure that your error handling code still works. See the instructions from week 2's homework on how to force an error response from GitHub.
    Modify the fetchJSON function to replace fetch with axios.
    Add a <script> tag to index.html to load the axios library from a CDN (Content Delivery Network) site. Use Google to find the right URL.

PART 2: Moving to the OOP version of the homework

In the homework-classes folder, modify the following:

    Modify the RepoView.js and ContributorsView.js files, by adding and adapting code from your non-OOP version of the homework to these files.
    You should also copy the styling from your non-OOP version.
    Make sure everything still works!
