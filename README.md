# sciaga
## Basic setup
#### For basic setap run below
### npm init
#### Above initialize npm project and create package.json

## Express
#### For install express type below (--save flag for saving in the dependencies)
### npm install express --save
#### Usage
#### const express = require('express'); // import express
#### const app = express(); // new express instance
#### const PORT = 4000 // define port
#### app.listen(PORT, () => {
#### &nbsp;&nbsp;&nbsp;&nbsp;console.log('message for listening');
#### }) // add listening

## GraphQL
#### For install required packages type below
### npm install graphql express-graphql --save
#### Usage
#### const graphqlHTTP = require('express-graphql'); // import express-graphql
#### app.use('/graphql', graphqlHTTP({ //enpoint, middleware
#### &nbsp;&nbsp;&nbsp;&nbsp;schema, //graphql schema
#### &nbsp;&nbsp;&nbsp;&nbsp;graphiql: true // optiona, true if graphiql shpuld be awaillable
#### }))

## Mongoose
#### For install type below
### npm install mongoose --save
#### Usage
#### const mongoose = require('mongoose'); // import mongoose
#### mongoose.connect('connect_string_to_database', { useNewUrlParser: true }) // second parameter, option
#### &nbsp;&nbsp;&nbsp;&nbsp;.then(
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; // code when connected example:
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; app.listen(PORT, () => {
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;console.log('message for listening');
#### })
#### .catch(err => console.log(err)); // return promise
