[![Stories in Ready](https://badge.waffle.io/auspi/gobble.png?label=ready&title=Ready)](https://waffle.io/auspi/gobble)
# gobble
Gobbly Wobble Boo

Steps to be followed during first deploy on heroku prod:

    * Go to heroku web
    * create new app with app name {heroku_app_name}
    * Go to deploy tab
    * enable git hub integration
    * select your github repo and branch
    * click connect
    * enable auto deploy
    * click deploy
    * go to settings
    * click Reveal Config Vars
    * add DEBUG with value false
    * add host with value {heroku_app_name}.herokuapp.com
    * This will finalize your deployment process
    * You will need to setup create your first superuser:

        * for this you will need heroku setup on you machine
        * please follow getting started with heroku to download heroku on your local system
        * then run `heroku run --app {heroku_app_name} python manage.py createsuperuser`


After this when ever you push your code to this repo, auto deploy will be initiated.

for local setup:

    * if you want to run heroku local:

        * delete `dev.py` if exist
        * update `.env` file with your heroku app name
        * run `heroku local`

    * if you want to use you local setup:

        * make sure that you have pstgress install and database created with settings from `settings/development.py`
        * rename development.py as dev.py
        * run `python manage.py collecstatic`
        * run `python manage.py migrate`
        * run `python manage.py runserver`


