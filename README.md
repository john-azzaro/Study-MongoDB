# MongoDB Atlas Cloud Deployment Study

<br>

## What is the MongoDB Cloud Deployment Study?
MongoDB 

* [What is MongoDB Atlas?](#What-is-MongoDB-Atlas)

<br>

## What is MongoDB Atlas?
MongoDB Atlas is a fully managed cloud version of MongoDB, a popular NoSQL database for build small to enterprise level applications.  But although MongoDB is open-source, scalable, and features high availability as well as support for complex queries and fine concurrency control, MongoDB Atlas provides an easy alternative to installing, tuning for optimal performance and security a database on the cloud for your own project.

<br>

## What can you do with MongoDB Atlas?
With Atlas, you can create a MongoDB **cluster** on any major cloud provider (AWS, Google Cloud, Azure, etc.) and use that cluster within minutes with a browser-based interface.  Additionally, you can allocate cloud resources and have the database automatically set itself up with predefined rules and further monitor its performance.  

<br>

## How do you use MongoDB Atlas?

### STEP 1: Create a cluster
The first time you do this, you will automatically be prompted to create a new cluster, but if you are already passed this point and want to create a new cluster, just click on ``` Build a New Cluster```.

### STEP 2: Create a database User
This user will be used to log onto the database.  All you need to do is click on "Security" > "Database Access" > "+ ADD NEW USER".  Once you get a pop-up to add a new user, selct the "Atlas admin" privileges option.   Then, when you add the user, put in the name and password.

### STEP 3: Whitelist your IP Address
To do this, select the "Security" > "Network Access" > "+ ADD IP ADDRESS".  For the moment, you can whitelist all IP addresses by selecting "ALLOW ACCESS FROM ANYWHERE"

### STEP 4: Connect to your remote Atlas database
When you connect to the Atlas, you need to select "Connect with the Mongo Shell".  Then, you will need to specify whether or not you have the Mongo Shell installed on your local machine.  To do this, open your Gitbash (or command line) and run ``` mongo --version```.  If you have Mongo Shell installed, you will get a version number and you can select "I have the Mongo Shell installed" option.

Once thats done, run the connection string in command line, replacing "password" with the password you chose for your user.

```
mongo "mongodb://my-first-atlas-db-shard-00-00-11uld.mongodb.net:27017,my-first-atlas-db-shard-00-01-11uld.mongodb.net:27017,my-first-atlas-db-shard-00-02-11uld.mongodb.net:27017/test?replicaSet=my-first-atlas-db-shard-0" --ssl --authenticationDatabase admin --username my-first-user --password <PASSWORD>

```
This shoudl give you access to your mongoDB database the same as if you had accessed it locally.

<br>

## How do you import data to Atalas database?
To import data to your Atlas database, you need to use the ```mongoimport``` command.  To do this, under the cluster overview section, click the 3 dots next to conenct, metrics, collections. Then, click "command line tools".  Then, under "Data Import and Export Tools"

```
mongoimport --host my-first-atlas-db-shard-0/my-first-atlas-db-shard-00-00-11uld.mongodb.net:27017,my-first-atlas-db-shard-00-01-11uld.mongodb.net:27017,my-first-atlas-db-shard-00-02-11uld.mongodb.net:27017 --ssl --username my-first-user --password password123 --authenticationDatabase admin --db test --collection restaurants --type json --file ~/datasets/primer-dataset.json
```
