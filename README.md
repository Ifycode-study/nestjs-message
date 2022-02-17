# Nestjs message api

App goal: Store and receive messages (strings) stored in a plain JSON file.

Create a module:

````
nest generate module messages
````

Generate a controller (set of) files:
````
nest generate controller messages/messages --flat
````
## VScode rest client extension setup
Instead of using postman, you can use the "VScode rest client" extension (iif you are using VScode editor).
- Install this extension from VScode extensions inside the VScode editor.
- Create a file called request.http in the root of your project, and add simple e.g. get and post requests such as the one in the code block below inside it.
- Start your dev server in thhe terminal as usual, test that the code in your controller is working by clicking the "send request" button in the request.http file.

````
### List all messages

GET http://localhost:3000/messages


### Create a new message
POST http://localhost:3000/messages
content-type: application/json

{
  "content": "hi there"
}


### Get a particular message

GET http://localhost:3000/messages/123123123
````

## Pipes and validation
Install two packages for use:
- class-validator
- class-transformer