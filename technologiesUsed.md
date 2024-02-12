# Table of Contents

- [JavaScript](#javascript)

- [Technologies Used](./technologiesUsed.md)

  - [MongoDB](#mongodb)
  - [Express](#express)
  - [React](#react)
  - [NodeJS](#nodejs)

## JavaScript

## MongoDB

```javascript
// server/ index.js
import express from "express";
import mongoose from "mongoose";
import dotenv from "dotenv";

dotenv.config();

// MongoDB connection using mongoose


// Method: 01 
// Mongodb connection using mongoose and ecpress
mongoose
  .connect(process.env.MONGO_LOCAL)
  .then(() => {
    console.log("MongoDB is connected to the MongoDB Atlas!");
  })
  .catch((err) => {
    console.log(err);
  });

// Method: 02 
// Mongodb connection using mongoose and ecpress

mongoose
  .connect(process.env.MONGO_LOCAL || process.env.MONGO_ATLAS)
  .then(() => {
    const connectedTo = process.env.MONGO_LOCAL ? "MongoDB is connected to the local MongoDB instance!" : "MongoDB is connected to the MongoDB Atlas!";
    console.log(connectedTo);
  })
  .catch((err) => {
    console.log(err);
  });

// Method: 03
// Mongodb connection using mongoose and ecpress

const mongoURI = process.env.MONGO_LOCA || process.env.MONGO_ATLAS;
mongoose
  .connect(mongoURI)
  .then(() => {
    const connectedTo = mongoose.connection.client.s.url;
    console.log(`MongoDB is connected to the ${connectedTo}!`);
  })
  .catch((err) => {
    console.log(err);
  });

// Method: 04
// Mongodb connection using mongoose and ecpress

const mongoURI = process.env.MONGO_LOCA || process.env.MONGO_ATLAS;
mongoose
  .connect(mongoURI)
  .then(() => {
    const connectedTo =
      mongoURI === process.env.MONGO_LOCAL
        ? "MongoDB Localhost"
        : "MongoDB Atlas";
    console.log(`MongoDB is connected to the ${connectedTo}!`);
  })
  .catch((err) => {
    console.log(err);
  });


// create express app
const app = express();

// This is the server port number
const port = 3000;

// Here I make a get request on root or /
app.get("/", (req, res) => {
  res.send("Hello World!");
});

// Here app.listen use for run expressjs  server on any port. I mension the port above
app.listen(port, () => {
  console.log(`Server is Running on port ${port} !`);
});

## Express

## React

## NodeJS

_Previous: [File Structure](./README.md/#file-structure)_ | _Next: [Getting Started](./README.md/#getting-started)_
```
