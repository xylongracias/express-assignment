# Assignment 1

 ## Solution

Need a server that will check the status of a remote server. The application should provide the following features.
### API 1
  * The API should read a JSON payload with a list of services and the method.
    >The structure of the payload should be decided by the developer

  * The API should immediately return a request saying `Request is accepted` 
  * The API should store the data in DB
  
### API 2
  * The API should read a JSON payload with a list of services and the method.
    >The structure of the payload should be decided by the developer
    
  * The API should return a JSON with the status of each service.
  
### The solution should provide a basic UI

 ## Key Points
  * You are free to add any package. ensure that is part fo package.json
  * There should be a UI where I can specify the Input.
  * Error Handling should be proper. All validations should be handled.
  * Ensure that exceptions do not shut down your server
  * Use an external logger to classify your output messages into info, debug and error
  * I should be able to disable the logger in production mode
  * All configurations should be able to be configured using environment variables.