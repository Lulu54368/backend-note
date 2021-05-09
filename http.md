---
title: "HTTP"
tags: ""
---

# HTTP Basics
## Introduaction
### Features
- Connectionless: _When a request is sent, the client opens the connection;_ once a response is received, the client closes the connection. The client and server only maintain a connection during the response and request. Future responses are made on a new connection.
- Stateless: There is **no dependency** between successive requests.
- Not Sessionless: Utilizing headers and cookies, **sessions** can be created to allow each HTTP request to **share the same context**.
- Media Independent:** Any type of data** can be sent over HTTP as long as both the client and server know how to handle the data format. In our case, we'll use JSON.

### Elements -URLS

Universal Resource Identifiers 
```
http://www.example.com/tasks/term=homew
ork.
```


- Scheme: specifies the**protocol** used to access the resource, HTTP or HTTPS. 
  ```
  http
  ```

- Host: specifies the host that holds the resources.
  ```
  www.example.com.
  ```
- Path: specifies the specific resource being requested. 
  ```
  /tasks.
  ```
- Query: an optional component, the query string provides information the resource can use for some purpose such as a search parameter. 
  ```
  /term=homework.
  ```
## Requests

_HTTP requests are sent from the **client**to the **server** to initiate some operation. In addition to the URL, HTTP requests have other elements to specify the requested resource._

### Elements
#### Example
```
GET http://www.example.com/tasks?term=homework HTTP/2.0
Accept-Language: en
```
Accept-Language: en
- Method: Defines the **operation**to be performed
  ```
  get
  ```
- Path: The URL of the resource to be fetched, excluding the scheme and
host
  ```
  tasks?term=homework
  ```
  
- HTTP Version
- Headers: optional information, success as 
  ```
  Accept-Language
  ```
- Body: optional information, usually for methods such as POST and PATCH, which contain the resource being sent to the server
### Request Methods

- GET: ONLY _retrieves information_ for the requested resource of the given URI
POST: Send data to the server to create a new resource.
- PUT: _Replaces all_ of the representation of the target resource with the request data
- PATCH: _Partially modifie_s the representation of the target resource with the request data
- DELETE: _Removes all_ of the representation of the resource specified by the URI
- OPTIONS: Sends the communication options for the requested resource
## Responses


*After the request has been received by the server and processed, the server returns an HTTP response message to the client. The response informs the client of the outcome of the requested operation.*

### Elements:
Status Code & Status Message
- HTTP Version
- Headers: similar to the request headers, provides information about the response and resource representation. Some common headers include:
  ```
  Date
  Content-Type: the media type of the body of the request
  Accept Ranges
  ```
- Body: optional data containing the requested resource

### Codescategories
```
1xx Informational
2xx Success
3xx Redirection
4xx Client Error
5xx Server Error
Common Codes:
200: OK
201: Created
304: Not Modified
400: Bad Request
401: Unauthorized
404: Not Found
405: Method Not Allowed
500: Internal Server Error
```
