---
title: "HTTP"
tags: ""
---

# End points and payloads
## Organizing API end points

### Principles
- intuitive
- Organize by resource
  - Use** nouns** in the path, not verbs
  - The method used will determine the operation taken
GOOD:
  ```
  https://example.com/posts
  ```
BAD:
  
  ```
  https://example.com/get_posts
  ```
  *Not concise*
- Keep a consistent scheme
  -** Plural nouns** for collections
  - Use **parameters** to specify a specific item
  
  
  
  GOOD:
  ```
  https://example.com/entrees
  https://example.com/entrees/5
  ```
  *entrees collection 5th ID*


  BAD:
  ```
  https://example.com/entree
  https://example.com/entree_five
  ```
 _Don’t make them too complex or lengthy
No longer than collection/item/collection_


*Looking for Id 5 in entrees , Id 4 in customers*
  
  
  GOOD:
  ```
  https://example.com/entrees/5/reviews
  ```
BAD:


```
https://example.com/entrees/5/customers/4/reviews
```

## CORS
_Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate **any other origins**(domain, scheme, or port) than its own from which a browser should permit loading of resources_

In normal cases, a web application using those APIs can only request resources from the same origin the application was loaded from unless the response from other origins includes the right CORS headers.

### machanism
- browser makes request to server
- check whether the server will permit
- sends methods and headers

### problem
the specification mandates that browsers "preflight" the request, soliciting supported methods from the server with the HTTP OPTIONS request method, and then, upon "approval" from the server, sending the actual request.
