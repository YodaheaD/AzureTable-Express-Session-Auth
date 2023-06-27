# Express API for Azure tables.
#### By: Yodahea Daniel


##### 1) Project Description
##### 2) Project Goals
##### 3) Technologies Used

### 1) Project Description

This app is the backend part of the previous project 'Data Repository'. 

- The 'Data repository' is the UI that interacts with this API.
- The user can register and login using the UI forms. 
- If sending data, the API inserts the data into azure table
- If requesting data, the API gets the data from the Azure table and returns it to requester. 

##### 2) Project Goals

My goals for this project:
- Create an Express API using session/cookie data for authentication.
- Learn more about Session and Cookie data.

### 3) Technologies Used

###### Session Data
- HTTP is stateless; in order to associate a request to any other request, you need a way to store user data between HTTP requests. 
- Cookies and URL are both readable and on the client side, Not good.

- With Sessions, the client an ID and it makes all further requests using that ID, in this project the data is housed in 'Auth' Azure Table.
- Information associated with the client is stored on the server linked to this ID.

###### ExpressJS and Express-Session
- A nodejs web app framework, used to created API endpoints. 
- A express based middleware for interacting with session data. 

###### Typescript
- Language built on JS but with static data types. 

###### Azure Tables
- Azure Table storage stores large amounts of structured data. The service is a NoSQL datastore

###### 'TableLike' generic
-  A generic class with built-in functions that allow us to interact with tables in a Azure Storage. 

###### Express- Expeditious 
- A library created by [@evanshortiss](https://github.com/evanshortiss/express-expeditious) for caching responses of HTTP requests. 
- Works by generating a 'cache' key for requests, checking if that key exists in a data object for storage called the 'storage engine', then either responding with the cached data or making the request. 

###### Swagger-autogen
- A tool for auto generating SwaggerUI documents by [@davibaltar](https://github.com/davibaltar/swagger-autogen) . Used for my 'auth' route and can be found in the route '____:__/api-docs/'. Swagger config file under 'utils' folder can be generated by running "npm run swagger" (look at package json file).

### Versions List 

##### 1.0 <-> Original Release
- API performs Add, view, and delete function for 'users' in a Azure Table.  
- Table like generic class with functions for interacting with Azure Table. 
- Table: 'users' hold users information.
- Table: 'Auth' holds sensitive User auth. info.
- Basic cache route for testing cache data speed using 'express-expeditious'.
- Future Improvement: Move functions in 'tablelike' that are specific to certain tables to their respective files in 'db'.




