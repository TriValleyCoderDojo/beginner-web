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

```javascript
function functionName(parameters) {
  code to be executed
}
```

The code inside the curly brackets, or the body, of the function can be any valid JavaScript statement.  Each statement will need to be terminated with a semicolon (;).  For a list of the available statements refer [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements).  Below is an example of a JavaScript function that accepts a number as a parameter, squares the number and then returns the result.


```javascript
function square(y) {
    return y * y;
}
```

### Other Useful JavaScript Info

JavaScript provides all the usual operators that you would expect, such as: arthimetic, assignment, comparison, logical etc...  A complete list can be found at [JavaScript Operator Reference](http://www.w3schools.com/jsref/jsref_operators.asp)

It is often a good idea to comment out some code while debugging and testing.  JavaScript provides two kinds of comments: 1) ``//`` for single line comments, and 2) ``/* any number of lines */`` for multiple line comments. 


## Using JavaScript in CodePen
If you recall CodePen has three editor windows: HTML, CSS & JS.  Previously, you were asked to ignore the other editors, until it was time to consider them, and now it is time to consider the JS or JavaScript editor.  Similar to the HTML and CSS editor, you can just enter your JavaScript into the editor.  

 ![JS Editor](https://raw.githubusercontent.com/TriValleyCoderDojo/beginner-web/master/screenshots/JS_01.PNG)

However, there is something that you will need to consider when entering your JavaScript in CodePen.  It will be executed immediately.  This can be a bit frustrating sometimes, because your code can be executed while you are trying to type it in, which might be distracting.  We will see an example of this with an alert box next.  


## Using Alert Box
So let's do our first line of JavaScript.  In the JS editor window, enter:

``alert("CoderDojo is awesome!")`` 

So I am sure that you noticed that as you were trying to type in the JavaScript code the pop-up window came up more than once, pretty annoying huh!  Well, this is happening because CodePen is executing your JavaScript immediately.  One suggestion might be to write the code in a seperate editor and then copy and paste the code into the JS editor window.  Go ahead and give that a try with your favorite editor, such as Notepad or Notepad++.  

Okay, so that was pretty boring. After going through the previous sessions, that was very much underwhelming.  I think we need a little bit more excitement.  We are CoderDojo Ninjas after all!  Let's do something more advanced.  We will start with with some baseline code, as shown below:

HTML
```html
<div class="box">
  <div class="box-inner">  
  <h2>My First JavaScript Program</h2>
  <p>I love doing cool stuff</p>
  <a class="button" href="http://codepen.io//" title="Fake Button">Fake Button</a>
  </div>
</div>
```

CSS
```css
body{
	font-family: 'Arial', sans-serif;
	padding: 2rem 4rem;
	background-color: #ffffff;
  color:#555555;
}

.box {
  display: block;
  width: 100%;
  position: relative;
  overflow: hidden;
  box-sizing:border-box;
  border: 1px solid #999;
  border-radius: 5px;
  background:#EAEAEA;
  text-align: center;
  text-decoration: none;
  margin-right:5px;
 }

.box-inner {
  margin: 15px; 
  display:block; 
}

.box h2 {
  border-bottom: 1px solid #ccc; 
  padding: 0.4em 0; 
  color:#333!important;         
  font-size:2.3rem!important;
  line-height: 2.5rem;
}

a.button, button, span {
    background: #01827D;
    color: #FFFFFF !important;
    display: inline-block;
    font-family: 'Arial',sans-serif;
    font-size: inherit;
    margin: 10px 0;
    padding: 10px 20px;
    border:none;
    border-radius: 5px;
    text-decoration:none;
}
```

This will give you a page that looks as shown below:

![Baseline Code](https://raw.githubusercontent.com/TriValleyCoderDojo/beginner-web/master/screenshots/JS_02.PNG)

Okay, now that is more like it.  Something worthy of CoderDojo Ninjas like us!  Now we are ready to do some serious coding!  

Let's start with a simple alert box.  Let's make an embedded alert box that is triggered by clicking the mouse.  In the HTML add the following code to the end:

```html
<span class="button" onclick="alert('Hello World!');">Click Here</span>
```

Go ahead and click on the "Click Here" and you should get the pop-up alert box.  Pretty cool, huh!  But we are just getting started.  Let's try another alert box.  This will have both HTML and JavaScript.  Here we will create an actual button and a JavaScript function that gets used when you click.  

Add this HTML
```html
<button class="button" onClick="noClickHere()">DO NOT CLICK</button>  
```

Add this JavaScript
```javascript
var noClickHere = function() {
  alert("I told you not to click there");
}
```

## Catching a Mouse Event
In the previous section, we got our feet wet with theJavaScript onclick() event handler to display an alert box.  We used it without talking about it.  Here we are going into a bit more detail on the mouse events, and how we can use them in JavaScript.  

Your browser will generate events when things happen.  This is something the browser does by itself and we have no control over it.  All we are going to be doing is to take advantage of what the browser is already doing.  Browsers will generate a lot of different events.  Here we are only going to be talking about the Mouse events, but the nice thing is that once you understand Mouse events, then all of the other events will just be more of the same.  

Here is a good list of the most commonly used mouse events:

  * onclick - generated when a user clicks the mouse
  * ondblclick - generated when a user double-clicks the mouse
  * onmousedown - generated when a user depresses a mouse button (the first half of a click) 
  * onmouseup - generated when a user releases a mouse button (the second half of a click) 
  * onmouseout - generated when the mouse pointer off an element on the page
  * onmouseover - generated when the mouse pointer is over an element on the page
  * onousemove - generated when the mouse pointer moves while over an element on the page

We already used the simplest example of an event handler, when we used the onclick with the alert box.  This used the onclick event in the list above.  When we added the onclick=”some action” as an attribute to the element, we were enabling the onclick event handler for that element, and telling it to do some action (the thing that is in the quotes).  Initially, we used an embedded alert box, and then later we assigned a function as the action.  

However, the events are actually more interesting than just doing something.  The events are actually objects themselves, with their own set of properties.  We can use the event object to get additional information about the event.  There are two kinds of properties that you will find in the Mouse events:

1. Base Event Properties – these are properties that can be available in all events
2. Mouse/Keyboard Properties – these are specific to mouse or keyboard events


Base Event Properties:

| Property | Description |
|:---------|:------------|
| bubbles | Returns whether or not an event is a bubbling event |
| cancelable | Returns whether or not an event can have its default action prevented |
| currentTarget | Returns the element whose event listeners triggered the event |
| eventPhase | Returns which phase of the event flow is currently being evaluated |
| target | Returns the element that triggered the event |
| timeStamp | Returns the time (in milliseconds relative to the epoch) at which the event was created |
| type | Returns the name of the event |


Mouse/Keyboard Event Properties:

| Property | Description |
|:---------|:------------|
| altKey | Returns whether or not the "ALT" key was pressed when an event was triggered |
| button | Returns which mouse button was clicked when an event was triggered |
| clientX | Returns the horizontal coordinate of the mouse pointer, relative to the current window, when an event was triggered |
| clientY | Returns the vertical coordinate of the mouse pointer, relative to the current window, when an event was triggered |
| ctrlKey | Returns whether or not the "CTRL" key was pressed when an event was triggered |
| keyIdentifier | Returns the identifier of a key |
| keyLocation | Returns the location of the key on the device |
| metaKey | Returns whether or not the "meta" key was pressed when an event was triggered |
| relatedTarget | Returns the element related to the element that triggered the event |
| screenX | Returns the horizontal coordinate of the mouse pointer, relative to the screen, when an event was triggered |
| screenY | Returns the vertical coordinate of the mouse pointer, relative to the screen, when an event was triggered |
| shiftKey | Returns whether or not the "SHIFT" key was pressed when an event was triggered |

Okay, so its great that there is all this additional information available to us, but how do we get it?  Well, if you recall JavaScript functions can have parameters, and the event handlers will accept the event as a parameter.  So all we need to do is rewrite our function in a different way and we will expose all of these cool properties, as shown below:

HTML
```html
<span onclick="clickHandler(event);">Click Here</span>
```

JavaScript
```javascript
function clickHandler(event) {
  var eType = event.type;
  var eTarget = event.target;
  alert("Captured Event (type=" + eType + ", target=" + eTarget + ")" );
}
```

With the above, we are only retrieving the type and target properties, but you can do the same thing for any of the properties you may be interested in using for whatever reason.  You will find that once you start using the event properties in a web application all kinds of possible uses will come up.  



## Catching a Keyboard Event

The Keyboard events are similar to Mouse events, only these will happen when a user does something with the keyboard.  Here is a list of the most commonly used keyboard events:

  * onkeydown - generated when a user is pressing a key
  * onkeyup - generated when a user releases a key
  * onkeypress - generated when a user presses a key

With a onkeypress event, the Unicode value of the key pressed is stored in either the keyCode or charCode property, never both. If the key pressed generates a character (e.g., 'a'), charCode is set to the code of that character, respecting the letter case (i.e., charCode takes into account whether the shift key is held down).  Otherwise, the code of the pressed key is stored in keyCode.  This means taht charCode and keyCode values for a particular key are not the same. Also, the charCode is only returned if the event that triggered your event handler was keypress.  This is further confused by there being some differences between browsers as well, so you will need to be careful.  

So what is this Unicode stuff anyway?  Well, this is one of the ways that printable characters are represented.  What happens is that a character is converted into a number representation, so the computer can use it.  For example an 'A' will be converted to U+0042 (in hexadecimal) or 66 (in decimal).  There is a lot of information available on Unicode character encoding on the internet.  

Capturing the event and referencing the target (i.e., the actual key that was pressed) is achieved in a similar way to mouse events:

HTML
```html
<p>Enter something:<input onkeypress="keypressHandler(event);" /></p>
```

JavaScript
```javascript
function keypressHandler(e) {
  var evt = e ? e:event;
  var chrTyped, chrCode = 0;
  var sProperties = ''
   +(evt.keyCode ==null ? '':' keyCode=' +evt.keyCode )
   +(evt.charCode==null ? '':' charCode='+evt.charCode)
   +(evt.which   ==null ? '':' which='+evt.which)
  alert(sProperties);
}
```


## Updating Existing HTML


## Hide and Unhide HTML


## Validate Inputs


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

