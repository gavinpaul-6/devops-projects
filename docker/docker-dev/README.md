# Developing with Docker


## **Project Overview**
This project provides a high level overview of how to use 
---

## **Technologies**
- **Docker Desktop for Windows**
- **Node.js**
- **MongoDB**
- **MongoExpress**

---

## **Features**
- Create Dockerfile for Nodejs application and build Docker image
- Run Nodejs application in Docker container and connect to
- MongoDB database container locally.
- Also run MongoExpress container as a UI of the MongoDB
database.

---

All components are docker-based

### With Docker

#### To start the application

Step 1: Create docker network

    docker network create mongo-network 

Step 2: start mongodb 

    docker run -d -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo    

<img src="images\1-docker_run.png">

Step 3: start mongo-express
    
    docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net mongo-network --name mongo-express -e ME_CONFIG_MONGODB_SERVER=mongodb mongo-express   

_NOTE: creating docker-network in optional. You can start both containers in a default network. In this case, just emit `--net` flag in `docker run` command_

<img src="images\2-mongo-express.png">

Step 4: open mongo-express from browser

    http://localhost:8081


<img src="images\4-mongo-ui.png">

Step 5: create `user-account` _db_ and `users` _collection_ in mongo-express

<img src="images\5-mongo-ui_2.png">


Step 6: Start your nodejs application locally - go to `app` directory of project 

    cd app
    npm install 
    node server.js
    
<img src="images\6-start-node_app.png">

Step 7: Access you nodejs application UI from browser

    http://localhost:3000

<img src="images\7-node_ui.png">
