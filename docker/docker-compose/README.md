## Demo app - Developing with Docker

This demo app shows a simple user profile app set up using 
- index.html with pure js and css styles
- nodejs backend with express module
- mongodb for data storage

All components are docker-based

### With Docker Compose

#### To start the application

Step 1: start mongodb and mongo-express

    docker-compose -f docker-compose.yaml up

<img src="images\docker-compose.png">

_You can access the mongo-express under localhost:8080 from your browser_
    
Step 2: in mongo-express UI - create a new database "user-account"

<img src="images\mongo-express-ui.png">

Step 3: in mongo-express UI - create a new collection "users" in the database "user-account"       

<img src="images\mongo-express-ui-2.png">

Step 4: start node server 

    cd app
    npm install
    node server.js

<img src="images\npm-install.png">

    
Step 5: access the nodejs application from browser 

    http://localhost:3000


#### To build a docker image from the application

    docker build -t my-app:1.0 .       
    
The dot "." at the end of the command denotes location of the Dockerfile.

<img src="images\build-app.png">
<img src="images\verify-app.png">

<img src="">
<img src="">