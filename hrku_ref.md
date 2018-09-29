## create conda virtual env
`conda create -n blly_bio_env python=3.6`

## activate the environment you just created
`source activate blly_bio_env`

## Install dependencies
`pip install gunicorn`
`pip install psycopg2`
`pip install flask`
`pip install flask-sqlalchemy`
`pip install pandas`

## Initialize the database
`python initdb.py`

## Run the app
`FLASK_APP=bellybutton/app.py flask run`

## Procfile
`touch Procfile`

## Open Procfile in VS Code or vim? and add the line
`web: gunicorn bellybutton.app:app`

## Finally
Create a Heroku app, click deploy, and scroll
down to section "Deploy Using Heroku Git"
[Link to Heroku Git steps](https://github.com/pattyjula/hrku-garbanzo/blob/master/Capture.PNG)
follow steps within Bash to deploy

https://boiling-beach-89163.herokuapp.com/


