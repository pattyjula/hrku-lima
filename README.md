# Quick Summary
Create a Flask app and deploy to Heroku: [deployed site](https://boiling-beach-89163.herokuapp.com/)

# Slightly Longer Introduction

The contents of this repository allow developers to deploy the provided Flask app to Heroku. This repository does not represent the best or only way to deploy a Flask application on Heroku. It is recommend you clone the repository and follow the steps exactly as described. After that, it is recommended you take what you learned from this deployment and apply it to your own Flask application. Take note of the use of gunicorn and the importance of initializing your database.

## Virtual Environment
Create a virtual env within GitBash using conda.  
Note, the virtual environment in this example is `blly_bio_env` you can set another name for the virtual environment.  
`conda create -n blly_bio_env python=3.6`

## Activation
Activate the environment you just created.  
`source activate blly_bio_env`

* Your app name will display in parenthesis at this point within Bash.  

## Dependencies
Install your dependencies, this list will vary for other deployments.  
* `pip install gunicorn`
* `pip install psycopg2`
* `pip install flask`
* `pip install flask-sqlalchemy`
* `pip install pandas`

## Initialize the database
`python initdb.py`

* Very important, note the presence of an init Python file [here](https://github.com/pattyjula/hrku-lima/blob/master/belly-prj/bellybutton/)

## Run the app locally
`FLASK_APP=bellybutton/app.py flask run`

## Procfile
`touch Procfile`

## Open Procfile in VS Code or vim and add the line
`web: gunicorn bellybutton.app:app`

* Notice how there is no extension on the app files and how the Flask code sits within the folder "bellybutton".  

## Heroku
These steps will deploy your app to Heroku
* Log into Heroku, from Command Line on Windows with `heroku login`
* Log into Heroku website and create an app, click deploy
** Alternatively you can run command to create app
* Scroll down to section "Deploy Using Heroku Git"
[Image for Heroku Git steps](https://github.com/pattyjula/hrku-lima/blob/master/imgs/Capture.PNG)
* Follow steps within Bash to deploy

https://boiling-beach-89163.herokuapp.com/

## Acknowledgment
Thank you [Trilogy Education](https://www.trilogyed.com/) for the Plotly JS content.




