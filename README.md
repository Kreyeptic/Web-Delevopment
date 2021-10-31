# Web-Delevopment
Week 14 Cyber Security Homework


In this homework, we will review the many of the concepts and tools covered in the Web Development unit. If needed, refer to the  reference sheets provided to you.

[HTTP Reference Sheet](https://github.com/kryshael/Week-14-Homework/blob/main/Reference/HTTP_Reference.md)

[curl Reference Sheet](https://github.com/kryshael/Week-14-Homework/blob/main/Reference/cURL_Reference.md)


 ### Questions
 
Before you work through the questions below, please create a new file and record your answers there. This will be your homework deliverable.

 ### HTTP Requests and Responses

Answer the following questions about the HTTP request and response process:

-What type of architecture does the HTTP request and response process occur in?

1. What type of architecture does the HTTP request and response process occur in?

```bash
Client-Server Architecture
```

2. What are the different parts of an HTTP request?

```bash
Request Line
Request Headers
Request Body
```

3. Which part of an HTTP request is optional?
```bash
Request Body
```

4. What are the three parts of an HTTP response?
```bash
Headers
Status Line
Body
```

5. Which number class of status codes represents errors?
```bash
400 range
```

6. What are the two most common request methods that a security professional will encounter?
```bash
GET Request
POST Request
```
7. Which type of HTTP request method is used for sending data?
```bash
POST Request
```

8. Which part of an HTTP request contains the data being sent to the server?
```bash
Request Body
```

9. In which part of an HTTP response does the browser receive the web code to generate and style a web page?
```bash
Request Body
```
 
  ### Using Curl
 
 Answer the following questions about curl:
 
10. What are the advantages of using curl over the browser?
```bash
* Ability to send and receive HTTP requests without the need for a user interface
* Ability to automate requests, but also be able to make adjustments
* Supports a variety of protocols
```
11. Which curl option is used to change the request method?
 ```bash
-X
```
12. Which curl option is used to set request headers?
 ```bash
-i
```
13. Which curl option is used to view the response header?
```bash
-h
```
14. Which request method might an attacker use to figure out which HTTP requests an HTTP server will accept?
```bash
Options
```
#### Sessions and Cookies

Recall that HTTP servers need to be able to recognize clients from one another. They do this through sessions and cookies.

Answer the following questions about sessions and cookies:

15. Which response header sends a cookie to the client?

  ```bash
Set-Cookie: cart=Bob
```

16. Which request header will continue the client's session?

```bash
Connection: Keep-Alive
```

#### Example HTTP Requests and Responses

Look through the following example HTTP request and response and answer the following questions:

**HTTP Request**

```HTTP
POST /login.php HTTP/1.1
Host: example.com
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Type: application/x-www-form-urlencoded
Content-Length: 34
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Mobile Safari/537.36

username=Barbara&password=password
```

17. What is the request method?
```bash
POST
```
18. Which header expresses the client's preference for an encrypted response?
```bash
Upgrade-Insecure-Requests: 1
```
19. Does the request have a user session associated with it?
```bash
No
```
20. What kind of data is being sent from this request body?
```bash
Login credentials
```
**HTTP Response**

```HTTP
HTTP/1.1 200 OK
Date: Mon, 16 Mar 2020 17:05:43 GMT
Last-Modified: Sat, 01 Feb 2020 00:00:00 GMT
Content-Encoding: gzip
Expires: Fri, 01 May 2020 00:00:00 GMT
Server: Apache
Set-Cookie: SessionID=5
Content-Type: text/html; charset=UTF-8
Strict-Transport-Security: max-age=31536000; includeSubDomains
X-Content-Type: NoSniff
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block

[page content]
```

21. What is the response status code?
```bash
200
```
22. What web server is handling this HTTP response?
```bash
Apache
```
23. Does this response have a user session associated to it?
```bash
Yes. SessionID=5
```
24. What kind of content is likely to be in the [page content] response body?
```bash
Details on the page configuration
```
25. If your class covered security headers, what security request headers have been included?
```bash
Strict-Transport-Security: max-age=31536000; includeSubDomains
```
#### Monoliths and Microservices

Answer the following questions about monoliths and microservices:

26. What are the individual components of microservices called?
```bash
Services
```
27. What is a service that writes to a database and communicates to other services?
```bash
API
```
28. What type of underlying technology allows for microservices to become scalable and have redundancy?
```bash
Load Balancer Technology
```
#### Deploying and Testing a Container Set

Answer the following questions about multi-container deployment:

29. What tool can be used to deploy multiple containers at once?
```bash
Docker
```
30. What kind of file format is required for us to deploy a container set?
```bash
.yml
Yaml Format
```
#### Databases

31. Which type of SQL query would we use to see all of the information within a table called `customers`?
```bash
SELECT column_name FROM customers
```
32. Which type of SQL query would we use to enter new data into a table? (You don't need a full query, just the first part of the statement.)
```bash
INSERT INTO `table_name` (column_1,column_2,column_3) VALUES (value_1,value_2,value_3)
```
33. Why would we never run `DELETE FROM <table-name>;` by itself?
```bash
It will delete the entire table if nothing is selected
```
---

