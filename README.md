1. git remote add (remote repo)
2. git fetch
3. git pull origin main (remote branch)

# MongoDB Essential
## Table of Contents
1. [Mongod Commands](#mongod-commands)
2. [Replica Set](#replica-set)
    i. [Connect to Instances](#connect-to-instances)

### Mongod Commands
***Start MongoDB***
```console
mongod --dbpath mongod_only
```
***Open MongoDB shell***
```console
mongosh
```
***Sow default databases***
```console
show databases
```
***Store inquiry data***
```console
db.test.insertOne({"Hello": "World"})
```
### Replica Set
*create directory*
```console
mkdir replica_set_cmdline
```
*Create keyfile*
```console
openssl rand -base64 755 > keyfile
```
*Restrict permissons*
```console
chmod 400 keyfile
```
*Create multiple folders*
```console
mkdir -p m{1,2,3}/db
```
*Start mongod processes*
```console
mongod --replSet myReplSet --dbpath ./m1/db --logpath ./m1/mongodb.log --port 27017 --keyFile ./keyfile

mongod --replSet myReplSet --dbpath ./m2/db --logpath ./m2/mongodb.log --port 27018 --keyFile ./keyfile

mongod --replSet myReplSet --dbpath ./m3/db --logpath ./m3/mongodb.log --port 27019 --keyFile ./keyfile
```
### Connect to Instances
*MongoDB shell*
```console
mongosh
```