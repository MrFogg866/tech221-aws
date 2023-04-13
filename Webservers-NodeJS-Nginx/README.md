## Webservers - NodeJS - NGINX


### How do Webservers work?

- When a user specifies a URL in the browser address bar, the web browser will then obtain the IP Adrress of the domain name through DNS (Domain Name System).
- This then goes gives access to the Web server, the browser requests the specific file from the web server by HTTP request
- The web server then responds, sending the browser the requested page through HTTP

### How does NODEJS work?

- Node.JS it is not a web server and it runs on the VB JavaScript Engine
- Nodejs allows us to have multiple threads (a thread is like a request) on a single CPU
- Node.JS will split the CPU time evenly between the threads


### How does NGINX work?

- NGINX is one of the most reliable servers for speed and scalability
- Used by online giants are Google, Netflix, Adobe, Cloudflare, WordPress.com
- NGINX uses worker connections contained in worker processes the worker process then handles all of the requests of the worker connection, the worker process then send to the master process to receive the results
- One worker connection may take care of unto 1024 requests
- This is why NGINX is the fastest web server


### Top 10 Use cases of NodeJS

1. Developing Streaming Web Applications
2. Developing Real-Time Chat-bots
3. Developing Collaboration Tools
4. Developing Big Data and Analytics Solutions
5. Developing Single-Page Applications
6. The Crafting of Microservices Architecture
7. Developing Dashboard to Track Real-time data
8. Crafting Web Extraction and Automation solutions
9. Enabling Server-side proxy
10. Facilitating Wireless Connectivity

### What are the dependencies of Nodejs?

* Production Dependencies
* Development Dependencies
* Peer Dependencies
* Optional Dependencies
* Bundled Dependencies

### What is NPM?

- NPM  is The World's Largest Software Registry (Library)
- The registry contains over 800,000 code packages.
- Open-source developers use npm to share software.
- Many organizations also use npm to manage private development
- npm is also a software Package Manager and Installer
- npm is free to use.



### What is a Reverse Proxy?


-  It’s a backend tool used by system administrators. 
- Instead of connecting directly to a website serving content, a reverse proxy like NGINX can sit in the middle. 
- When it receives a request from a user, it will send forward, or “proxy,” that request to the final server. This server is called the “origin server” since it’s what will actually be responding to requests.
- They can be used for Centralized Logging,Configurable Frontend,Network Protection & Privacy, Caching, Load Balancing