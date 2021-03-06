This boiler plate project is meant to be used to quickly deploy a parse server to heroku. This boiler plate includes the parse-server dashboard. To use: download this repo and deploy to heroku. The steps to deploy to heroku are outlined below.

Prerequisites:

1. you have a heroku account setup
2. you have a mongo database setup that is accessible through HTTP (I recommend using mLAB for their free sandbox db)
3. you have node and npm setup on your computer

##download heroku cli:

https://devcenter.heroku.com/articles/heroku-cli

##create the heroku app

1. login to the heroku dashboard
2. click new dropdown and select create new app
3. set an app name
4. click create app

##open up a terminal
```
$ cd my-project/
$ git init
$ heroku git:remote -a [appName]
```

##deploying application

1. add the changes: 'git add -u'
2. commit the changes: 'git commit -m "[message]"'
3. push to heroku repo: 'git push heroku master'


##setup the environmental variables:

| KEY    |  VALUE     |
| :------------- | :------------- |
| APP_ID       | <string> any id       |
| DATABASE_URI       | String used to connect using a driver via the standard MongoDB URI       |
| MASTER_KEY       | <string> any string -- keep this secret       |
| SERVER_URL       | <string> "https://[yourAppName].herokuapp.com/parse" -- replace the [] with your app name       |


##Check if deployment was successful:

go to dashboard: https://[yourAppName].herokuapp.com/dashboard/
user credentials should be specified in the index.js file
