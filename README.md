# TicketMaster_Project
Titan is event search and recommendation app + service to improve personal experience for event seekers.
The front end includes HTML page and an iOS app to interact user. 
The backend includes a database and a java service to process data.
At last, we deploy this service to Amazon Cloud and you can access everywhere.

API to implement:
1. Show events near your location (namely SearchEvents)
2. set favored events (namely ViewHistory)
3. Recommend new events (namely RecommendEvents)

HTTP request message:
URL
Request method: Get, Post, Delete
Request body (optional) - content

HTTP response message:
Status Code
Response body

URL: identify the resource over the web
protocal://hostname:port/path-and-file-name
http://localhost:8080/Titan/history

Web application:
Software application that user runs in the web browser.
Web service:
API runs on the server, which provides data to the client over http through a standardized messaging system (XML, JSON)

3-tier application architecture
Presentation layer
Logic layer
Data layer

Servlet
1. Java servlet is a java program that extends the capabilities of a server. -> implement applications hosted on Web 	Servers.
2. Java servlet response to particular network request (HTTP request)
3. javax.servlet / javax.servlet.http

Tomcate Apache (servlet container)
Tomcate Server, which is java servlet container and provides http web server environment in which java code could run. 
Servlets runs in container.
Container handles the networking side (parsing http request and connection handling), mapping a URL to a particular servlet and ensuring that the URL requester has the correct access-rights.



Rest Architecture style for designing networked application, uses simple HTTP to make calls between machines.
1. Uniform Interface -> simplify and decouple
2. Stateless -> each request from client to server must contain all the information. Session state is entirely kept on 	  the client.
3. Cacheable
4. Clent-server
Benefit: decoupling, server = resources + operation

Titan:
1. Search for nearby [SearchItem], given lat, lon, return a list of object.
	a. Package: rpc
	b. Class name: SearchItem
	c. URL pattern: /search, http method: get
2. Recommend event for users, given an id and given a list of favorite events objects.
	URL pattern: /recommendation, http method: get
3. Set/Unset favorite events for user, given id and a list of favorite event ids, return status[OK or ERROR]
	URL pattern: /history, http method: post

JSON
data-interchange format
Key Value pair
JSON only allow key names to be String
JSON array: ["John": "Jack", "Mary": "Bob"]



