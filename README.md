# week-14-homework

Week 14 Homework: Web Development
Overview
In this homework, we will review the many of the concepts and tools covered in the Web Development unit. If needed, refer to the reference sheets provided to you.

curl Reference Sheet curl Reference Sheet
Questions
Before you work through the questions below, please create a new file and record your answers there. This will be your homework deliverable.

HTTP Requests and Responses
Answer the following questions about the HTTP request and response process.

What type of architecture does the HTTP request and response process occur in?
Client-Server Architecture
What are the different parts of an HTTP request?
Request Line, Request Headers, Request Body
Which part of an HTTP request is optional?
Request Body
What are the three parts of an HTTP response?
Headers, Status Line, Body
Which number class of status codes represents errors?
400s range
What are the two most common request methods that a security professional will encounter?
GET and POST requests
Which type of HTTP request method is used for sending data?
POST Request
Which part of an HTTP request contains the data being sent to the server?
Request body
In which part of an HTTP response does the browser receive the web code to generate and style a web page?
Response body
Using curl
Answer the following questions about curl:

What are the advantages of using curl over the browser?

Ability to manage HTTP Requests / Responses in a Repeatable , Programmatic way
Ability to quickly test HTTP HTTP Requests in away that can be automated
Allows ability to make adjustments as the security professional works
Ability to support numerous protocols even if a UI is not present
Which curl option is used to change the request method?

-X
Which curl option is used to set request headers?

-H
Which curl option is used to view the response header?

-I
Which request method might an attacker use to figure out which HTTP requests an HTTP server will accept?

Options
Sessions and Cookies
Recall that HTTP servers need to be able to recognize clients from one another. They do this through sessions and cookies.

Answer the following questions about sessions and cookies:

Which response header sends a cookie to the client?

Set-Cookies HTTP/1.1 200 OK Content-type: text/html Set-Cookie: cart=Bob


Which request header will continue the client's session?

GET /cart HTTP/1.1
Host: www.example.org
Cookie: cart=Bob
'Connection: keep-alive'
Example HTTP Requests and Responses
Look through the following example HTTP request and response and answer the following questions:

HTTP Request

POST /login.php HTTP/1.1
Host: example.com
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Type: application/x-www-form-urlencoded
Content-Length: 34
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Mobile Safari/537.36

username=Barbara&password=password
What is the request method? * POST

Which header expresses the client's preference for an encrypted response? * Upgrade-Insecure-Requests: 1

Does the request have a user session associated with it? * No the Session is not restablished yet

What kind of data is being sent from this request body? * Login credentials

HTTP Response

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
What is the response status code?

200
What web server is handling this HTTP response?

Apache webserver
Does this response have a user session associated to it?

Yes SessionID=5
What kind of content is likely to be in the [page content] response body?

Detail of the page configuration
If your class covered security headers, what security request headers have been included?

Strict-Transport-Security: max-age=31536000; includeSubDomains
Monoliths and Microservices
Answer the following questions about monoliths and microservices:

What are the individual components of microservices called?

Services
What is a service that writes to a database and communicates to other services?

APIs
What type of underlying technology allows for microservices to become scalable and have redundancy?

Load Balancer Technology
Deploying and Testing a Container Set
Answer the following questions about multi-container deployment:

What tool can be used to deploy multiple containers at once?

Docker
What kind of file format is required for us to deploy a container set?

.yml Yaml format
Databases
Which type of SQL query would we use to see all of the information within a table called customers?

SELECT column_name FROM customers;
Which type of SQL query would we use to enter new data into a table? (You don't need a full query, just the first part of the statement.)

INSERT INTO table_name (column_1, column_2, column_3) VALUES (value_1, 'value_2', value_3);
Why would we never run DELETE FROM <table-name>; by itself?

It will delete the entire table there is no select statement.
