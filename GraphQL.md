# Managing GraphQL servers with AWS Fargate & Prisma
**Nicolas Burk** from Prisma

## What is GraphQL
 Strongly typed schema for your API
 Query exactly what you need
 Smooth and fancy
 Not bound to a data source

## Stricture
    Schema Definition Language (SDL)
    Defines API
    Root Types:
        Query
```
//Schema:
type Query {
    hello: String!
}
//Query:
query {
    hello
}
//Response
response {
    "hello": "Hi there!"
}
```
        Mutation
```
type Mutatuion{
    createUser(name: String!): User!
    updateUser(id: ID!, anme: String!): User
    deleteUser(id: ID!): User
}
```
        Subscription

## Behaviour
    Resolver functions
        implementation of the api
        one resolver function per field in SDL schema
        query execution


## Setup
    Engine
    Network


## Links

[How To GraphQL](https://www.howtographql.com/)
[graphql-yoga (npm)](https://www.npmjs.com/package/graphql-yoga)