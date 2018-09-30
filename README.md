# hrku-lima
Create flask app and deploy to Heroku [site](https://boiling-beach-89163.herokuapp.com/)

# Introduction

The contents of this repository do not represent the best or only way to deploy a Flask application on Heroku. It is recommend you clone the repository and follow the steps exactly as described. After that, it is recommended you take what you learned from this deployment and apply it to your own Flask application. 

## create conda virtual env within GitBash
### Note, the virtual environment in this example is `blly_bio_env` you can set another name as you wish
`conda create -n blly_bio_env python=3.6`

## activate the environment you just created
`source activate blly_bio_env`

* Your app name will be in parenthesis at this point within Bash

## Install dependencies
* `pip install gunicorn`
* `pip install psycopg2`
* `pip install flask`
* `pip install flask-sqlalchemy`
* `pip install pandas`

## Initialize the database
`python initdb.py`

## Run the app
`FLASK_APP=bellybutton/app.py flask run`

## Procfile
`touch Procfile`

## Open Procfile in VS Code or vim? and add the line
`web: gunicorn bellybutton.app:app`

## Finally
* Log into Heroku, from Command Line on Windows with `heroku login`
* Log into Heroku website and create an app, click deploy
** Alternatively you can run command to create app
* Scroll down to section "Deploy Using Heroku Git"
[Image for Heroku Git steps](https://github.com/pattyjula/hrku-lima/blob/master/imgs/Capture.PNG)
* Follow steps within Bash to deploy

https://boiling-beach-89163.herokuapp.com/





