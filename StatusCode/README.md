# HTTP response status codes

HTTP response status codes indicate whether a specific HTTP request has been successfully completed.  

Responses are grouped into five categories:   
1.Informational responses (100 – 199)  
2.Successful responses (200 – 299)  
3.Redirection messages (300 – 399)  
4.Client error responses (400 – 499)  
5.Server error responses (500 – 599)

# 1.Information responses

**100 Continue**
This  response indicates that the client should continue the request or ignore the response if the request is already finished.

**101 Switching Protocols** 
This code is sent in response to an Upgrade request header from the client and indicates the protocol the server is switching to.

**102 Processing (WebDAV)**
This code indicates that the server has received and is processing the request, but no response is available yet.

 **103 Early Hints**

This status code is mainly used with the Link header. It allows the browser to start preloading resources or establishing connections to needed origins while the server is still preparing the response.

# Successful responses

**200 OK**
- The request was successful. The meaning of "success" varies by method:
  - **GET**: The resource was fetched and is in the response body.
  - **HEAD**: Headers are in the response, no body.
  - **PUT or POST**: The result of the action is in the response body.
  - **TRACE**: The response body contains the request message received by the server.

**201 Created**
- The request was successful, and a new resource was created. Commonly used after POST or some PUT requests.

**202 Accepted**
- The request was received but hasn't been acted upon yet. It may be handled by another process or server later.

**203 Non-Authoritative Information**
- The response metadata is from a local or third-party source, not the origin server. Use 200 OK if the metadata is from the origin server.

**204 No Content**
- No content to send for this request, but headers might be useful. The user agent can update its cached headers for this resource.

**205 Reset Content**
- Tells the user agent to reset the document that sent this request.

**206 Partial Content**
- The response contains part of the resource, as requested with the Range header.

**207 Multi-Status (WebDAV)**
- Provides information about multiple resources where multiple status codes might be needed.

**208 Already Reported (WebDAV)**
- Used to avoid repeatedly listing the internal members of multiple bindings to the same collection in a <dav:propstat> response element.

**226 IM Used (HTTP Delta encoding)**
- The server has fulfilled a GET request, and the response represents the result of one or more instance manipulations applied to the current instance.  

# Redirection messages

**300 Multiple Choices**
- The request has multiple possible responses. The user or browser should choose one. HTML links to options are recommended.

**301 Moved Permanently**
- The resource URL has changed permanently. The new URL is in the response.

**302 Found**
- The resource URL has changed temporarily. The same URL should be used for future requests.

**303 See Other**
- The server directs the client to fetch the resource at a different URL using a GET request.

**304 Not Modified**
- For caching. It tells the client to use the cached version of the response as it hasn't changed.

**305 Use Proxy (Deprecated)**
- Previously indicated that the resource must be accessed via a proxy. Now deprecated for security reasons.

**306 Unused**
- No longer used, reserved for future use.

**307 Temporary Redirect**
- The server directs the client to a different URL using the same HTTP method as the original request.

**308 Permanent Redirect**
- The resource is now permanently at a new URL. Use the same HTTP method as the original request (e.g., POST remains POST).

# Client error responses


**400 Bad Request**
- The server can't process the request due to client error (e.g., bad syntax).

**401 Unauthorized**
- The client must authenticate to get the requested response.

**402 Payment Required**
- Reserved for future use for digital payments.

**403 Forbidden**
- The client is known but does not have permission to access the resource.

**404 Not Found**
- The server can't find the requested resource.

**405 Method Not Allowed**
- The request method is not supported by the resource.

**406 Not Acceptable**
- The server can't provide a response that matches the client's criteria.

**407 Proxy Authentication Required**
- Authentication is required by a proxy.

**408 Request Timeout**
- The server wants to close the idle connection.

**409 Conflict**
- The request conflicts with the current server state.

**410 Gone**
- The requested resource is permanently deleted.

**411 Length Required**
- The server requires the Content-Length header.

**412 Precondition Failed**
- The server does not meet the client's preconditions.

**413 Payload Too Large**
- The request entity is too large for the server.

**414 URI Too Long**
- The requested URI is too long for the server to handle.

**415 Unsupported Media Type**
- The server doesn't support the request's media format.

**416 Range Not Satisfiable**
- The requested range is not available.

**417 Expectation Failed**
- The server cannot meet the Expect header requirements.

**418 I'm a teapot**
- The server refuses to brew coffee with a teapot.

**421 Misdirected Request**
- The request was sent to the wrong server.

**422 Unprocessable Content**
- The request is well-formed but contains semantic errors.

**423 Locked**
- The resource is locked.

**424 Failed Dependency**
- A previous request failed, causing this request to fail.

**425 Too Early**
- The server is unwilling to process a request that might be replayed.

**426 Upgrade Required**
- The server requires the client to use a different protocol.

**428 Precondition Required**
- The server requires the request to be conditional to prevent conflicts.

**429 Too Many Requests**
- The client has sent too many requests in a short time.

**431 Request Header Fields Too Large**
- The request headers are too large for the server.

**451 Unavailable For Legal Reasons**
- The resource is unavailable due to legal reasons, like government censorship.

# Server error responses
**500 Internal Server Error**
- The server encountered an unexpected error.

**501 Not Implemented**
- The server does not support the request method. Servers must support GET and HEAD.

**502 Bad Gateway**
- The server acting as a gateway received an invalid response from the upstream server.

**503 Service Unavailable**
- The server is not ready to handle the request, often due to maintenance or overload. A Retry-After header may indicate when to try again.

**504 Gateway Timeout**
- The server acting as a gateway did not get a response in time.

**505 HTTP Version Not Supported**
- The server does not support the HTTP version used in the request.

**506 Variant Also Negotiates**
- Internal server configuration error with content negotiation.

**507 Insufficient Storage (WebDAV)**
- The server cannot store the needed representation to complete the request.

**508 Loop Detected (WebDAV)**
- The server detected an infinite loop while processing the request.

**510 Not Extended**
- The request needs further extensions to be fulfilled by the server.

**511 Network Authentication Required**
- The client must authenticate to gain network access.




