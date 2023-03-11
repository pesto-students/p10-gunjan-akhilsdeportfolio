# Browsers and Internals of Browsers
## what is the main responsibility of browsers 
The main function of a browser is to present the web resource you choose, by requesting it from the server and displaying it in the browser window. The resource is usually an HTML document, but may also be a PDF, image, or some other type of content. The location of the resource is specified by the user using a URI (Uniform Resource Identifier).


# High Level componenets in the Browser
[![High Level Components ](https://web-dev.imgix.net/image/T4FyVKpzu4WKF1kBNvXepbi08t52/PgPX6ZMyKSwF6kB8zIhB.png?auto=format&w=650 "Shiprock, New Mexico by Beau Rogers")]
## Browser User Interface
Browser user interfaces have a lot in common with each other. Among the common user interface elements are:

1. Address bar for inserting a URI
2. Back and forward buttons
3. Bookmarking options
4. Refresh and stop buttons for refreshing or stopping the loading of current documents
5. Home button that takes you to your home page

## Browser Engine 
Browser Engine is responsible for bridginng the ui actions to the rendering engine and it also has access to the data persistence layer so that it can retrive data from data sources like localstorage and Index DB

## Rendering Engine 
rendering engine is responsible for rendering the html content on to the screen , there are certain steps in the process of rending the content on to the screen
1. Parsing the HTML and CSS
2. Constructing the DOM Tree
3. Painting the screen

as you can see the rending process happens in the 3 steps in the first step , Html parser would get the html from the source code and parse it and the same would happen with css , once the html is parsed a DOM tree is contructed from the html elements and then the browser will start painting the screen pixel by pixel.

Rendering engine has access to the newtworking component , javascript interpreter.

## Networking component
networking componenet is responsible for all the network call that a web page makes , it makes network calls and parses the response and returns to the rendering engine so that rendering engine can work on the the data sent by the server.
## Javascript Interpreter
JS interpreter is responsible for interpreting the js code present in the webpage it parses the js code and starts executing the code.
## Data persistence Layer
we need some sort of mechnaisim to store the data and this is provided bt the  data persistance layer which has localstorage,Index DB API's responsible for storing the key-value pairs of data.

## Order of Execution of scripts 

scripts placed in the head tag execute first
scripts tags with out defer tag and placed in the head  start executing before html content is loaded
scripts with defer tags exectue once the page loads
scripts placed in the body tag start executing once the html content is loaded.
