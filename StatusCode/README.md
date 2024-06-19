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




