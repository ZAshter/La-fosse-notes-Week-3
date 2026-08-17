# La-fosse-notes-Week-3- Monday 17th August 2026
#Backend development 

API is taking something that is complicated and making it easy and sophisticated for you to understand.
anything that talks to a netform is making a request and asking for it back. 

using: https://bored-api.appbrewery.com/
then...
#Thunderclient in VS code
- https://**bored-api.appbrewery.com**/random  
- **base url** essentially this doesnt change
- the word after the / is called an endpoint
- Resource= a way of grouping together similar endpoints e.g:
- bbc.com/sports/football     //sports is the resource here, bbc is the base and football is the endpoint

DONT CONFUSE END POINTS WITH THESE parameters:

1) REQUEST PARAMETER URL/ID (id is not an endpoint it is a request parameter)
2) request query URL?type=walue (type=value is a request query)

#Query parameters
e.g type=music
can combine parameters using '&'.For example: type=music&participants=1

can filter the activity using the key number given e.g
 https://bored-api.appbrewery.com/activity/3943506  

# **What is the idea behind rest?**
https://en.wikipedia.org/wiki/REST

The formal REST constraints are as follows:
- Client/Server – Clients are separated from servers by a well-defined interface
- Stateless – A specific client does not consume server storage when the client is "at rest"
- Cache – Responses indicate their own cacheability
- Uniform interface
- Layered system – A client cannot ordinarily tell whether it is connected directly to the end server, or to an intermediary along the way
- Code on demand (optional) – Servers are able to temporarily extend or customize the functionality of a client by transferring logic to the client that can be executed within a standard virtual machine (the server can send code that the client can execute)

- we installed devn dependency called demon which allows to run in the background (npm i -D nodemon)
- scripts needed are "dev": "nodemon index.js"
    "start": "node injex.js"
- then npm run dev

- We then installed dependency express by npm i express
  <img width="1536" height="2048" alt="WhatsApp Image 2026-08-17 at 11 05 11" src="https://github.com/user-attachments/assets/3dd09557-ca83-4b95-bf2e-f49969bc26a6" />

  We want to create the program

 
