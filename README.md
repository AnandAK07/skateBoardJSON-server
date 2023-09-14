# JSON_Server_Deployment
1.npm init -y :->install package.json

2.npm i json-server cors json-serve :-> install the dependency (package.json is missing some dependency)

3.In package.json ->scripts->write in 1st line "start":"node index.js",

4.create a file index.js & write :->
const jsonServer = require("json-server"); // importing json-server library
const server = jsonServer.create();
const router = jsonServer.router("db.json");
const middlewares = jsonServer.defaults();
const port = process.env.PORT || 8080; //  chose port from here like 8080, 3001

server.use(middlewares);
server.use(router);

server.listen(port);

5.create a file .gitignore & write 
node_modules

6.create a file db.json
  i.add your product array between {} link { "products":[]}