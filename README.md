### CodeSquad Class Exercise - Web Notes App

#### Mockup of Parts 1-6
![Mockup Image of Parts 1-6](public/images/mockups/mockup-parts%201%20to%206.png)

#### Part 1: Project Setup
1. Create a project folder called web-notes
2. Make sure the entry point file app.js is in the root of the project folder.
3. In the terminal, make sure you are in your project folder.
4. In the terminal, type: npm init
5. Answer the prompts, making sure your app.js file is the entry point.
6. In the terminal, type: npm install express ejs
7. In the terminal, type: npm install nodemon --save-dev
8. Create a public folder for your static assets (css, js, image) in your project folder.
9. Create a css folder in the public folder.
10. Create a views folder in the project folder. This is where we store our ejs templates.

#### Part 2: Express Setup
1. Require express
2. Create an Express application
3. Create a port variable and assign it to 3000
4. Require the path module
5. Tell express to use your public folder. Later, notice in our ejs file all we need is "css/styles.css"
6. Set the view engine to 'ejs' so that we don't have to specify the .ejs extension in our routes

#### Part 3: Listen
1. Listen for a connection on the port variable and console.log() a confirmation message
2. Start your app through the terminal and make sure your message appears: node app.js
* If you are using nodemon, it would be: nodemon app.js

#### Part 4: EJS file
1. Before we create any routes, put the notes.ejs file in the views folder.
2. Take 3-5 minutes to look over the code and digest it.

#### Part 5: Root route
1. Create a get route for the root '/' to render to the notes page, passing through the myNotes array.
2. Remember that express automatically looks in the views folder.
3. Test your route by going to localhost:port
4. You should see the starter data myNotes displayed on the page! Look at the ejs file again and piece together what is happening.

#### Part 6: CSS file
1. Put the given CSS file in the css folder if you haven't already.
2. Add the stylesheet link to the ejs template

#### Mockup of Parts 7-9
![Mockup image of Parts 7-9](public/images/mockups/mockup-%20parts%207%20-%209.png)

#### Part 7: HTML form
1. In notes.ejs: Right before the closing `</body>` add a `<form>`
2. Set the method attribute to "POST", because that's the HTTP request we want.
3. The action attribute tells the form which path to post to, in this case we want to post to the notes page so we can display all of the written notes: `<form method="post" action="/notes">`
4. Inside of the form create a div with the class "form-group". This is our friend Bootstrap.
5. Inside of the form-group, create a text input with the name of "note", and a label for it.
6. Outside of the form-group, create a submit input with the value of "Save". Set the class to "btn btn-primary".
7. Relaunch your app, and take a look at the network tab in the browser. If you try to submit the form, you will get an error because we haven't made anything in our web notes app that responds to an http post request at the path /notes yet. 

#### Part 8: Body Parser
1. Require the body-parser module and tell the app to use it
2. This transforms the “body,” or contents, of the request (which is a string) into an object which we can then reference with req.body in our code.

#### Part 9: Post Route
1. Create a post route for the notes page: 
   * In the callback function: Grab the data using req.body and push it to our myNotes array, then redirect to '/'

#### Mockup of Bonus
![Mockup Image of Bonus](public/images/mockups/mockup-%20bonus.png)

#### BONUS
1. In the ejs file, add some logic that will add the class .highlight to the div if the note contains 'important' or '*'
2. Add a limit to the number of characters that the input will take.
3. Add a restriction to the characters that the input will take.
