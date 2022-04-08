# api-weather
API created in Flask Python using annother api to get the weather about any city

## How deploy this app in heroku
mkdir myproject
cd myproject
py -3 -m venv venv

////// Enviroment
venv\Scripts\activate

//////// Instalar flask
pip install Flask

////////  Setear la variable de entorno 
set FLASK_APP=app
//////// Correr la app
flask run

///// Instalar gunicorn
pip install gunicorn

/////// Crear el Procfile
web: gunicorn app:app

///// Requerimientos
pip freeze > requirements.txt

git init

git add .
git commit -am "first commit"
heroku login
heroku create xxxxxx
git push heroku master
