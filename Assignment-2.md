# Approval System

## Solution

Implement an Approval System for a Request

You have to implement the following API.

## API 1 : Register Approver
 * Register level 1 and level 2 approvar
 * Each approver should have a name and designation. The json format of the input payload is
 ```json
{
  "request" : [
    {
      "name" : "Tom Hanks", 
      "Designation" : "Director",
      "role" : "Level 1"
      
    },
    {
      "name" : "Jack Sparrow", 
      "Designation" : "Actor",
      "role" : "Level 2"
    }
  ]
}
```
 
 * Each approver will recieve an Accesstoken (Alphanumeric key with 8 characters).. Response should be like
 
```json
{
  "result" : [
    {
      "name" : "Tom Hanks", 
      "accessToken" : "AFGH768I"
    },
    {
      "name" : "Jack Sparrow", 
      "accessToken" : "UYHIT9879"
    }
  ],
  "status" : {
      "code": "200",
      "message" : "Succesfully registered the approvers"
  }
}
``` 
 * Check for Duplicate values
  > Should have a basic UI

## API 2 : Register Services
 * Should read a list fo services from the input payload. Payload should mention the required aprovals for the service
 * Should immediately return a `Services registered` message
 * Request Strucutre would be
 ```json
 {
    "request" : [
      {
        "name" : "Purchase Iphone", 
        "approvals" : ["Level 1", "Level 2"]
      },
      {
        "name" : "Create Email", 
        "approvals" : ["Level 1"]
      }
    ]
  }
 ```
 * Response will contain service Id for each service created
 * Response structure
 ```json
 {
   "result" : [
     {
        "name" : "Purchase Iphone", 
        "serviceId" : "IKJLH786"
     },
     {
        "name" : "Create Email", 
        "serviceId" : "98767HYN"
     }
   ],
   "status" : {
       "code": "200",
       "message" : "Succesfully registered the services"
   }
 }
 ```
 * Check for duplicate Services
 > Should have a basic UI

## API 3 : Request  a Service
 * API will read a service request and return a request id (Alphanumeric key with 8 characters).
 * Request Structure
 ```json
 {
  "request" : [
    {"sercviceId" : "IKJLH786"}
  ]
 }
 ```
 * Response Should return a Request Token
 * Response structure
 ```json
  {
    "result" : [
      {
         "requestToken" : "IKJLH786"
      }
    ],
    "status" : {
        "code": "200",
        "message" : "Succesfully registered the approvers"
    }
  }
  ```
 > Should have a basic UI

## API 4 : Provide Level 1 Approval
 * Should proide level a approval to a given service
 * Should read accesstoken and service id from the UI.
 * Request Structure
 ```json
 {
  "request" : [
    {
      "sercviceId" : "IKJLH786", 
      "accessToken" : "AFGH768I"
    }
  ]
 }
```
* Response structure
 ```json
  {
    "result" : [
      {
         "requestToken" : "IKJLH786"
      }
    ],
    "status" : {
        "code": "200",
        "message" : "Succesfully Approved"
    }
  }
  ```
 > Should have a basic UI
   
## API 5 : Provide Level 2 Approval 
 * Should proide level a approval to a given service
 * Should read accesstoken and service id from the UI.
 * Should read accesstoken and service id from the UI.
  * Request Structure
  ```json
  {
   "request" : [
     {
       "sercviceId" : "IKJLH786", 
       "accessToken" : "AFGH768I"
     }
   ]
  }
 ```
 * Response structure
  ```json
   {
     "result" : [
       {
          "requestToken" : "IKJLH786"
       }
     ],
     "status" : {
         "code": "200",
         "message" : "Succesfully Approved"
     }
   }
   ```
   * Should check if the Level 1 approval is already provided. Level 2 should not be provided if level 1 is not granted
 > Should have a basic UI
 
## API 6 : Check status of the service request.
 * Should provide level a approval to a given service
 * Should read Access Token and service id from the UI.
 * Request JSON should be
 ```json
{
   "request" : [
     {
       "requestToken" : "IKJLH786"
     }
   ]
  }
```
 Response structure
   ```json
    {
      "result" : [
        {
           "requestToken" : "IKJLH786",
           "approvals" : {
            "stage" : "level1",
            "Approver" : "Tom Hanks",
            "Approver date" : "22/08/2018"
           }
        }
      ],
      "status" : {
          "code": "200",
          "message" : "Succesfully Approved"
      }
    }
    ``` 
 > Should have a basic UI