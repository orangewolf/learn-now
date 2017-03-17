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

# jQuery absolute primer

## Include jQuery in your HTML file

test
