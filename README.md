# Using Mongo

## Starting MongoDB service

`brew services run mongodb-community`

_we can use start instead of run if we want the service start when we login on macbook_

## Checking if MongoDB is running

`brew services list`


## Stopping mongo service

`brew services stop mongodb-community`

# Shell Mongo

## Access to the mongo Shell

`mongo`

### Connect to Mongo With authentification

`mongo -u user -p password`

_(only if the user is in the Admin database)_

### Quit the shell

`exit`

_( For MacOS Catalina Only )_
## Path to

### Databases

`/System/Volumes/Data/data/db`

### Configuration files

`/usr/local/etc/mongod.conf`

#### Log directory

`/usr/local/var/log/mongodb`

### Data directory

`/usr/local/var/mongodb`


# Manipulate Database with Mongo

## Show Databases

`show dbs`

## Show the current database

`db`

## Use a Database

`use film`

## Show Statics of the Database

`db.stats()`


## Show collections

`show marvel`

---



## Add data in a collection

`db.film.insert({title: "SpiderMan"})`

_(if databasename doesn't exist, mongo will create the db)_

## Import collections

`mongoimport --db films --collection dccomics --drop -u adaane --authenticationDatabase admin --file /path/to/collection/dc-comics.json`

_'drop' option delete the collection if already exist_

## Show a collection

`db.marvel.find()`

## Format the JSON

`db.marvel.find().pretty()`
# cheat_sheet_Mongo
