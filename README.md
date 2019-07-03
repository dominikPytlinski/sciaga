# sciaga
### Technology
### Express, Mongoose, GraphQL, Nodemon
## Basic setup
#### For basic setap run below
### npm init
#### Above initialize npm project and create package.json

## Nodemon
#### For instal type below
### npm install nodemon --save-dev
#### Above installed nodemone and save as a developer dependencies
#### Usage
#### edit package.jason
#### "scripts": {
####  &emsp;"test": "echo \"Error: no test specified\" && exit 1",
####  &emsp;"start": "nodemon app.js" // add this line than in terminal you can type npm start to run
#### }

## Express
#### For install express type below (--save flag for saving in the dependencies)
### npm install express --save
#### Usage
#### const express = require('express'); // import express
#### const app = express(); // new express instance
#### const PORT = 4000 // define port
#### app.listen(PORT, () => {
#### &emsp;console.log('message for listening');
#### }) // add listening

## GraphQL
#### For install required packages type below
### npm install graphql express-graphql --save
#### Usage
#### const graphqlHTTP = require('express-graphql'); // import express-graphql
#### app.use('/graphql', graphqlHTTP({ //enpoint, middleware
#### &emsp;schema, //graphql schema
#### &emsp;graphiql: true // optiona, true if graphiql shpuld be awaillable
#### }))
### Schema
#### in schema file require graphql
#### const graphql = require('graphql');
#### const { GrqaphQLObjectType, GraphQLString, GraphQLIn, GraphQLID, GraohQLSchema } = graphql; // deconstruct graphql, require needed
#### Creating a type
#### const NameType = new GraphQLObjectType({
#### &emsp;name: 'Name',
#### &emsp;fields: () => ({
#### &emsp;&emsp;propName: { type: one of gql types ex GraphQLString }
#### &emsp;&emsp;propName: { // prop wchich is user created type, has resolver for getting the data
#### &emsp;&emsp;&emsp;type: ExistingType,
#### &emsp;&emsp;&emsp;resolve(parent, args) {
#### &emsp;&emsp;&emsp;&emsp;//code for get from db
#### &emsp;&emsp;&emsp;}
#### &emsp;&emsp;}
#### &emsp;})
#### });
#### Creating a query
#### const RootQuery = new GraphQLObjectType({
#### &emsp;name: 'RootQueryType',
#### &emsp;&emsp;fields: {
#### &emsp;&emsp;&emsp;name: {
#### &emsp;&emsp;&emsp;&emsp;type: TypeWchichYouWantToUse, // usuly custom type
#### &emsp;&emsp;&emsp;&emsp;args: { type: OneOfTheGraphQlTypes }, // if they are needed
#### &emsp;&emsp;&emsp;&emsp;resolve(parent, args){
#### &emsp;&emsp;&emsp;&emsp;&emsp;// code for getting form db
#### &emsp;&emsp;&emsp;&emsp;}
#### &emsp;&emsp;&emsp;},
#### &emsp;&emsp;&emsp;secondname: {
#### &emsp;&emsp;&emsp;&emsp;type: TypeWchichYouWantToUse, // usuly custom type
#### &emsp;&emsp;&emsp;&emsp;args: { type: OneOfTheGraphQlTypes }, // if they are needed
#### &emsp;&emsp;&emsp;&emsp;resolve(parent, args){
#### &emsp;&emsp;&emsp;&emsp;&emsp;// code for getting form db
#### &emsp;&emsp;&emsp;&emsp;}
#### &emsp;&emsp;&emsp;}
#### &emsp;&emsp;}
#### });
#### Exports
#### module.exports = new GraphQLSchema({ // export witch graphqlschema, params query and mutatnion
#### &emsp;query: RootQuery,
#### &emsp;mutation: RootMutation
#### });

## Mongoose
#### For install type below
### npm install mongoose --save
#### Usage
#### const mongoose = require('mongoose'); // import mongoose
#### mongoose.connect('connect_string_to_database', { useNewUrlParser: true }) // second parameter, option
#### &emsp;.then(
#### &emsp;&emsp; // code when connected example:
#### &emsp;&emsp; app.listen(PORT, () => {
#### &emsp;&emsp;&emsp;console.log('message for listening');
#### })
#### .catch(err => console.log(err)); // return promise
#### Creating a scheam
#### in schema file type:
#### const mongoose = require('mongoose');
#### cosnt Schema = mongoose.Schema;
#### 
#### const nameSchema = new Schema({
#### &emsp;name: String // properity name and type
#### });
