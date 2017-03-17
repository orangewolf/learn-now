# Tech Stack

## Front End
#### View
Web Browser
* HTML
* CSS
* Javascript

## Business Processes
#### Controller
Web Server
* Ruby
* Ruby on Rails

## Persistant Storage
#### Model
Database Server
* Data Model
* SQL
* PostgreSQL

## MVC

<a href="https://www.youtube.com/watch?v=XdCxfJki4t4" target="_blank">CS50 MVC</a>s

# HTML Basics

<iframe src="https://player.vimeo.com/video/152475600" width="640" height="400" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/152475600">HTML Basics Live Demo</a> from <a href="https://vimeo.com/user35425389">LEARN</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

See also <a href="https://www.youtube.com/watch?v=657YnQs2hVw" target="_blank">CS50 HTML</a>

## Tags to Know

These are tags with clear semantics:

```html
<html>
<head>
<body>
<title>
<h1>...<h6>
<strong>
<em>

<img src="...">

<a href="...">

<nav>
<section>
<aside>
<header>
<footer>

<ul>
<ol>
<li>

<table>
<thead>
<th>
<tbody>
<tr>
<td>
<tfoot>
<caption>
```

## General HTML Structure

```html
<html>
  <head>
  </head>
  <body>
    Stuff to show
  </body>
</html>
```

## Head Contents

```html
<html>
  <head>
    <title>My Web Page</title>
  </head>
  <body>
    Stuff to show in page
  </body>
</html>
```

## Body Contents

```html
<html>
...
  <body>
	<nav>
	  <p>Home</p>
	</nav>
    <h1>My Cool Web Page</h1>
    <h2>My First Section</h2>
    <h3>First Subsection of First Section</h3>
    <h3>Second Subsection of First Section</h3>
    <h2>My Second Section</h2>
  </body>
</html>
````

# Challenge
Create a basic html file with the following properties

1) a head with a title "hello world"
2) a body with an h1 tag that says "hello world"

# Git Basics

<iframe src="https://player.vimeo.com/video/154385357?title=0&byline=0&portrait=0" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

<table border="1">
  <tr>
    <th>Task</th>
    <th>Notes</th>
    <th>Git Command</th>
  </tr>
  <tr>
    <td>Tell Git who you are</td>
    <td>Configure the author name and email address to be used with your commits.</td>
    <td>
      git config user.name "Sam Smith"<br><br>
      git config user.email sam@example.com
    </td>
  </tr>
  <tr>
    <td>Create a new local repository</td>
    <td>No notes</td>
    <td>git init</td>
  </tr>
  <tr>
    <td>Check out a repository</td>
    <td>Create a working copy of a local repository:</td>
    <td>git clone /path/to/repository</td>
  </tr>
  <tr>
    <td>Add Files</td>
    <td>Add one or more files to staging (index):</td>
    <td>
      git add `filename` <br>or<br>
      git add .
    </td>
  </tr>
  <tr>
    <td>Commit</td>
    <td>Commit changes to head (but not yet to the remote repository):</td>
    <td>git commit -m "Commit message"</td>
  </tr>
  <tr>
    <td>Push</td>
    <td>Send changes to the master branch of your remote repository</td>
    <td>git push origin master</td>
  </tr>
  <tr>
    <td>Status</td>
    <td>List the files you've changed and those you still need to add or commit:</td>
    <td>git status</td>
  </tr>
  <tr>
    <td>Connect to a remote repository</td>
    <td>
      If you haven't connected your local repository to a remote server, add the server to be able to push to it.
      <br><br>
      List all currently configured remote repositories.
    </td>
    <td>
      git remote add origin `server`
      <br><br>
      git remote -v
    </td>
  </tr>
</table>

# Challenge
Create your Github account if you do not have one yet, then add your html page from above to each persons Github account.

Put the app to 1 account, then fork it to the other account.

# jQuery absolute primer

jQuery is a Javascript library that makes it easy to make web pages interactive.

<iframe width="640" height="360" src="https://www.youtube.com/embed/T2mFyPxL-fU" frameborder="0" allowfullscreen></iframe>

## First thing first with jQuery

We need to tell our html page to use jQuery. We can download the latest uncompressed version from <a href="https://jquery.com/download/" target="_blank">jQuery website</a> and
move it into your js folder or use the CDN as pictured below. jQuery, like many popular JavaScript libraries, serves their code from a public CDN, which we're using here. The convenient thing about using their CDN is that web browsers cache these files when they are first downloaded, which saves load time the next time the browser visits a page using that library.  If your browser has the file cached, it can use that file immediately instead of having to download it again. You can also serve JQuery from your own application.

Let's also make a file for our own JavaScript code, and then begin developing our page with this HTML. It's important that our own js file goes after the standard jQuery file, as it will rely on jQuery functionality that must be loaded first. And similar to Bootstrap, you can reference the file <a href="http://code.jquery.com" target="_blank" >directly</a> in the script tag.


```html
<!DOCTYPE html>
<html>
<head>
  <script src="https://code.jquery.com/jquery-2.2.4.min.js" integrity="sha256-BbhdlvQf/xTY9gja0Dq3HiwQF8LaCRTXxZKRutelT44=" crossorigin="anonymous"></script>
  <script src="yourfile.js"></script>
</head>
<body>
  <h1>This is a heading</h1>
</body>
</html>
```

## Document Ready?

When a web page loads, it is loading an HTML document, and that document will have other files to load with it, such as a css file, or javascript file. JQuery uses the DOM but since it simplifies HTML document traversing by accessing the p tags, div tags, button tags, and so on, the HTML document needs to be fully loaded before loading jQuery, otherwise jQuery is adding event listiners and button clicks to HTML tags that are not present. We load jQuery by wrapping it in a document `.ready` function.

Use the following file:

js/yourfile.js:
```javascript
alert("Your js is running");
$(document).ready(function() {
  alert("document is ready");
});
alert("Your js has run");
```

Jquery will run the callback function that is passed into `.ready()`. Then that function will run our code. Generally, it's a good idea to wrap your JavaScript in a function passed to `.ready()`


## Working with jQuery

Working with jQuery, is as easy as calling a function, because that's all jQuery is, a function. We can call jQuery two ways, by explicitly saying `JQuery` or to save time, and the most common way, by typing the `$`.

One thing that the jQuery function does is to select HTML elements on the page, based on the argument you pass into it. The selectors are exactly the same as those in CSS. And *all* of those tags will be selected.

These are selectors:

```javascript
jQuery("tag")
jQuery(".class")
jQuery("#id")
```
Instead of having to type jQuery every time, we can use `$` to replace jQuery. And from now on we will use `$` when accessing the jQuery library. ie

```javascript
$("tag")
$(".class")
$("#id")
```

## Your first click listener

Use the following in your HTML file:

```html
<!DOCTYPE html>
<html>
<head>
  <script src="js/jquery/1.12.0/jquery.min.js"></script>
  <script src="js/yourfile.js"></script>
</head>
<body>

  <h2>This is a heading</h2>

  <p>This is a paragraph.</p>
  <p>This is another paragraph.</p>
  <p id="test">This is another paragraph.</p>
  <p class="test">Yet another paragraph.</p>
  <button>Click me</button>

</body>
</html>
```


In your javascript file put in:
*js/yourfile.js*
```javascript
$(document).ready(function() {
  $("button").on(
    "click",
    function() {
      $("p").hide();
    });
  });
```

or

```javascript
$(document).ready(function(){
  $("button").on(
    "click",
    function() {
      $(".test").hide();
    });
});
```

or

```javascript
$(document).ready(function(){
  $("button").on(
    "click",
    function() {
      $("#test").hide();
  });
});
```

So, for example the code `jQuery("p")` selects all of the paragraphs on the page or
the code `jQuery(".test")` selects all the elements with `class="test"` and
the code `jQuery("#test")` selects the all the elements with the id of test.

After we select the elements, we use methods to attach an event handler to them.
In this case the `.on()` method. The event handler "listens" to the elements and responds when they're "clicked".

```html
...
<body>
  <!-- Add this -->
  <p>Click!</p>
  <button id="btn1">Don't Click</button>
  <button id="btn2">Really don't click</button>
</body>
...
```
Then in your javascript file:

```javascript
$(document).ready(function(){
  // Add this
  $("#btn1").on(
    "click",
    function() {
      alert("You clicked the button, didn't you?");
    });
  $("#btn2").on("click",
    function() {
      alert("You clicked the other button - try doing it again, I dare you!");
  });
  ...
});
```

And we can also make the buttons stop:

```javascript
$(document).ready(function(){
  // Change this
  $("#btn2").on("click",
    function(){
      alert("You clicked the other button - try doing it again!");
      $("#btn2").off("click");      // Add this line
  });
  ...
});
```

You can click on the buttons once and it will never work again. `.off()` removes a listener, in this case the click listener.

## Hiding and Seek

We can have elements that while still in the DOM are not visible.

```html
...
<body>
  <!-- Add this -->
  <p>If you click on the "Hide" button, I will disappear.</p>
  <p>If you click on the "Toggle" button, I will disappear and come back.</p>

  <button id="hide">Hide</button>
  <button id="show">Show</button>
  <button id="toggle">Toggle</button>

</body>
...
```

We can target out the first and second element of your selection

```javascript
$(document).ready(function(){
  $("#hide").on("click",
    function(){
      $("p").hide();
  });
  $("#show").on("click",
    function(){
      $("p").first().show();
  });
  $("#toggle").on("click",
    function(){
      // $("#second").toggle();
      $("p").eq(1).toggle();
  });
});
```

```html
...
<body>

  <!-- Add this -->
  <div id="div1" style="height:100px;width:300px;border:1px solid black;">

    This is some text in the div, not a p tag.
    <p>This is a paragraph in the div.</p>
    <p>This is another paragraph in the div.</p>

  </div>
  <br/>

  <button id="removeSecondPara">Remove second p element</button>

  <button id="removeP">Remove all p elements</button>

  <button id="removeDiv">Remove div element</button>

</body>
...
```
```javascript
$(document).ready(function(){
  // Add this
  $("#removeSecondPara").on("click",      
    function() {
      $("p").eq(1).remove();
  });
  $("#removeP").on("click",
    function() {
      $("p").remove();
  });
  $("#removeDiv").on("click",
    function() {
      $("#div1").remove();
  });
});
```

## Getting and Changing Content with jQuery

For general HTML elements, the `text()` method allows us to get and set the contents:

```javascript
alert($("p").text());
$("p").text("New contents...");
```

This is similar to how the `innerHTML` attribute in the DOM API works (except `text()` is a function).

However, with `input` elements, the `val()` method returns or sets the value attribute of the selected elements (similar to the `value` attribute in the DOM API):

```html
<p>Hello</p>
<input type="text" placeholder="Your name here"/>
<button>Click you</button>
```

```javascript
$("input").val();       -> "Input here..."
$("input").val("Hi There!");
```

# Challenge
**Note: It is really important to remember to use `$(document).ready`**

## Magic 8 Ball

As a user I can enter a question on a web page and magically get an answer to my question.


**View**

* Create an `input` tag to accept questions from the user. Give it an id of "question".
* Create a `button` tag to send the question to the Javascript code. Give it an id of "submit".
* Create a `p` tag to hold the answer the Magic 8 Ball sends back. Give it an id of "answer".

**Controller**

1. Create a click listener for the `button` tag, which opens up an alert.
1. Make the click listener show what is in the input field. Use the jQuery function `.val()`.
1. Make the click listener show what's in the input field in the paragraph section. Use the jQuery function `.text()`.
1. Clear the input field after the button is clicked.
1. Reuse your code from the previous Magic 8 Ball challenge to give a random answer.
