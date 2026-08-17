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

1) REQUEST PARAMETER URL/:ID (id is not an endpoint it is a request parameter)
2) request query URL?type=value (type=value is a request query)

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
- if we want to use json we need to use {} and "".

- request parameter is usually only one value

  #what we have entered in our js file so far:
- const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
    res.status(420).end()
})
//means if someone makes a get request from '/' I  am going to look at the request made by the client and generate a response

app.listen(port, () => {
    console.log(`Example app running on port ${port}`)
})
//gets the app up and running

 
<img width="1606" height="546" alt="image" src="https://github.com/user-attachments/assets/aecae15c-0e59-42ab-903b-f13172d9636c" />


#Architechure patterns 

**sofware design patterns (why seperate files rather than work on one document?)**
1) scaling (as the project gets bigger its easier to know where to narrow a bug to etc)
2) Teamwork (avoids merge conflicts)
3) Testing/debugging

**How do we achieve this then?**
Separation of concern
i.e 3 files:
-index.html
-script.js
-styles.css

component based architechure
-doing separation of concern but for components
e.g. a button component

#**MVC architechure1**

breaks down an entire application intro three parts:
1) view- I as a user clicks on a button on a page
2) controller- what button do i need to request (may speak to model- kind of like a middle man)
3) Model- interacts with database.

   <img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/e9930e97-f985-4bda-912e-14683859d7c5" />

#Microservices vs Monolithic
A monolithic architecture builds an entire application as a single, unified unit with one centralized codebase and database, whereas a microservices architecture breaks an application into a collection of small, independent, loosely coupled services that communicate via APIs.

<img width="989" height="538" alt="image" src="https://github.com/user-attachments/assets/b4f5fd54-9a75-42c0-a215-129945a99c56" />

#HTTP Methods
- GET- Retrieves data from specified recourse
- POST- submit data to be processed to a specified resource
- PUT - update a specified resource 
- PATCH- update partial resource
- DELETE - delete a specified resource

ACRONYM: standard and used for lots of things
c post
r get
u patch 
d delete

#Building a CRUD application (crud rest API)

currently we have building: client request --> app --> get --> response
now we will make: client request --> app --> controller --> model 
<img width="1536" height="2048" alt="image" src="https://github.com/user-attachments/assets/73db99fc-d844-4260-bff2-19e63b0df0fe" />

The model is for handling data/representing data and talks to the controller.
The controller is responsible for handling the request and responsw

#class
-Classes are a template for creating objects. They encapsulate data with code to work on that data.
class Animal {
  constructor(name, age, species, hobby) {
  this.name = name
  this.age = age
  this,species = species
  this.hobby= hobby;
  }
  welcome() {
   return `My name is ${this.name}. I am ${this.age}. I am a ${this.species} and I love ${this.hobby}`
}
}


#when something is declared as static it belongs to the class itself and not the objects.
class  needs to be singular and have a capital letter at the start of its name e.g Fruit not Fruits
   

