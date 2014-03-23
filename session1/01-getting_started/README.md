# Getting Started

To get started you should open a new bin project on : [http://jsbin.com/](http://jsbin.com/)

![JS Bin empty bin](https://raw.githubusercontent.com/TriValleyCoderDojo/beginner-web/master/screenshots/js_bin_start.PNG)

Across the top of the page in the center, you will notice five buttons: HTML, CSS, JavaScript, Console and Output.  For now you will only want to have the HTML and Output selected.  You can tell they are selected because the button will turn light blue and a window will appear that matches the button.  

### Base HTML 

You will notice that JS Bin has already created some HTML code for you.  This is the base HTML that every page needs to have, and although JS Bin has already given it to you, let's take a minute to explain it.  At the top there is a DOCTYPE element, `<!DOCTYPE html>`.  Web browsers look for a document type tag at the beginning of an HTML document in order to determine how they should read and render the HTML. You should always add this, and it is telling the web browser that we are using the latest version of HTML.  You can read more about document type [here](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/Introduction_to_HTML5).

Next you will notice the opening, `<html>`, and closing, `</html>` tags.  The combination of these two tags are used to tell the browser that everything in between them will be HTML code.  Most HTML tags will use the opening and closing tags approach, with only a few easy to remember exceptions.  

Next are the `<head>` and `<body>` tags. 

* The `<head>` tags are used to give additional information about this page.  Generally, the stuff inside of these tags will not be be displayed.  There can only be one pair of these.  

* The `<body>` tags tell the web browser that this is the stuff that will be rendered.  Again there can only one pair. 

This is the base HTML that every page should have. 

```html
<html>
  <head>
  </head>
  <body>
  </body>
</html>
```

----------------------------

**Next HTML Topic:** [Your First Text](https://github.com/TriValleyCoderDojo/beginner-web/tree/master/session1/02-first_text)

