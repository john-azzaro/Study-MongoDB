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

#### STEP 1: Create a cluster
The first time you do this, you will automatically be prompted to create a new cluster, but if you are already passed this point and want to create a new cluster, just click on ``` Build a New Cluster```.

#### STEP 2: Create a database User
This user will be used to log onto the database.  All you need to do is click on "Security" > "Database Access" > "+ ADD NEW USER".  Once you get a pop-up to add a new user, selct the "Atlas admin" privileges option.   Then, when you add the user, put in the name and password.

#### STEP 3: Whitelist your IP Address
To do this, select the "Security" > "Network Access" > "+ ADD IP ADDRESS".  For the moment, you can whitelist all IP addresses by selecting "ALLOW ACCESS FROM ANYWHERE"

### STEP 4: Connect to your remote Atlase database
