1. git remote add (remote repo)
2. git fetch
3. git pull origin main (remote branch)

# MongoDB-Essential
## Start MongoDB
```console
mongodb --dbpath mongod_only
```
## Open MongoDB shell
```console
mongosh
```
### Commands
***Sow default databases***
```console
show databases
```
***Sore inquiry data***
```console
db.test.insertOne({"Hello": "World"})
```
