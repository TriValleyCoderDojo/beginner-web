Session 4 - Introduction to JavaScript
=================

## What is JavaScript?
JavaScript is a scripting language that can be used in your browser. It is used to make your web pages more interactive and interesting.  It will allow you to write code that will create a pop-up alert box, catch mouse events, catch keyboard events, allow you to hide/unhide parts of the page, plus a whole lot more.  Contrary to its name, it has nothing to do with Java.  

In this session we will learn only some of the basic things you can do with JavaScript.  There are a number good resources available to learn more.  All you will need to do is a search from your browser.  

### JavaScript Variables
Variables in JavaScript let you save data or functions with associated names. This will allow you to reference that data or function later.  

* Variable names must begin with a letter
* Variable names can also begin with $ and _ (but we will not use it)
* Variable names are case sensitive (y and Y are different variables)
* [Reserved Words](http://msdn.microsoft.com/en-us/library/0779sbks.aspx) (like JavaScript keywords) cannot be used as variable names

Variables in JavaScript do not have a specific type associated with them (eg: integer, string, etc...)  The type of the variable will be determined by how it is used in the code.  The variables will be declared with the keyword ``var``

* A string ``var name = "Alex";``
* An integer ``var counter = 3;``
* A decimal number ``var percent = 58.326;``
* In scientific notation ``var y = 123e5;``
* A boolean ``var done = false;``
* An array ``var cars = ["Saab", "Volvo", "BMW"];``
* An object ``var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};``
* A function ``var myFunction = function() { /* some code here */ }``

Where a variable is defined makes a difference.  If a variable is defined inside of a function, then that variable will only be known inside of that function.  This is called the scope of the variable.  In JavaScript there are two scopes, local and global.  Local variables are defined within some context, such as a function.  Global variables are defined at the highest level, and are available to everything.  

### JavaScript Functions
A function is a set of instructions to do the some kind of work for you.  They might do some kind of calculation, or return some value.  They allow you to do the same set of operations again and again, without needing to repeat the code in different places.  You create your function once, and you can use it as many times as you need to.  You can use parameters to change the inputs which makes them very flexible and powerful.  

There is a specific format that you need to follow for a JavaScript function:

```
function functionName(parameters) {
  code to be executed
}
```

The code inside the curly brackets, or the body, of the function can be any valid JavaScript statement.  Each statement will need to be terminated with a semicolon (;).  For a list of the available statements refer [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements).  Below is an example of a JavaScript function that accepts a number as a parameter, squares the number and then returns the result.


```
function square(y) {
    return y * y;
}
```

## Using JavaScript in CodePen
If you recall CodePen has three editor windows: HTML, CSS & JS.  Previously, you were asked to ignore the other editors, until it was time to consider them, and now it is time to consider the JS or JavaScript editor.  Similar to the HTML and CSS editor, you can just enter your JavaScript into the editor.  

 ![JS Editor](https://raw.githubusercontent.com/TriValleyCoderDojo/beginner-web/master/screenshots/JS_01.PNG)

However, there is something that you will need to consider when entering your JavaScript in CodePen.  It will be executed immediately.  This can be a bit frustrating sometimes, because your code can be executed while you are trying to type it in, which might be distracting.  We will see an example of this with an alert box next.  


## Using Alert
Let's try writing our very first line of JavaScript. In the JavaScript window of jsfiddle, type in ``alert("CoderDojo is awesome!")``. Click "run" or "update" and see what happens. You should see an alert message that says "CoderDojo is awesome!"

## Catching a Mouse Event


## Catching a Keyboard Event


## Using the Inspector and console.log();
Unlike HTML and CSS where you can see what changes you make in your Codepen.IO websites, Javascript requires you to use the web inspector's console to see what is going on. The console is a way to see exactly what your JavaScript code is doing, since sometimes you can't tell if your code works or not just by looking at it like in HTML or CSS. You can access the console in various browsers:

* Chrome: Go to View -> Developer -> JavaScript Console
* Firefox: Go to Tools -> Web Developer -> Web Console
* Safari: Go to Preferences -> Advanced -> select "Show Develop Menu in Menu Bar." After that Develop option should show up on the menu. Then go to Develop -> Show Web Inspector
* IE: Tools -> Developer Tools (click on Scripts tab or Console tab, depending on the IE version)





## Talking to JavaScript
Let's give your website some personality.
First, we should teach your website your name! In your JavaScript section type in and see what this does:

* ``prompt("What is your name, visitor?")``

You should see an alert box pop up that has a place to type in your name. Go ahead and tell your webpage what your name is! In your Inspector's Console you should see your name in quotation marks.




## Adding Data to Your Page
All of our JavaScript data is just stored in our JavaScript code right now. But what if we wanted to display our data on the website? Let's create a welcome message for our users.

* First lets add an HTML element for our welcome message. ``<div id="welcome-container"></div>``
* We also need a button to run our function: ``<button onclick="setWelcomeMessage()>Set Welcome Message!</button>"``
* Add some CSS

```
#welcome-container {
  font-size: 25px;
  padding: 20px;
  background: #33ffcc;
  margin: 20px;
  border: 10px dotted white;  
  display: none;
}
```
* Paste this code into your JavaScript section:

```
// Set a welcome message with my data
var setWelcomeMessage = function() {
  var name = getMyName();
  var welcomeMessage = "Welcome " + name + "!";
  var welcomeContainer = document.getElementById('welcome-container');
  welcomeContainer.innerHTML = welcomeMessage;
  welcomeContainer.style.display= 'block';
}
```
Notice how we are using the function we already wrote in our JavaScript to get our ``name`` value.

Keep in mind that browsers are forgetful! They cannot remember everything you do unless we tell our code to make the browser remember. When we refresh our page, the name you stored will be gone.

