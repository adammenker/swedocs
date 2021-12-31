# HTTP/HTTPS

---

# Overview
* HTTP vs HTTPS
  * HTTPS is secure version of HTTP
    * uses SSL or TSL for security 
* Stateless
  * requests are independent
  * data is not cached
    * must use cookies or sessions to create a state
---
# Methods
### GET 
* gets data from the server
  * passes request parameters through the url
  * is not secure
  * should only be used to retrieve non-sensitive data

### POST
* sends data to the server
  * passes request parameters through the body of the request
    * makes request secure
  * should be used to add data to the server or database

### PUT
* used to update data in the server or database
* vulnerable to arbitrary data

### DELETE
* used to remove data from the server or database
* vulnerable to arbitrary data
---

# Header
* where the request and response data is held
### general
* the url, method, status code...
### request
* what the client sends
* cookies, content type, authorization
### response
* what the server sends back
* server name, content type, date, set cookies
---

# Status Codes
* 100s => informational 
* 200s => success
* 300s => redirect, request was received but needs extra step to be completed
  * 302 => redirect occurred
  * 304 => caching occurred
* 400s => client error
  * 401 => unauthorized
  * 404 => not found
* 500s => server error
---

# HTTP2
* faster and more efficient
  * make multiple request to get multiple responses
    * req -> req -> req -> res -> res -> res
      * previously need to wait for response before sending another request
* responds with more data
* more secure