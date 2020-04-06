### Questions

1. What is responsible for defining the routes of the `games` resource?

The file create_router.js holds all the code for handeling the routes

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
 - server handles the seed, routes
 - The client side handles how the information is viewed and the storign the information in an array to display the games added


3. What are the the responsibilities of server.js?

 - The file defines all the middleware we require
 - it sets the connection to the mongo database
 - sets up the server to use port 3000

4. What are the responsibilities of the `gamesRouter`?

The gamesRouter pulls the data from mongo DB, posts new data to the db and also deletes from the datbase.

5. What process does the the client (front-end) use to communicate with the server?

They use the form on the web page by entering the details of the game and clicking on save

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs

the second parameter is an init object and in this case allowes post information to the database

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

The front end consumes the following routes
 - router.get('/')
 - router.post('/')
 - router.delete('/:id')

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

It basically allows javascript's promise based systme to talk to mongo's callback based system

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

The ObjectId is the unique identifier the mongo uses for each document like a serial id in SQL. we can use this to select and manipulate secific documents easily.