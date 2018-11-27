---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

includes:
  #- errors

search: true
---

# Introduction

Welcome to Scogo API documentation. Scogo API endpoint is ```https://api.scogo.in/v1```

### What API commands are used by Scogo ?
Scogo APIs are plain JSON over HTTP and use the following HTTP verbs:

Command | Purpose
--------- | -------
GET | Fetch one or more objects
POST | Create an object
PUT | Update an object
DELETE | Remove an object

<aside class="notice">
All API requests should hit the secured endpoint i.e. only HTTPS. Calls made over plain HTTP will fail
</aside>

# /auth

Authenticate a user and return ``jwt`` token.

All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication will also fail.

## GET

This endpoint retrieves all the service partners.

### HTTP Request

`GET https://api.scogo.in/v1/servicePartners`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.


> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

<aside class="notice">
You first need to authenticate before interacting with API endpoints.
</aside>



# /servicePartners

## GET

This endpoint retrieves all the service partners.

### HTTP Request

`GET https://api.scogo.in/v1/servicePartners`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.


```shell
curl "https://api.scogo.in/v1/servicePartners"
  -H "Authorization: YourTokenHere"
```

> The above command returns JSON structured like this:

```json
[
  {
    "user_id": 1,
    "first_name": "Fluffums",
    "last_name": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "user_id": 1,
    "first_name": "Fluffums",
    "last_name": "calico",
    "fluffiness": 6,
    "cuteness": 7
  }
]
```


## GET

This endpoint retrieves a specific kitten.

### HTTP Request

`GET https://api.scogo.in/v1/servicePartner/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the service partner to retrieve

```shell
curl "https://api.scogo.in/v1/servicePartners/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```



## DELETE

This endpoint deletes a specified service partner.

### HTTP Request

`DELETE https://api.scogo.in/v1/servicePartners/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the service partner to be deleted

```shell
curl "https://api.scogo.in/v1/servicePartners/2"
  -X DELETE
  -H "Authorization: JWT_Token"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```




# /courierPartners

## GET

This endpoint retrieves all the courier partners.

### HTTP Request

`GET https://api.scogo.in/v1/courierPartners`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.


```shell
curl "https://api.scogo.in/v1/courierPartners"
  -H "Authorization: YourTokenHere"
```

> The above command returns JSON structured like this:

```json
[
  {
    "user_id": 1,
    "first_name": "Fluffums",
    "last_name": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "user_id": 1,
    "first_name": "Fluffums",
    "last_name": "calico",
    "fluffiness": 6,
    "cuteness": 7
  }
]
```


## GET

This endpoint retrieves a specific kitten.

### HTTP Request

`GET https://api.scogo.in/v1/courierPartner/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the courier partner to retrieve

```shell
curl "https://api.scogo.in/v1/courierPartners/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```



## DELETE

This endpoint deletes a specified courier partner.

### HTTP Request

`DELETE https://api.scogo.in/v1/courierPartners/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the courier partner to be deleted

```shell
curl "https://api.scogo.in/v1/courierPartners/2"
  -X DELETE
  -H "Authorization: JWT_Token"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```



# /fieldEngineers

## GET

This endpoint retrieves all the courier partners.

### HTTP Request

`GET https://api.scogo.in/v1/fieldEngineers`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.


```shell
curl "https://api.scogo.in/v1/fieldEngineers"
  -H "Authorization: YourTokenHere"
```

> The above command returns JSON structured like this:

```json
[
  {
    "user_id": 1,
    "first_name": "Fluffums",
    "last_name": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "user_id": 1,
    "first_name": "Fluffums",
    "last_name": "calico",
    "fluffiness": 6,
    "cuteness": 7
  }
]
```


## GET

This endpoint retrieves a specific kitten.

### HTTP Request

`GET https://api.scogo.in/v1/courierPartner/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the courier partner to retrieve

```shell
curl "https://api.scogo.in/v1/fieldEngineers/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```



## DELETE

This endpoint deletes a specified courier partner.

### HTTP Request

`DELETE https://api.scogo.in/v1/fieldEngineers/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the courier partner to be deleted

```shell
curl "https://api.scogo.in/v1/fieldEngineers/2"
  -X DELETE
  -H "Authorization: JWT_Token"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```






