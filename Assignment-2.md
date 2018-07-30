# Assignment 2

## Solution

Implement an Approval System for a Request

You have to implement the following API.

## API 1 : Register Approver
 * Register level 1 and level 2 approvar
 * Each approver will recieve a Accesstoken (Alphanumeric key with 8 characters).
 * Same user cannot have both the roles
  > Should have a basic UI

## API 2 : Register Services
 * Should read a list fo services from the input payload. Payload should mention the required aprovals for the service
 * Should immediately return a `Services registered` message
 > Should have a basic UI

## API 3 : Request  a Service
 * User will read a service request and return a request id (Alphanumeric key with 8 characters).
 > Should have a basic UI

## API 4 : Provide Level 1 Approval
 * Should proide level a approval to a given service
 * Should read accesstoken and service id from the UI.
 > Should have a basic UI
   
## API 5 : Provide Level 2 Approval 
 * Should proide level a approval to a given service
 * Should read accesstoken and service id from the UI.
 > Should have a basic UI