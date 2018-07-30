# Instructions for adding code.

## Prerequisites
  * nodejs
  * npm
  
### Step 1

Fork this repository

### Step 2

Implement the features requested in the assigment

### Step 3

Create a PR agains this Branch

> Note : Any PR to merge branch will not be entertained

# Assignment List
* [Service Status](./Assignment-1.md)
* [Approval System](./Assignment-2.md)

# Instructions for the Assigment
 * You are free to add any package. Ensure that it is part fo package.json.
 * There should be a UI where I can specify the Input.
 * Error Handling should be proper. All validations should be handled.
 * Ensure that exceptions do not shut down your server.
 * Use an external logger to classify your output messages into info, debug and error.
 * I should be able to disable the logger in production mode.
 * All configurations should be able to be configured using environment variables.
 * All UI should have a traversable Menu to access the appropriate actions.
 * For CSS use Bootstrap. If you use SASS or LESS it will fetch additional points.
 * All assignments should have a response with the following structure.
  ```$xslt
  {
    result : []
    status : {
        code: "numeric code"
        message : "Message"
    }
  }
  ```
 