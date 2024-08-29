# Hexaskill

![GitHub Open Issues]
# skillnavigation Online School

_This is the first stage of intial development of the upskilling learning management system for hackthon._

## Overview
The project is an online learning management system that collects candidate details, processes batch split-ups, tracks learning progress, and generates reports.

- Administrators:
    - You control who uses the platform, by registering them, managing their batch and data, temporarily deactivating users or permanently deleting them and their data.
    - You get a bird's eye view of the entire business: what teachers are doing, what students are doing, what Hiring manager have to say
    - You manage lesson contents by uploading them to the platform

- Teachers:
    - Tasked with guiding students through the lessons
    - They mark students' attendance, compounded to ratify each student's participation.
    - They assess their submitted lesson projects
    - They grade students projects

- Hiring managers:
    - They register their Learner once approved by the admin. Done so that student information is accurate.
    - They see how well their Learner's attendance has been
    - They get to see how they perform in each chapter by scoring 9+ is hard and getting crm insights

- Students:
    - They have access to lessons
    - They are required to complete the lessons in the order they progress
    - Access to subsequent lessons is dependant on the performance on the current chapter/lesson


### Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Additional Details](#additional-details)
- [Application Details](#application-details)
    - [Newsletter](#newsletter)
    - [Multi-user Support](#multi-user-support)
- [Testing It Locally](#testing-it-locally)
- [Areas of Improvement](#areas-of-improvement)


## Features

- Multi-user support
- Batch allocation
- Newsletter subscription
- Basic user authentication
- Two-factor authentication
- 24/7 chatbot
- AI valuation engine
- Reporting
- Sending of emails from the app


## Technologies Used

- Flask micro-framework
- Python for programming
- Sprinkles of JavaScript for front-end design
- Twilio Verify API for two-factor authentication
- Twilio SendGrid for email support
- Gunicorn for live app deployment
- Phonenumbers package for beautiful phone numbers
- DatatableJS for interactive tables
- Pytest and pytest-cov for testing
- Psycopg2 for postgresql adaptability
- Postgresql database or fallback to SQLite database
- Flask-sqlalchemy ORM for database management
- Flask-migrate for database migrations
- Flask-moment for time formatting
- Hugging face transformers
- need to workon--


## Application Details

### Newsletter:

- A user interested in receiving periodic updates about skillnavigation can sign up for the newsletter service.
- Registration is limited to those who verify their email addresses only

- The application automatically sends pre-prepared emails to them at set intervals

- Admin can email an individual newsletter subscriber to enhance one-on-one communication (optional)


### Multi-user Support

>The application features a **superadmin**, who cannot be deleted. This superadmin is the source of all activities in the app. For example:
>
>- All teachers are added by the superadmin
>- Other admins, with limited powers, are also added by the superadmin
>
>To login as a superadmin, you can use this credentials:
>
>- Visit: **https://skillnavigation/login**
>- Username: **tastebolder**
>- Password: **skillnavigation123**

- Hiring manager Registration (anonymous user can register as a Hiring manager)
    - Done from the home page **https://skillnavigation/register**

- Student Registration (done ONLY by a registered Hiring manager - designed so to allow for their association)
    - Done from the logged-in Hiring manager's account **https://skillnavigation.onrender.com/register/student**
      
    - An email will be sent to the student to check their login details


- Teacher Registration content delivery(done only by a logged in admin - not necessarily the superadmin)
    - Done from the logged-in admin's account **https://skillnavigation.onrender.com/register/teacher**

    - An email will be sent to the teacher to check their login details
    
- Other admin registration (done only by a logged in admin - not necessarily the superadmin)
    - Done from the logged-in admin's account **https://skillnavigation.onrender.com/register/admin**
    
        - An email will be sent to the admin to check their login details
    
## Testing It Locally

- Clone this repo:

    ```python
    $ git clone git@github.com:aishwarya134/skillnavigation-online-school-using-flask.git
    ```
- Change directory into the cloned repo:

    ```python
    $ cd skillnavigation-online-school-using-flask
    ```
- Create and activate a virtual environment

    ```python
    # Using virtualenvwrapper
    $ mkvirtualenv venv

    # Normal way
    $ python3 -m venv venv
    $ source venv/bin/activate
    ```

- Install needed dependancies:

    ```python
    (venv)$ pip3 install -r requirements.txt
    ```

- Add and update environment variables in a `.env` file as seen in `.env-template`:

    ```python
    (venv)$ cp .env-template .env
    ```

- Start the flask server:

    ```python
    (venv)$ flask run
    ```

- Check the application in your favourite browser by pasting http://127.0.0.1:5000.


### "Dream we deliver"
