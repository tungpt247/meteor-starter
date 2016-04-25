#Getting started with Meteor
----------------------------
A Meteor boilerplate to start your Meteor next project

##Requirements

	Environment:
		Meteor version: 1.3.2.2
		Node version: v5.10.1
		Npm version: 3.8.7

	Database: Mongodb
		Use an external database with mLab service at https://mlab.com

	Free hosting: Heroku

##Installing
```npm install```

##Local development
```npm start```

```open http://localhost:3000```


#Deploying your app to Heroku
-----------------------------

##Setup Heroku repository
```heroku login```

```heroku create your-app-name```

##Setup external Mongodb for Heroku

####Use [mLab service](https://mlab.com)

	1. Setup your Account
	2. Create database: **your-database-name**

mLab will auto generated "your-database-name" database:
> 
> 	To connect using the mongo shell:
> 	mongo ds047468.mlab.com:47468/[your-database-name] -u [dbuser] -p [dbpassword]
> 
> 	To connect using a driver via the standard MongoDB URI:
> 	  mongodb://[dbuser[:[dbpassword]@[host:port]/[your-database-name]


####Set env and build pack:
```heroku buildpacks:set https://github.com/tungpt247/heroku-buildpack-meteor.git```

```heroku config:set MONGO_URL=mongodb://[username]:[password]@[host]:[port]/[dbname]```

```heroku config:set ROOT_URL=https://<your-app-name>.herokuapp.com/```

##Deploying:

```git remote add heroku your-github-repository-url```

```npm push heroku master```

##The result
open https://your-app-name.herokuapp.com/
