
# Rest APIs


### Representational State Transfer

Rest API is an architectural style for providing standard between computer systems making it easier to communicate to each others.

Rest system are separated and stateless to the client.

### Separation of the Client and Server

The client and server are completely modular each part has its own code and can be changed anytime without affecting the operation of the client.

### Statelesness

The server doesn't need to know the status of the client or vice versa to be able to operate. Making the system unpredictable and very reliable.

# Comunication between Client and Server


## Making Requests

Rest requires that a Client make a request to a server in order to retrieve or modify data on the server a request generally consist of:

- An __HTTP verb__, describes what kind of operation to perform
- A __Header__, which allows the client to pass along information about the request
- A __Path__ to the resource
- An __optional message__ body with the data provided.

## HTTP verbs

### Get
Retrieve specific resource or a collection of resources.
It's used to get information from the database

### Put
Update a specific resource with the id.
It's used to update information in the database

### Post

Create a resource.
It's used create information in the database.

### Delete
Delete a specific resource with the id.
It's used to delete information from the database

## Paths

Request should contain a path to a resource that the operation should be performed on.

Conventionally, the first part of the path should be the plural form of the resource, to improve readability

Example:

``` Link
boutique.com/users/223/orders/2 
```

## Response codes 

Response codes from the server contain status codes to alert the client to inform about success of the operations.

| _Status_ | _Response_ |
| ---- | ---- |
| *220* (OK) | Successful Response |
| *201* (Created) | Item being created |
| *204* (No Content) | Successful request but nothing returning in the response body |
| *400* (Bad Request) | Request cannot be processed |
| *403* (Forbidden) | Client doesn't have the persmission to acces  |
| *404* (Not Found) | The resource cannot be found |
| *500* (Internal Error) | An unexpected error in the server |


## HTTP status Codes

Each HTTP verb has its own status code.

| _HTTP verb_ |   _Code_ |
| ---- | ---- |
| _GET_ | *200* (OK) |
| _POST_ | *201* (Created) |
| _PUT_ | *200* (OK) |
| _DELETE_ | *204* (No Content) |


