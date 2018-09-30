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
* Create a Heroku app, click deploy
* Scroll down to section "Deploy Using Heroku Git"
[Image for Heroku Git steps](https://github.com/pattyjula/hrku-garbanzo/blob/master/Capture.PNG)
* Follow steps within Bash to deploy

https://boiling-beach-89163.herokuapp.com/


