# Simple API #

A simple API, no auth protection so you can add and delete what you want in a multi-user mode.

The API is available at `https://apichallenges.eviltester.com`

## Endpoints ##

### List of items ###

GET `/simpleapi/items`

Return all the instances of item

### Create item ###

POST `/simpleapi/items`

We should be able to create item without a ID using the field values in the body of the message. A maximum of 100 items is allowed.

The request body needs to be in JSON format and include the following properties:

 - `type` - String - Required
 - `isbn13` - String - Required
 - `price` - Number - Required
 - `numberinstock` - Integer - Required

Example
```
POST /simpleapi/items
{
  "type": "cd",
  "isbn13": "123-4-56-789012-3",
  "price": 97.99,
  "numberinstock": 0
}
```

The response body will contain the Id.


