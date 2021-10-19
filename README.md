MS3 README

OVERVIEW:
This site was created for MS3 submission for Code Institute.
The site's name is Book Recommendations.
The source code can be found on GitHub
The site is deployed using Heroku

The purpose of this site is to help people find books they might like to read in a particular genre, and leave 
recommendations on books they have read and would recommend. Users can browse the site and read the "Quick Picks" 
recommendations, but must be logged in to add a review, edit, and delete a review. 

There are currently two types of accounts at the moment:

**Username**: Reader **Password**: Reader

and 

**Username**: Admin **Password** Admin

Both accounts are test accounts used to test site functionality, for example: 
Reader was used to check if accounts were showing on the Database, and Admin was used to check if only reviews added by admin could be edited by admin. 


**UX GOALS:**

Users can create, edit and delete reviews on books they've read, either books recommended on the site or one they've read themselves, and browse recommendations by others.


**OWNERS GOALS:**

Provide a service that encourages people to read books and genres they may not normally try, and find good books.

**ABOUT THE SITE:**

The site has a total of 9 pages. Some are only visible to users who are logged in (profile page for example).
Users who are logged in have the option to add, edit and delete their reviews, while those who aren't logged in
can only browse other people's reviews. The genres chosen range from the ones that tend to be more popular among
people (Crime and Thriller) and those that aren't (Fantasy and Horror). 

**Code Used**

The site is build using:
*HTML* to provide the site's structure

*CSS* to add style to the site.

*PYTHON* to add the backend functionality to the site.

FRAMEWORKS

*MATERIALIZE CSS* is used to help style the site, and add some features to the site using JQUERY. The code used by Materialize is marked. I chose to work with Materialize, as it incorporated bootstrap, that helps with the making the site mobile friendly, and also to challenge myself with learning a new framework. Materialize may help with styling, but there can be some speificity issues when using it. For example my issues of using it include: trying to size images in the carousel, and header images on the home and reviews pages. (The former has been resolved, but the latter is still not fullwidth). 

*FLASK* is used to help with the structuring of Python, and can be seen in the site using the for loops on the homepage that get the books from the server {% for books in books2 %}

*Jinja Template* is used to render the templates and write code similar to Python.


FILES MADE:

There were 9 HTML files made in this project, 2 python files, a JavaScript file, a CSS file, a Procfile and requirements.txt file. 

Most can be viewed on GitHUb, however the env.py file contains sensitve information, and has not been pushed to GitHub.

The HTML files are stored in the templates folder, as they form the basis of the site. 

The static folder contains the JavaScript and CSS files, and is used to help structure the code.

The app.py file provides the backend code that handles the data of the site. It is used for submitting data to the database and pulling information from the database. 


**The DataBase**

MongoDB is used for the site as it offers a open source document-orientated database. 

*Structure* The Database has 6 collections described below:

*Books2* This holds the books that are recommended on the site already.

*genres* is used to connect the dropdown menus with the genres on on the homepage to the database.

*genres2* is used in the dropdown menu on the add-review page to connect the genres with the genre field on the form. Due to technical difficulties, it wasn't possible to connect the genres collection with the form, so genres2 was created. The site was getting errors, and the genres weren't displaying correctly.

*improvements* collection holds information submitted from the contact us page, including email and feedback.

*reviews* collection holds the data submitted through the add a review page, this includes, the genre, the name of the book, the name of the person who submitted it, the author and the review itself.

*users* holds the information of people who have created accounts to the site. 





