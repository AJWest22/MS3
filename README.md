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

*Books2* This holds the books that are recommended on the site already and their authors.

*genres* is used to connect the dropdown menus with the genres on on the homepage to the database.

*genres2* is used in the dropdown menu on the add-review page to connect the genres with the genre field on the form. Due to technical difficulties, it wasn't possible to connect the genres collection with the form, so genres2 was created. The site was getting errors, and the genres weren't displaying correctly.

*improvements* collection holds information submitted from the contact us page, including email address to contact the person with and their feedback.

*reviews* collection holds the data submitted through the add a review page, this includes, the genre, the name of the book, the name of the person who submitted it, the author and the review itself.

*users* holds the information of people who have created accounts to the site.

PyMongo is currently used to connect the database with the site. 


**DESIGN:**

*TYPOGRAPHY* The site uses Oswald font (imported from google fonts) and Roboto (also imported from Google fonts). The reason for these two fonts is they are becoming increasingly popular amongst web designers, and also lift the site a bit. For example the header's oswald font creates a bold, dark eye catching effect for the header. The nav bar also has a text-shadow applied to it, again using the Materialize CSS framework, ('text-shadow') to help make it stand out and be more readable against the paler blue background.

*COLORS:* The site uses predominantly blue coloring, and the code used to make it comes from the color classes in the Materialize CSS framework. The navbar uses the class **blue lighten-4** which has the corresponding hex code of: #bbdefb. The dropdown menus uses the Materialize CSS color class of **blue accent-3**, which has the corresponding hexcode of #2979ff. 

*IMAGES* The images used come from pixabay and pexels, and links to the images are used to connect them to their corresponding place on the site. 


**FEATURES TO BE ADDED**

This project has some features I would like to add at a later date. 

1: The ability for users to display their social media pages on their profile. This was attempted but due to time constraints couldn't be done in time.

2: Pagination: Pagination was originally going to be used to keep the users reviews displayed in an orderly fashion, however after much research, I couldn't find anything on Pagination for PyMongo, and MongoDB, it was using SQL Lite and SQL Alchemy, and I needed to install MongoEngine instead of PyMongo. 

3: Profile picture: Currently a carousel from Materialize CSS is used to display images on the site and they can't chosen by the user, at some pont I'd like to be able to add the option for the user to display their own profile picture on the site instead of relying on the sites images.