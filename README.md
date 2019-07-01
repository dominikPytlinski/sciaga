# sciaga
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
####  &nbsp;&nbsp;&nbsp;&nbsp;"test": "echo \"Error: no test specified\" && exit 1",
####  &nbsp;&nbsp;&nbsp;&nbsp;"start": "nodemon app.js" // add this line than in terminal you can type npm start to run
#### }

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
### Schema
#### in schema file require graphql
#### const graphql = require('graphql');
#### const { GrqaphQLObjectType, GraphQLString, GraphQLIn, GraphQLID, GraohQLSchema } = graphql; // deconstruct graphql, require needed
#### Creating a type
#### const NameType = new GraphQLObjectType({
#### &nbsp;&nbsp;&nbsp;&nbsp;name: 'Name',
#### &nbsp;&nbsp;&nbsp;&nbsp;fields: () => ({
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;propName: { type: one of gql types ex GraphQLString }
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;propName: { // prop wchich is user created type, has resolver for getting the data
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;type: ExistingType,
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;resolve(parent, age) {
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;//code for get from db
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
#### &nbsp;&nbsp;&nbsp;&nbsp;})
#### });
#### Creating a query
#### const RootQuery = new GraphQLObjectType({
#### &nbsp;&nbsp;&nbsp;&nbsp;name: 'RootQueryType',
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;fields: {
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;name: {
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;type: TypeWchichYouWantToUse, // usuly custom type
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;args: { type: OneOfTheGraphQlTypes }, // if they are needed
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;resolve(){
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;// code for getting form db
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;},
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;secondname: {
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;type: TypeWchichYouWantToUse, // usuly custom type
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;args: { type: OneOfTheGraphQlTypes }, // if they are needed
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;resolve(){
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;// code for getting form db
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
#### });
#### Exports
#### module.exports = new GraphQLSchema({ // export witch graphqlschema, params query and mutatnion
#### &nbsp;&nbsp;&nbsp;&nbsp;query: RootQuery,
#### &nbsp;&nbsp;&nbsp;&nbsp;mutation: RootMutation
#### });

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
