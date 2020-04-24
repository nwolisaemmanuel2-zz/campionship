champion.gg
========

WEBSITE: http://champion.gg
A MEAN project (with a dash of Angular).
In order to get a local version of champion.gg running you need to have MongoDB, Node and NPM installed. (Ensure MongoDB is running when trying to run champion.gg)
In order to get a working version set up you will need to clone the repo, install the dependencies, builds the database and then start the server from the command line. 

The commands to enter are listed below.

# To Get setting up

Clone champion.gg:
```sh
git clone https://github.com/nwolisaemmanuel2/championship.git
```

Install dependencies from project directory: 
```sh
npm install
```

Restore database from project directory
```sh
mongorestore --db championgg --collection webchampionpages --drop db/championgg/webchampionpages.bson
mongorestore --db championgg --collection webchampionroles --drop db/championgg/webchampionroles.bson
mongorestore --db championgg --collection webmatchuppages --drop db/championgg/webmatchuppages.bson
mongorestore --db championgg --collection weboverallroledatas --drop db/championgg/weboverallroledatas.bson
mongorestore --db championgg --collection weboverallstats --drop db/championgg/weboverallstats.bson
mongorestore --db championgg --collection webhomepagesummaries --drop db/championgg/webhomepagesummaries.bson
mongorestore --db championgg --collection webstatisticspages --drop db/championgg/webstatisticspages.bson
```

Start Champion.gg
```sh
npm start
#if you have another web server running on port 80 you can set the port as such
PORT=8888 npm start
```
You can now access champion.gg on http://localhost/ or if you set a port number http://localhost:8888/

# Development 

In order to work on champion.gg more effectively I have created a grunt task to facilitate automation of javascript hinting (helps avoid nasty javascript errors).
```sh
grunt watch
```

To get asset ready for production:
```sh
grunt production
```
