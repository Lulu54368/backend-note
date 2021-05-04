---
title: "Introduction"
tags: ""
---

# What is API
,you don't need to understand the entirety of the application implementation in order to interact with it through the API. 

## Benefits
- It **doesn't expose** the implementation to those who s**houldn't have access to it**
- The API provides **a standard way** of **accessing** the application
- It makes it much easier to understand how to access the application's data

## Some examples
- Google
[https://developers.google.com/maps/documentation/](url)
- Spotify
[https://developer.spotify.com/documentation/web-api](url)

# How API works
## Client-Server Communication

1. Client
**_ sends a request _**to the API server

2. The
 API server **_parses that request_**

3. Assuming the request is formatted correctly, the server queries the **__database_ _** for the information or _**performs the action **_in the request

4. The
 server formats the response and**_ sends it back to_** the client
The client renders the response according to its implementation

### Document
[[https://bl](url)og.postman.com/intro-to-apis-what-is-an-api/](url)

# Internet protocals
the protocol for sending data from one computer to another across the internet.

### Categories
- Transmission Control Protocol (TCP) 
  
  used for _data transmission_
- Hypertext Transmission Protocol (HTTP)      transmitting _text and hyperlinks_
- File Transfer Protocol (FTP) which is used to _transfer files_ between server and client


# Restful API


## Restful Principles

- Uniform interface
  - standardized way of accessing and processing data resources
    - resource identifier(eg URL)
    - self-descriptive messages(json VS XML)
    
- Stateless: 
  - Every client request is self-contained
  -  the server doesn't need to store any application data in order to respond to subsequent requests
  -  remember previous requests
- Client-Server: There must be both a client and server in the architecture
