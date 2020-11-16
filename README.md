# Building a REST API with NodeJS

REST means Representational State Transfer. This basically means transferring data around.

Server --> Client(Browser)

Browser sends a request.
Server serves the response.

**Exchanging Data is the core of RESTful API**

RESTful APIs are *Stateless Backends*

Client sends a AJAX (or HTTP or XML) Request and we receive a (JSON or XML or URLEncoded or FormData, basically not HTML) Response. 

**Essentially, the only way we can connect a mobile app or single page applications to Backend**

## What makes an API a RESTful API?

+ Client-Server Architecture
+ Stateless - No Client-Context (e.g. Session) is stored on the Server
+ Cacheability
+ Layered System
+ Uniform Interface
+ Code on Demand (optional)

## Practical

+ Building our API
+ `/products` Route : GET, POST (p)
+ `/products/{id}` Route : GET, PATCH (p), DELETE (p)
+ `/orders` Route : GET (p), POST (p)
+ `/orders/{id}` Route : GET (p), DELETE (p)

> (p) means Protected Route

## Important Topics

+ Handling Errors
+ Body-Parser
+ CORS
+ Morgan
+ MongoDB and Mongoose
+ Mongoose Validation
+ Authentication
+ Bcrypt
+ JSON Web Token


### CORS

Cross Origin Resource Sharing. If both the client and the server are on the same server (e.g. `localhost:3000`). In case of a REST API Client and Server are on different servers, so CORS comes in.

### Authentication

Client sends Auth Data (Email and Password) to Server. Server sends Session(?) in a normal Node App but in RESTful we don't have sessions (**Stateless**), Server sends a *Token*. This token can be attached to future requests. Client stores token in Storage and this is sent to authorize subsequent requests from Client.

> Token = JSON Data + Signature (Can be verifed) --> JSON Web Token (JWT)