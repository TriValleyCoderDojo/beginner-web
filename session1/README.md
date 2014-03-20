# Build a web page - HTML - Lesson 1

## Overview

In this session we are going to use [HTML](http://en.wikipedia.org/wiki/HTML) to tell a story in the web browser that we can show our friends and family.  The story has been created for you, and although you may not be interested in this particular story, it might be a good idea to follow along with this story just to learn how to do it, and then create your own story, once you have mastered the HTML code.  

HTML is a markup language that we can use to add structure and formatting to content to be displayed in web browsers.

A web browser (commonly referred to as a browser) is a software application for retrieving, presenting and traversing information resources on the World Wide Web.  Examples are Firefox, Chrome, Internet Explorer and Safari. 

A web page is made up of many HTML elements, each a tag, or more commonly a set of tags, enclosed in angle brackets. The paragraph above is an example of how you mark a paragraph in html, by surrounding it in opening and closing `<p>` tags.

**Description**

To get started in web development we'll need to learn how to use html, so today we are going to:

* Start with a basic HTML 
* Tell our story and use HTML to add structure and formatting
* Display (render) the HTML in a browser

**Demo**

Below is an exmaple of HTML code:

```
<!DOCTYPE html>
<html>
  <head>
    <title>My day at work</title>
  </head>
  <body>
    <h1>My day at work</h1>
    <p>I had a good day at work. I was able to accomplish my goals and mentor a colleague.</p>
    <p>My goals included:</p>
    <ul>
      <li>Implement <strong>like</strong> feature</li>
      <li>Test emplementation in staging</li>
      <li>Deploy feature to production</li>
      <li>Blog about building and shipping the <strong>like</strong> feature</li>
    </ul>
    <p>When I think about it, today was actually an excellent day!</p>
  </body>
</html>
```

When this HTML is displayed (rendered) in a browser it will create a web page that looks like this:

![demo](http://cl.ly/image/0e1d3b2C3y2P/content#.png)

Check out the [live demo](http://codepen.io/anon/pen/vmibf) to experiment yourself.

## Prerequisites and Tools

To get started the only prerequites you will need is

* A willingness to learn
* A computer
* An internet connection
* Some kind of editing tool

In order to work with HTML you will need a way to edit the HTML and a way to render the HTML in a browser.  Once you become more skilled you will be able to edit the HTML files directly, open those in a browser, or even serve them from a web server.  However, for now let's keep it simple and use a tool that will do some of the work for us.  CodePen is a very good place to get started. The URL to their website it given below:


* [CODEPEN](http://codepen.io/pen/)

CodePen will do a lot for you, but it is also pretty easy to use.  You can use it without creating an account, but then you will not be able save your work as easily.  It is recommended that you create an Free account using the SignUp process, which will require a valid email address.  Here is a short Youtube video that gives an overview of [CodePen](https://www.youtube.com/watch?v=UF0_eMojlEw).

> Note: If you chose not SignUp and create an account, then you will need to manually keep track of the URL of each page you create.  The URL that is created will allow you to go back to those pages later.  


## Getting Started

To get started you should open a blank project on CODEPEN: [http://codepen.io/pen/](http://codepen.io/pen/)

![CODEPEN empty project](http://cl.ly/image/35081n120I42/content#.png)

For now ignore the JS and CSS areas so uncheck the boxes next to them.

![Uncheck JS and CSS](http://cl.ly/image/1f3C0E1O1t2Q/content#.png)

Now add the minimal amount of HTML to make the page work. Start by clicking in the HTML area and adding opening and closing `<html>` tags.  Notice it comes in an opening, `<html>`, and closing, `</html>` tag.  The combination of these two tags are used to tell the browser that everything in between them will be HTML code.  Most HTML tags will use the opening and closing tags approach, with only a few easy to remember exceptions.  

```html
<html>
</html>
```

Your screen should look like this now:

![CODEPEN after adding html tags](http://cl.ly/image/1y1H1M1n2r1m/content#.png)

Next add the `<head>` and `<body>` tags. 

* The `<head>` tags are used to give additional information about this page.  Generally, the stuff inside of these tags will not be be displayed.  There can only be one pair of these.  

* The `<body>` tags tell the web browser that this is the stuff that will be rendered.  Again there can only one pair. 

Now our HTML should look like this:

```html
<html>
  <head>
  </head>
  <body>
  </body>
</html>
```

This is the base HTML that every page should have.  

## Telling Your Story

Now you can start telling your story by typing some text inside of the `<body>` tags! Here is an example:

```html
<html>
  <head>
  </head>
  <body>
    Today I took the dogs to the park and we had a great time!
  </body>
</html>
```

![Basic demo of HTML in action](http://cl.ly/image/2P3l3V1A302i/content#.png)

Now tell more of your story, what else happened?

```html
<html>
  <head>
  </head>
  <body>
    Today I took the dogs to the park and we had a great time!

    After the dogs played with their friends we took a walk around the track together.
  </body>
</html>
```

![Telling more of the story](http://cl.ly/image/2w1Q090V1b2t/content#.png)

## Using Paragraphs

Here you can see that we separated my paragraphs by using new lines (on the right) but the rendered html (on the left) didn't get separated into paragraphs. This is because HTML does not recognize the new lines as paragraph separators.  In fact, HTML treats spaces, tabs and new lines as just a single character.  In order to create paragraphs in HTML we need to use paragraph (`<p>`) tags.

Add the `<p>` around the paragraphs:

```html
<html>
  <head>
  </head>
  <body>
    <p>Today I took the dogs to the park and we had a great time!</p>
    <p>After the dogs played with their friends we took a walk around the track together.</p>
  </body>
</html>
```

![Adding paragraph tags](http://cl.ly/image/1U053V060k0u/content#.png)

Now the paragraphs are displayed correctly!

## Adding a Title and Header

Next, we need to add a title to your page. The title is required and there can only be one per page.  Ordinarily, the title will appear in the browser title bar, but since we are using CodePen you will not see the title bar.  You should still add it, so when you move your page to an actual web server it will be there.  We will need to add the `<title>` to the `<head>` as shown below.

Also, we need to add a main header.  The header will need to go in the body.  It is usually at the top of the page and gives the reader an idea of what the page is about.  Unlike the title, there can be any number of headers.  We will need to use the `<h1>` tags and add it to the `<body>`.

```html
<html>
  <head>
    <title>A day at the dog park</title>
  </head>
  <body>
    <h1>A day at the dog park</h1>
    <p>Today I took the dogs to the park and we had a great time!</p>
    <p>After the dogs played with their friends we took a walk around the track together.</p>
  </body>
</html>
```

![Story with title](http://cl.ly/image/1e352r043A1x/content#.png)

In addition, to the `<h1>` tags, there is a set of them `<h1>` to `<h6>`.  The smaller the number the smaller the smaller the font that will be used.  However, each header will bold to be different from regular text.  

## Picture Time!

This story would be a lot more interesting with pictures! Adding a picture to our story is simple, we just need to use the `<img>` tag and tell it where our image is.

The `<img>` tag has an attribute called `src` and this is a URL to where the image has been saved. In this example, the image has been saved and then mapped with a bitly URL, and we are using a fully qualified link.  However, that is not the only way images can be referenced.  They could be just a file name that the page can reach directly.  More information can be found at [HTML img tag](http://www.w3schools.com/tags/tag_img.asp).

Here is an example `<img>` tag:

```html
<img src="http://f.cl.ly/items/2f473l1d233S0S1k3J3d/dogs-playing.jpg">
```

Now we can add a couple of images to our story, as shown below:

```html
<html>
	<head>
		<title>A day at the dog park</title>
	</head>
	<body>
		<h1>A day at the dog park</h1>
		<p>Today I took the dogs to the park and we had a great time!</p>
		<img src="http://f.cl.ly/items/2f473l1d233S0S1k3J3d/dogs-playing.jpg">
		<p>After the dogs played with their friends we took a walk around the track together.</p>
		<img src="http://f.cl.ly/items/0o0T0V0g261C1R0I022z/walking-the-track.jpg">
	</body>
</html>
```


![Story with images](http://cl.ly/image/3w2d1C0P1N3I/content#.png)

## Strong and Emphasis

Sometimes we want to bring more attention to parts of our story. One way we can do this is by using the `<strong>` tag to make certain parts of our story look bolder compared to other parts. Here is an example:

```html
<html>
  <head>
    <title>A day at the dog park</title>
  </head>
  <body>
    <h1>A day at the dog park</h1>
    <p>Today I took the dogs to the park and <strong>we had a great time!</strong></p>
    <img src="http://f.cl.ly/items/2f473l1d233S0S1k3J3d/dogs-playing.jpg">
    <p>After the dogs played with their friends we took a walk around the track together.</p>
    <img src="http://f.cl.ly/items/0o0T0V0g261C1R0I022z/walking-the-track.jpg">
  </body>
</html>
```

![Story with strong](http://cl.ly/image/1u083V0I0Y3O/content#.png)

We can bring emphasis to parts of our story by *making them italic*. We use the `<em>` tag for emphasis. Here is an example:

```html
<html>
  <head>
    <title>A day at the dog park</title>
  </head>
  <body>
    <h1>A day at the dog park</h1>
    <p>Today I took the dogs to the park and <strong>we had a great time!</strong></p>
    <img src="http://f.cl.ly/items/2f473l1d233S0S1k3J3d/dogs-playing.jpg">
    <p>After the dogs played with their friends <em>we took a walk around the track together.</em></p>
    <img src="http://f.cl.ly/items/0o0T0V0g261C1R0I022z/walking-the-track.jpg">
  </body>
</html>
```

![Story with emphasis](http://cl.ly/image/45033t3W3v3R/content#.png)

## Lists

You can easily add a list to your story using `<ul>` and `<li>` tags. Here is an example:

```html
<html>
	<head>
		<title>A day at the dog park</title>
	</head>
	<body>
		<h1>A day at the dog park</h1>
		<p>Today I took the dogs to the park and <strong>we had a great time!</strong></p>
    <img src="http://f.cl.ly/items/2f473l1d233S0S1k3J3d/dogs-playing.jpg">
    <p>After the dogs played with their friends <em>we took a walk around the track together.</em></p>
    <img src="http://f.cl.ly/items/0o0T0V0g261C1R0I022z/walking-the-track.jpg">
		<p>While we were at the dog park we saw many kinds of dogs, including:</p>
		<ul>
			<li>Poodles</li>
			<li>Great Danes</li>
			<li>Black Labs</li>
		</li>
	</body>
</html>
```

The `<ul>` tag tells the browser this is a list of items. The `<li>` tags are used around each list item.

![Story with list of dogs](http://cl.ly/image/3E2k0C3k3u3N/content#.png)

If you want the list to use numbers instead of bullet points you can change the `<ul>` tag (unordered list) to an `<ol>` tag (ordered list).

```html
<html>
	<head>
		<title>A day at the dog park</title>
	</head>
	<body>
		<h1>A day at the dog park</h1>
		<p>Today I took the dogs to the park and <strong>we had a great time!</strong></p>
    <img src="http://f.cl.ly/items/2f473l1d233S0S1k3J3d/dogs-playing.jpg">
    <p>After the dogs played with their friends <em>we took a walk around the track together.</em></p>
    <img src="http://f.cl.ly/items/0o0T0V0g261C1R0I022z/walking-the-track.jpg">
		<p>While we were at the dog park we saw many kinds of dogs, including:</p>
		<ol>
			<li>Poodles</li>
			<li>Great Danes</li>
			<li>Black Labs</li>
		</ol>
	</body>
</html>
```

![Story with ordered list](http://cl.ly/image/3x2t1c1N1v3o/content#.png)

## Hyperlinks

One of the things that makes web pages so amazing for telling stories is you can **link** things together with other web pages on the internet and it is really easy to do!

In the pervious example I included three kinds of dogs that we saw at the park, now I'm going to use hyperlinks (the `<a>` tag) to link the dog names to their descriptions on Wikipedia.

The `<a>` tag has an attribute called `href` and we will set that attribute equal to the url of the web page we want to link to. Here is an example where I link the word Poodles to the web page about Poodles on Wikipedia:

```
<a href="http://en.wikipedia.org/wiki/Poodle">Poodles</a>
```

Here is what it looks like in the context of our story:

```html
<html>
	<head>
		<title>A day at the dog park</title>
	</head>
	<body>
		<h1>A day at the dog park</h1>
		<p>Today I took the dogs to the park and <strong>we had a great time!</strong></p>
    <img src="http://f.cl.ly/items/2f473l1d233S0S1k3J3d/dogs-playing.jpg">
    <p>After the dogs played with their friends <em>we took a walk around the track together.</em></p>
    <img src="http://f.cl.ly/items/0o0T0V0g261C1R0I022z/walking-the-track.jpg">
		<p>While we were at the dog park we saw many kinds of dogs, including:</p>
		<ul>
			<li><a href="http://en.wikipedia.org/wiki/Poodle">Poodles</a></li>
			<li><a href="http://en.wikipedia.org/wiki/Great_Dane">Great Danes</a></li>
			<li><a href="http://en.wikipedia.org/wiki/Labrador_Retriever">Black Labs</a></li>
		</li>
	</body>
</html>
```

## Telling More Than One Story

If you want to write another story you don't have to start a whole new web page, you can use the same page you have been working on and use HTML to indicate where one story stops and the next begins. Typically we will use `<article>` tags to accomplish this. Here is an example:

```html
<html>
  <head>
    <title>A day at the dog park</title>
  </head>
  <body>
    <h1>Dog Stories</h1>
    <article>
      <h2>A day at the dog park</h2>
      <p>Today I took the dogs to the park and <strong>we had a great time!</strong></p>
      <img src="http://f.cl.ly/items/2f473l1d233S0S1k3J3d/dogs-playing.jpg">
      <p>After the dogs played with their friends <em>we took a walk around the track together.</em></p>
      <img src="http://f.cl.ly/items/0o0T0V0g261C1R0I022z/walking-the-track.jpg">
      <p>While we were at the dog park we saw many kinds of dogs, including:</p>
      <ul>
        <li><a href="http://en.wikipedia.org/wiki/Poodle">Poodles</a></li>
        <li><a href="http://en.wikipedia.org/wiki/Great_Dane">Great Danes</a></li>
        <li><a href="http://en.wikipedia.org/wiki/Labrador_Retriever">Black Labs</a></li>
      </li>
    </article>
    <article>
      <h2>Driving Across The Country With Leo and Bailey</h2>
      <p>A year ago we drove across the country <em>with Leo and Bailey</em> when we moved from Indiana to California.</p>
      <img src="http://cl.ly/image/3G2Z3x0G3Z46/content#.png">
      <p>One time after stopping to eat lunch we found Leo in the front seat ready to drive. <strong>This made us laugh really hard :)</strong></p>
    </article>
  </body>
</html>
```

You will notice a few new things in the html above. We added a second story, we enclosed both stories in `<article>` tags, we changed the story titles to use `<h2>` (Heading 2) tags, and we changed the `<h1>` (Heading 1) at the top to say **Dog Stories**.

## Style

In the next lesson we will start learning how to add style to our story using html attributes and css. Here is an example to help get you excited about the next lesson.

In Codepen we want to check the box next to CSS and then paste the following css code into the CSS box:

```css
body {
  font-family: Arial;
  background-color: #eee;
  color: green;
}

img {
  border: 2px solid green;
  padding: 2px;
}
```

![Story with CSS](http://cl.ly/image/002B0l3l090P/content#.png)

## Advanced Topics

### HTML Doctype

Web browsers look for a document type tag at the beginning of an HTML document in order to determine how they should read and render the HTML. We can add the `<!DOCTYPE html>` tag to our web page to tell browsers that we are using the latest version of HTML.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>A day at the dog park</title>
  </head>
  <body>
    <h1>A day at the dog park</h1>
    <p>Today I took the dogs to the park and <strong>we had a great time!</strong></p>
    <img src="http://f.cl.ly/items/2f473l1d233S0S1k3J3d/dogs-playing.jpg">
    <p>After the dogs played with their friends <em>we took a walk around the track together.</em></p>
    <img src="http://f.cl.ly/items/0o0T0V0g261C1R0I022z/walking-the-track.jpg">
    <p>While we were at the dog park we saw many kinds of dogs, including:</p>
    <ul>
      <li>Poodles</li>
      <li>Great Danes</li>
      <li>Black Labs</li>
    </ul>
  </body>
</html>
```
You can read more about document type [here](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/Introduction_to_HTML5).

## Other Resources

* [HTML Glossary](http://www.codecademy.com/glossary/html)
* [Mozilla Developer Network](https://developer.mozilla.org/en-US/)
