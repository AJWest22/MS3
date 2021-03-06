**MS3 README**

## Table of Content

1. [Overview](#overview)

2. [Site Goals](#site-goals)
    1. [UX Goals](#ux-goals)
    2. [Siteowners Goals](#siteowners-goals)
    3. [User Stories](#user-stories)
    4. [Siteowner Stories](#siteowner-stories)

3. [About The Site](#about-the-site)
    1. [Target Audience](#target-audience)

4. [Development Lifecycle](#development-lifecycle)
    1. [HTML Development](#html-development)
    2. [CSS Devlopment](#css-development)
    3. [Python Development](#python-development)
    4. [JQUERY Development](#jquery-development)
    5. [Pagination](#pagination)

5. [Bugs](#bugs)

6. [Code Used](#code-used)
    1. [Frameworks](#frameworks)
    2. [Files Made](#files-made)

7. [The Database](#the-database)
    1. [Database Collection](#database-collection)
    2. [Mongo URI Keys](#mongo-uri-keys)

8. [Design](#design)
    1. [Typography](#typography)
    2. [Colors](#colors)
    3. [Images](#images)

9. [Code Features](#code-features)

10. [Features to be Added](#features-to-be-added)

11. [Testing](#testing)
    1. [HTML Validation](#html-validation)
    2. [CSS Validation](#css-validation)
    3. [Python Validation](#python-validation)
    4. [Browser Compatibility](#browser-compatibility)
    5. [Devices Tested On](#devices-tested-on)

12. [Deployment](#deployment)

13. [Credits](#credits)
     1. [Icons](#icons)
     2. [Imagery](#imagery)
     3. [CSS Framework](#css-framework)
     4. [JQuery Framework](#jquery-framework)

14. [Acknowledgements](#acknowledgements)
  



## **Overview**
 - This site was created for MS3 submission for Code Institute.
 - The site's name is Book Recommendations.
 - The source code can be found on GitHub
 - The site is deployed using Heroku

 - The purpose of this site is to help people find books they might like to read in a particular genre, and leave 
   recommendations on books they have read and would recommend. Users can browse the site and read the books in the dropdown menu
   recommendations, but must be logged in to add a review, edit, and delete a review. 

 - There are currently two types of accounts at the moment:

     **Username**: Reader **Password**: Reader
    and 

    **Username**: Admin **Password** Admin
Both accounts are test accounts used to test site functionality, for example: Reader was used to check if accounts were showing on the Database, and Admin was used to check if only reviews added by admin could be edited by admin. 

View site [here](https://flask-book-site.herokuapp.com/)

## **Site Goals**

### **UX Goals**

 - Users can create, edit and delete reviews on books they've read, either books recommended on the site or one they've read themselves, and browse recommendations by others.

 - Users can also leave feedback or ask any questions they may have regarding the site.


### **Siteowners Goals**

 - Provide a service that encourages people to read books and genres they may not normally try, and find good books.

 - Ensure the database continues to accept new data, such as: books, reviews, users, and feedback or questions.


 ### **User Stories**

 - As a user of this site I want to find a good book from a variety of genres

 - As a user I want to know my feedback on the site has been submitted.

 - As a user i want to know if my login was successful or not.

 - As a user I want a easy to use, simple site.

 - As a user I want the ability to edit or delete any of my recommendations


### **Siteowner Stories**

 - As the owner of this site, I want to create a easy to use site that serves a purpose.

 -  As the owner of this site, I want users to know their feedback and any questions have been submitted

 -  As the owner of this site, I want users to come back to this site.

 - As the owner of this site, I want users to be able to have control over their reviews, so edit and delete them as well as the ability to create them. 

 - As the owner of this site I want users login details to be stored safely and securely by encrypting the password on the server.

 - As the owner of this site I want users to know their data is secure. 


## **About The Site**

 - The site has a total of 9 pages. Some are only visible to users who are logged in (profile page for example).
 - Users who are logged in have the option to add, edit and delete their reviews, while those who aren't logged in
 - can only browse other people's reviews. The site's purpose is to help people find books they'd like to read, and users can
 - create, edit and delete recommendations/reviews on books they have read. The genres chosen range from the ones that tend to be - more popular among people (Crime and Thriller) and those that aren't (Fantasy and Horror) so that it caters for a wide array 
 - of audiences. 

### **Target Audience**
 - The site is primarily aimed and adults/young adults who are either big readers and want to find thier next book, or people who want to read more but aren't sure what to read. 


## Development Lifecycle

This is the second version of the site. The original didn't have enough commits, so this is the same site, and code, copied over from the original submission. The following is a brief overview of the development of the site, and contains a list of bugs that were made and corrected. Any current bugs that haven't been solved are recorded in the bugs section of this README. The overview is divided into four sections: Python Development, HTML Development, and CSS Development and JQUERY Development. 

There was one bug when setting up the folders and files needed for the site, when initially creating the static folder and the CSS, Images and JS folders, they initially all ran together, and couldn't be seperated. This resulted in long filepaths, and made it harder to use, for example to access the JS for the site, the filepaths was 'static/css/images/js/style.css/script.js'. To oslve this, the folders were deleted before being re-added and and creating each folder individually, then dragging and dropping each folder individually into the main static folder. 

### HTML Development

The HTML files form the base structure of the site. A base.html template was used to contain the navbar and other sections that needed to appear on all pages, for example any flash messages. The base.html file also contains the scripts needed for the JQUERY, images, and CSS. Jinja Templating is used to copy the blocks across the various other HTML files/pages. There are 9 HTML files for this project: 

- The base.html file which contains the template for the rest of the HTML files to follow, and contains important parts of the site functionality.

- Books.html which gets the books and genres from the databe and displays them onto the site.

- signup.html has a form that is used to sign up new users to the site.

- login.html which holds the form used by users to login to the site and view their profile. 

- profile.html holds a user's profile page, at the moment it is very basic styling, and at some point I would like to edit this and add more features, such as a customizable profile picture.

- reviews.html gets the reviews on the databse, and displays them on the site.

- add_review.html adds a new review to the database, which can then be displayed on the reviews page

- edit_review.html is used to allow users to edit their reviews.

- delete_review.html allows users to delete their reviews.

- contact_page.html is used to submit suggestions to improve the site. 

Forms are used a lot through the site, and can be found in more detail in the [forms](#forms) section of this README.

### CSS Development

MaterializeCSS is used a lot for the design and adding some key features to the site, for example: the slider, and carousel. MaterializeCSS also plays a part in the JQERY used in this site. The CSS design has not changed that much over the course of development, and is near identical to the original site, the only difference being the nav bar color, which was originally a MaterializecSS class called 'blue lighten-4', but is now blue lighten-2. 

### Python Development

The Python was the hardest part of this site to make. Some of the variables were changed during the site's development to make the code more readable, and this created several bugs. For example when getting the genres from the databse to display on the site, the code used was initially: genres = list(mongo.db.genres.find()) and genres=genres in the app.py file, and then '{% for genres in genres %} in the books.html file. Due to this being considered ba dcoding practise, it was then changed to 'genre' to make the code more readble and easier to follow. So it is now: genre = list(mongo.db.genres.find()) and {% for genre in genres %}.
When this was initially done, the genres didn't display in the dropdown menu on the homepage, this was corrected by checking the for loop, and correcting it.

There are functions for most things on the site, the user can interact with For example a function for getting the books, and for logging in/out and signing up. 

### JQUERY Development

The JQUERY used for this site comes from MaterializeCSS, and is used to add interactivity to the site. For example the slider and the carousel. The JQUERY can be found on MaterializeCSS site, at the bottom of each module. 

### Pagination

Pagaination was added in the later stages of development. Flask-paginate is used to implement this on the reviews page, so the reviews count will be displayed on the reviews page.

## Bugs

There were some bugs during development of this site: 

- 1: Originally the a collection was created called 'Books' that was originally intended to hold the books on the database and display them on the site. However due to some technical difficulties, 'Books' was discarded, and 'Books2' was created. 

- 2: During the Python development there were several issues with the reviews CRUD functionality. An error appears saying review wasn't defined, this was fixed by updating it to 'reviews', to match the backend variable.

- 3: There was one instance where the books wouldn't display on the site, this was fixed by changing books2 to book, to match the backend variable.

- 4: There is currently a bug with the carousel, the action image doesn't display for some reason. I have tried adding different images, and taking it out completely and re-adding it, but the image can't be displayed for some reason.

- 5: When editing a review it can sometimes not open the review. If this happens, double click the review's edit button and it should then open and allow for it to be edited.


## **Code Used**

 The site is build using:
 - *HTML* to provide the site's structure and features, for example the contact form.

 - *CSS* to add style to the site, for example the font of the typography.

 - *PYTHON* to add the backend functionality to the site, for example sending data to the database.

 - *JQUERY* to offer interactivity to the site, for example dropdown menus.


### **Frameworks**

 - *MATERIALIZE CSS* is used to help style the site, and add some features to the site using JQUERY. The code used by Materialize is marked. I chose to work with Materialize, as it incorporated bootstrap, that helps with the making the site mobile 
 friendly, and also to challenge myself with learning a new framework. Materialize may help with styling, but there can be some
 speificity issues when using it. For example some issues I had with using it included: trying to size images in the carousel, and the header images on the home and reviews pages. (The former has been resolved, but the latter is still not fullwidth). 

 - *FLASK* is a framework and is used to help with the structuring of Python, and can be seen in the site using the for loops on the homepage that get the books from the server {% for books in books2 %}

 - *Jinja Template* is used to render the templates and write code similar to Python. For example: render_template(signup.html)


### **Files Made**

 - There were 9 HTML files made in this project, 2 python files, a JavaScript file, a CSS file, a Procfile and requirements.txt file. 

 - Most can be viewed on GitHUb, however the env.py file, that was created to connnect the database with the site, contains 
   sensitve information, and has not been pushed to GitHub.

 - The HTML files are stored in the templates folder, as they form the basis of the site, and it helps structure and organise 
   the code. 

 - The static folder contains the JavaScript and CSS files, and is used to help structure the code files, and keep things orderly.

 - The app.py file provides the backend code that handles the data of the site. It is used for submitting data to the database and pulling information from the database. 

 - The env.py file that was created contains information regarding the database and has not been pushed to GitHub.



## **The DataBase**

MongoDB is used for the site as it offers a open source document-orientated database. 

- *Structure* The Database has 6 collections described below:

- *Books2* This holds the books that are recommended on the site by the site owner and their authors in their correct genre.

- *genres* is used to connect the dropdown menus' genres on on the homepage to the ones stored in the database.

- *genres2* is used in the dropdown menu on the add-review page to connect the genres with the genre field on the form. Due to 
technical difficulties, it wasn't possible to connect the genres collection with the form, so genres2 was created. The site was getting errors, and the genres weren't displaying correctly.

- *improvements* collection holds information submitted from the contact us page, including email address to contact the person   with and their feedback.

- *reviews* collection holds the data submitted through the add a review page, this includes, the genre, the name of the book,  
the name of the person who submitted it, the author and the review itself. 

- *users* holds the information of people who have created accounts to the site. Information collected in this collection on the server includes: username, and their password which can't be read using password_hash encryption. 

PyMongo is currently used to connect the database with the site, as it is simpler to use than other Python frameworks, and was the one I felt most confident using.


### **Database Collections** 

Below are some images of the collections in the database so you can see how data is stored.

- <details><summary>Books2 Collection which contains data on the books and authors:</summary>
  <img src="static/images/books2.jpg">
  </details>

- <details><summary>Genres holds the data on the genres used in the dropdowns menu on the homepage:</summary>
  <img src="static/images/genres.jpg">
  </details>

- <details><summary>Genres2 holds the data on the genres used in the dropdown menu on the review page:</summary>
  <img src="static/images/genres2.jpg">
  </details>

- <details><summary>Users has the data on the users of the site, password has been encrypted so can't be read.</summary>
  <img src="static/images/users.jpg">
  </details>

- <details><summary>Improvements has the feedback data. The feedback key can also hold question data.</summary>
  <img src="static/images/improvements.jpg">
  </details>

- <details><summary>Reviews has the information on the reviews left by users on the site.</summary>
  <img src="static/images/reviews.jpg">
  </details>

  ### Mongo URI Keys

  The following is a brief overview on how to make a Mongodb database

  1. Create an account at mongodb

  2. Create a database cluster

  3. Select the cluster, and in the collections section create a database and create 5 collections under the database: memories, comments, ratings, tournaments, users 

  4. In the database access, create a user and allow the user read/write access. Note the username

  5. In the network access tab, allow network access from the ip-address of the application connecting to the database

  6. In the Databases section click Connect, and select connect your application

  7. Note the MONGO_URI, MONGO_DBNAME and user, these parameters are used when deploying locally(env.py file) and deploying on the likes of heroku(config vars)

## **Design**

The site was designed to have a more relaxed feel to it, and easy to use. The site uses simpe coloring, fonts and imagery to create and achieve this effect. 


### Typography 
- The site uses Oswald font (imported from google fonts) and Roboto (also imported from Google fonts). The reason for these two  fonts is they are becoming increasingly popular amongst web designers, and also lift the site a bit. For example the header's oswald font creates a bold, dark eye catching effect for the header. The nav bar also has a text-shadow applied to it, again using the Materialize CSS framework, ('text-shadow') to help make it stand out and be more readable against the paler blue background.


### Colors 
 - The site uses predominantly blue coloring, and the code used to make it comes from the color classes in the Materialize CSS framework. The navbar uses the class **blue lighten-4** which has the corresponding hex code of: #bbdefb. The dropdown menus uses the Materialize CSS color class of **blue accent-3**, which has the corresponding hexcode of #2979ff. The sites coloring is a softer tone and is designed to be simple, as reading books should be a relaxing task. 


### Images 
- The images used come from pixabay and pexels, and links to the images are used to connect them to their corresponding place on the site. They are chosen with the book genres in mind, so Game of Thrones and Harry Potter for fantasy, and images of dystopian cities for Sci-Fi.


## **Site Features**

Site features on this site are: a navbar, contact form, dropdown menus, a signup form and a login form, and edit reviews form.  

### **NavBar**

- Is used to offer a way of navigating the site. 

- Is a global element, as it appears on all pages.

- Uses if statements to hide certain pages from users that aren't logged in. For example the add review page is hidden from uses that aren't logged into the site. 

- Contains hidden statements that can only be accessed by clicking on certain buttons, for exmaple the edit button on a review takes you to the edit_review page. 

### **Forms**

- There are several forms on this site: A login form, a signup form, a contact form, a add review form, and a edit review form. 

  - The Login Form:

     - Appears on the login page.

     - Contains fields called: Username and Password.

     - Has a submit button to submit the data to the database.

     - A flash message appears welcoming the user if they login successfully.

     - A flash message appears if the login is unsuccessful, by letting the user know either their username or password was incorrect.

     - Icons are used to add a bit of decoration, and come from fontawesome.

     - All fields are required.


  - The Sign Up Form:

     - Appears on the signup page.

     - Contains fields: username, password, and date of birth.
 
     - Has a calender for which user can click to verify their date of birth. 

     - Has a sign up button that submits their data to the database.

     - A flash message appears letting them know the have signed up successfully.

     - All fields are required.

     - Icons are used to add a bit of decoration, and come from fontawesome.


  - Contact Form:

     - Appears on the contact page.

     - Users can submit feedback to improve the site, or ask questions on the site.

     - Users dont have to have an account or login to use it.
 
     - Contains fields asking for an email and their feedback/question so they can be contacted directly.

     - Offers a means of direct commnication between the siteowner and users.

     - All fields are required.

     - Icons are used to add a bit of decoration, and come from fontawesome.


  - Edit Reviews Form

     - Appears on Edit Review Page.

     - Allows users to edit their reviews.

     - Users can only edit their own reviews, not others.

     - Contains a drop down menu from which users can change the genre if needed.

     - Contains fields including: genre, name of book, book author, book description.

     - Contains an update button.

     - All fields are required.
 
### Dropdown Menus

- Appear on homepage, reviews and add a review pages.

- Offer a bit of interactivity with the site.

- Contain information stored on the database.

- Icons come from Fontawesome.


## **Features To Be Added**

This project has some features I would like to add at a later date. 

- 1: The ability for users to display their social media pages on their profile. This was attempted but due to time constraints couldn't be done in time. If statements would be used to check if they had any social media, and a flash message to be displayed if they didn't have any, prompting them to add some. 

- 2: Pagination: Pagination was originally going to be used to keep the users reviews displayed in an orderly fashion, however after much research, I couldn't find anything on Pagination for PyMongo, and MongoDB, it was all either using SQL Lite and SQL Alchemy, or MongoEngine instead of PyMongo. 

- 3: Profile picture: Currently a carousel from Materialize CSS is used to display images on the site and they can't chosen by the user, at some pont I'd like to be able to add the option for the user to display their own profile picture on the site instead of relying on the sites images.


## **TESTING**

### HTML Validation
   - The code was validated using NU HTML Validator and displayed some errors linked to the flask for loops, and the scripts needed for Matertialize CSS, and CSS classes. 

   <details><summary>HTML Validation</summary>
  <img src="static/images/html-validation.png">
  </details>
  

### CSS Validation
  - The code was tested using The W3C Jigsaw CSS Validation Service and encountered no errors:

  <details><summary>CSS Validation</summary>
  <img src="static/images/css-validation.png">
  </details>


### Python Validation
- The code was validated using PEP8 online check, and had several errors to do with whitespace, however when i have debugged these, I have encountered more errors. For example in the PEP8 validator it asks for a new line at the end of file, when I add one in, I get an error saying trailing whitespace.

  <details><summary>Python Validation</summary>
  <img src="static/images/python-validation.png">
  </details>


### Browser Compatibility

The website has been viewed on the following browsers:
 - Google Chrome
  <details><summary>Home Page View on Chrome Browser</summary>
    <img src="static/images/chrome.png">
  </details>

 - Mozilla Firefox

 <details><summary>Home Page View on Firefox Browser</summary>
    <img src="static/images/acer-aspire5.png">
  </details>

 - Safari
  
  <details><summary>Home Page View on Safari</summary>
    <img src="static/images/ipad.PNG">
  </details>

 - Microsoft Edge

 <details><summary>Home Page View on Microsft Edge browser</summary>
    <img src="static/images/edge.png">
  </details>

### Devices tested on

The site has been tested on the following devices:

 - iPhone SE 2020
  <details><summary>Homepage View on iPhone SE 2020</summary>
    <img src="static/images/iphone.PNG">
  </details>

  <details><summary>Menu View on iPhone SE 2020</summary>
    <img src="static/images/iphone2.PNG">
  </details>

 - iPad 8th Gen
    <details><summary>Home Page View on iPad 8th gen</summary>
      <img src="static/images/ipad.PNG">
    </details>
 - Acer Aspire 5
    <details><summary>CSS Validation</summary>
      <img src="static/images/acer-aspire5.png">
    </details>

 - iPad 7th Gen
    <details><summary>Home Page View on iPad 7th gen</summary>
      <img src="static/images/ipad.PNG">
    </details>

  - NB I have used the same photo for the iPad7th Gen as the iPad 8th gen, as they looked the same, and I havn't been able to get a screen grab of the site on that device.


## Deployment

- This site was deployed using Heroku using the following steps:

  1. Create a proc.file in your files, and connect to the app.py file.
  
  2. Create a requirements.txt file.

  3. Create an account on heroku.com

  4. Create a new application and give it a name. NOTE: This name must be new, and one not already in use.

  5. In the application dashboard, go to the deploy section and connect your application to your chosen GitHub repo, by selecting your repo's name.

  6. Select the branch to enable automatic deploys, (as was done with this project). Alternatively you can set it to deploy manually.

  7. Set key/value pairs for the following keys:IP, MONGO_DBNAME, MONGO_URI, PORT, SECRET_KEY

  8. Return to your dashboard and click deploy.

  9. Once dployed, click open app.


## Credits

### Icons
All icons can be found here: https://fontawesome.com/

### Imagery

All images come from pixabay and pexels: https://pixabay.com/
                                         https://www.pexels.com/
All links to specific images are as follows:

 - Home page slider images in order:
   - Fantasy Image: https://images.pexels.com/photos/3359734/pexels-photo-3359734.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260

   - Sci-Fi image: https://images.pexels.com/photos/7709020/pexels-photo-7709020.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260
   - Crime Image: https://images.pexels.com/photos/750241/pexels-photo-750241.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260
   - Thriller Image: https://images.pexels.com/photos/143580/pexels-photo-143580.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260
   - Action Image: https://cdn.pixabay.com/photo/2016/03/09/09/18/biking-1245722_1280.jpg
   - War Image: https://cdn.pixabay.com/photo/2014/10/02/06/34/war-469503_1280.jpg
   - Non-Fiction Image: https://cdn.pixabay.com/photo/2018/08/15/13/10/galaxy-3608029_1280.jpg
   - Horror Image: https://cdn.pixabay.com/photo/2017/10/13/14/15/fantasy-2847724_1280.jpg

  - Reviews Page:
    - https://cdn.pixabay.com/photo/2015/09/05/07/28/writing-923882_1280.jpg
  
  - Contact Us Page:
    - https://cdn.pixabay.com/photo/2017/02/07/00/44/feedback-2044700_1280.jpg
  
  - Profile Page Carousel (in order of appearance)
    - Carousel 1: https://cdn.pixabay.com/photo/2016/10/07/22/15/game-of-thrones-1722710_1280.png
    - Carousel 2: https://cdn.pixabay.com/photo/2020/11/13/16/51/white-walker-5739181_1280.jpg
    - Carousel 3: https://cdn.pixabay.com/photo/2019/05/05/15/05/game-of-thrones-4180794_1280.jpg
    - Carousel 4: https://cdn.pixabay.com/photo/2014/08/14/16/32/harry-potter-418108_1280.jpg
    - Carousel 5: https://cdn.pixabay.com/photo/2020/03/31/13/29/ufo-4987627_1280.jpg

  
### CSS Framework

Materialize CSS provided the Jquery and some CSS for this site: https://materializecss.com/ It also helped with making the site mobile responsive.


### JQUery Framework

Materialize CSS also provided the JQuery for this site, for the dropdown menus on the homepage and add a review page, the carousel on the profile page, and slider on the homepage. 


## Acknowledgements 

- My mentor Tim Nelson for his feedback and support.

- My family and friends for testing this site on their devices, and for their support with this project and course.
