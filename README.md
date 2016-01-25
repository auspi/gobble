[![Stories in Ready](https://badge.waffle.io/auspi/gobble.png?label=ready&title=Ready)](https://waffle.io/auspi/gobble)
# gobble
Gobbly Wobble Boo

Steps to be followed during first deploy -
    change `DATABASE_URL` in .env file to DATABASE_URL=postgres:///{heroku_app_name}
    Go to heroku web
    create new app with app name {heroku_app_name}
    Go to deploy tab
    enable git hub integration
    select your github repo and branch
    click connect
    enable auto deploy
    click deploy
    go to settings
    click Reveal Config Vars
    add DEBUG with value false
    add host with value {heroku_app_name}.herokuapp.com


After this when ever you push your code to this repo, auto deploy will be initiated.

