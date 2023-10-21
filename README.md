# Create json server for your crud Application

## Create a folder for server

1. create package.json on folder - command `npm init -y`
2. install json-server - command `npm i json-server`
3. create `.gitignore` file in server folder and mention to be ignored ex:node_module
4. create a js file 
5. edit script of package.json file into index.js to run server - `"start": "node yourfile.js"`
6. create a json file (ex: db.json)


 ## Steps to generate json server
 
 ### `1. import json server library
const jsonServer = require('json-server')`

 ### `2. create our own server to run json file
const server = jsonServer.create()`

 ### `3. generate a middleware to use in json server
const middleware = jsonServer.defaults()`

 ### `4. set up route/path for db.json
const router = jsonServer.router("db.json")`

 ### `5. set up port for server
const port = 3000 || process.env.PORT`

 ### `6. use middleware and router to server
server.use(middleware)
server.use(router)`

 ### `7. server listen or run to request
server.listen(port,()=>{
    console.log("Server started at port no : "+port);
})`

