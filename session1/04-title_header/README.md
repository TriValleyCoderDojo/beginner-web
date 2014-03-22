# Adding a Title and Header

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

In addition, to the `<h1>` tags, there is a set of them `<h1>` to `<h6>`.  The smaller the number the smaller the font that will be used.  However, each header will bold to be different from regular text.  

------------------------------------

**Next HTML Topic:** [Adding Pictures](https://github.com/TriValleyCoderDojo/beginner-web/tree/master/session1/05-pictures)
