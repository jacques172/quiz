 # HarvardX CS50W: Web Programming with Python and JavaScript
# Requirements
The final project is your opportunity to design and implement a dynamic website of your own. So long as your final project draws upon this course’s lessons, the nature of your website will be entirely up to you, albeit subject to the staff’s approval.
In this project, you are asked to build a web application of your own. The nature of the application is up to you, subject to a few requirements:
 - Your web application must utilize at least two of Python, JavaScript, and SQL.
 - Your web application must be mobile-responsive.
 - In README.md, include a short writeup describing your project, what’s contained    in each file you created or modified, and (optionally) any other additional information the staff should know about your project.
 If you’ve added any Python packages that need to be installed in order to run your web application, be sure to add them to requirements.txt!

# Overview

In this project Users will be able to take differents type of quizes, get the results after taking these quizes and get feedback as well on what they did correctly and incorrecty. If the time finishes before the user submitted his reponse, the system will count only the option selected by user befre the end
The project was built using Django as a backend framework and JavaScript as a frontend programming language. All generated information are saved in database (SQLite by default).

All webpages of the project are mobile-responsive.
Justification
I consider that this project meets all the expectations raised in the assignment of the CS50W final project, as it is a web platform that implements most of the concepts and techniques taught in the course.

The whole application is based on the Django framework, which allowed  database models, http requests, static files and the page rendering.

The web application is mobile responsive. I have included bootstrap library to make my front end mobile responsive.



## Installation
- Install project dependencies by running pip install -r requirements.txt.Dependencies include Django
- Make and apply migrations by running python manage.py makemigrations and python manage.py migrate.
- Create superuser with python manage.py createsuperuser. This step is optional.
![Screenshot 2022-11-17 174122](https://user-images.githubusercontent.com/96381612/202492617-254a0d58-52d3-4605-bab6-96b3dbde88e9.png)
********************************************************************************************************************************************
![Screenshot 2022-11-17 174144](https://user-images.githubusercontent.com/96381612/202492662-c1d6d9c7-5104-434f-9429-2da56fe45b1f.png)
********************************************************************************************************************************************
![Screenshot 2022-11-17 174208](https://user-images.githubusercontent.com/96381612/202492701-43dd65a8-3a5e-4e17-b50d-0daebf3c90f7.png)
********************************************************************************************************************************************
![Screenshot 2022-11-17 175207](https://user-images.githubusercontent.com/96381612/202492749-f90f01d3-6397-483f-932e-b51a4224cab7.png)
********************************************************************************************************************************************
## Files and directories
- `questions` - application directory that handles the questions of the quiz
 - apps.py files: - This file deals with the application configuration of the apps. The default configuration is sufficient enough in most of the cases.
  - `models.py`: contains 2 models: 
    - the model Questions represents the question to be answered 
    - the model Answer represents the answers suggestions to be picked
- `quiz_proj` (project directory)
            - Manage.py file:
            This file is used as a command-line utility and for deploying, debugging, or running the web application.This file contains code for runserver, makemigrations or migrations, etc. that we use in the shell. (Not changing anything here)
            - init.py files:
            This file is empty and remains that way. they are present only to tell that this particular directory is a package. (No changes to this file either)
            - settings folder:
            This file is present for adding all thr applications and the middleware application present. This also has informations about templates and databases. This is present in the main file of the Django web application.
            - urls.py files:
            This file handles all the URLs of our Django web application. This file contains the lists of all the endpoints that we will have for our web application. Also, this files is like a link to the views in the app with the host web URL.
            - admin.py files:
            Similar to the name of the file, this file is used for registering the models into the django administration. The models that are present have a superuser/admin who can control the information that is being stored. (they are pre-built)
            - wsgi folder:
            This file mainly concerns with the WSGI server and is used for deploying the web application on to the servers similar to apache, etc. (No changes to this file as well)
            - test.py files:
            This file containts the code that contains different test cases for the application. It is used to test the working of the application. (did not implement tests in this web application)

- `quizes`:  - application directory that enable to create quizes
   - `static/quizes` contains static contents:
       - main.js: script that run in the `main.html` 
       - quiz.js: script that run in the `quiz.html`
   - `templates/quizes`: conatains the applications templates:
       - main.html: template the show the quizes' characterisques(name, difficulty, minutes, time, score to pass)
       - quiz.html: template that shows teh quiz form  
  - `models.py`: contains 1 models that handles the creation of a quiz with the name, number of question,time and difficulty of the quiz.
  - `views.py`: contains 3 views: 
     - the QuizListView  display a particular quiz,
     - the quiz_data_view which display questions and answers related to the quiz,
     - the save_quiz_view which enables the submittion of the user' answers and his score
- `results`: application directory that enable to get the quiz results of the user
   - `models.py`: contains the Result model which register each user with his quiz score 
- `static`: which contains `styles.css`               
- `templates`: contains the base.html
   - `base.html`: base template. All other tempalates extend it.

                      
## Documentations:
- https://docs.djangoproject.com/en/4.1/intro/tutorial01/

       
