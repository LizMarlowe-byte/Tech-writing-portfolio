# {API Name} Guide

## Overview

The {Name of API} allows you to {describe what it allows you to do}. You can use the {Name of API} to {describe examples, use cases, etc.}. 

> For example: The Widgets API allows you to create, retrieve, update, and delete widgets. It supports pagination, filtering, and authentication via Bearer tokens.

For REST APIs:
The {Name of API} is organized around REST. It has resource-oriented URLs, form-encoded request bodies, returns JSON-encoded responses, and uses standard HTTP response codes and authentication.

---

## Base URL

All API requests are made to the following base URL. Append the endpoint paths to this root URL when constructing requests. The API is served over HTTPS for security, and all endpoints are versioned.

**Production:**

'''

https://api.example.com

'''

**Sandbox (for testing):** 

'''

https://sandbox.api.example.com

'''

---

## Authentication
{Describe the authentication method(s) used for the API, such as using an API key, OAuth, Bearer token, etc.}

Example 1:
The {Name of API} uses [API keys](#get-an-api-key) to authenticate requests. All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication will also fail.

Example 2:
All requests require a **Bearer token** in the `Authorization` header.

**Header:**
```
Authorization: Bearer <YOUR_TOKEN>
```

Include:
- `Authorization` header on every request
- `Content-Type: application/json` for requests with JSON bodies
- `Accept: application/json` to request JSON responses

> How to obtain a token: Refer to your account or developer portal. Tokens typically expire; handle refresh per your auth system.}
>

---

## Rate limits
A rate limit is the number of requests the API can receive in a specific time period. API rate limiting helps ensure that the API runs efficiently and is available to all users. It also prevents abuse and denial-of-service attacks. Once the limit is reached, API requests from the client fail.

{Describe the rate limits for the API - for example:

The rate limits are different, depending on whether you are an authenticated or unauthenticated user:

- Rate limit for _authenticated_ users: You can use a personal access token to make API requests. Additionally, you can authorize an OAuth app to make API requests on your behalf. When using a personal access token, you have a personal rate limit of 6,000 requests per hour. Requests made on your behalf have a higher rate limit of 16,000 requests per hour.
  
- Rate limit for _unauthenticated_ users: You can only make unauthenticated requests if you are only retrieving public data. The primary rate limit for unauthenticated requests is 50 requests per hour.}

### Rate limit headers

- `X-RateLimit-Limit`: total quota
- `X-RateLimit-Remaining`: remaining quota in the current window
- `X-RateLimit-Reset`: UNIX timestamp when the window resets

**Example 429 error response:**

```json
{
  "error": {
    "code": "rate_limited",
    "message": "Too many requests. Try again later.",
    "retry_after": 30,
    "request_id": "req_xR72m3"
  }
}
```

---

## Status codes and errors
Errors and statuses are returned with appropriate HTTP status codes and a structured JSON body.

### Example error JSON response

```json
{
  "error": {
    "code": "invalid_request",
    "message": "Field 'name' is required.",
    "details": [
      { "field": "name", "issue": "missing" }
    ],
    "request_id": "req_8fA7ka"
  }
}
```

### Common HTTP status codes

|Code           |Description|When it occurs|
|:--------------|:----------|:-------------|
|200            |OK         |Successful requests|
|201            |Created    |Resource created (POST)  |
|204            |No Content |Successful DELETE  |
|400            |Bad Request|Validation errors, malformed JSON  |
|401            |Unauthorized|Missing/invalid token|
|403            |Forbidden   |Insufficient permissions|
|404            |Not Found   |Resource does not exist|
|409            |Conflict    |duplicate or version conflict|
|429            |Too Many Requests|Rate limited|
|500            |Server Error|Unexpected server-side error

---

## Pagination
Two patterns are supported in the {Name of API} API:

- [Offset Pagination](#offset-pagination): You specify in the request a limit (number of items per page) and an offset or page number. For example, you can use the query parameters **limit=50&page=2** to limit the response to 50 items a page, starting with page 2.
  
- [Cursor Pagination](#cursor-pagination): You specify in the request a cursor or token representing a position in the dataset. You pass the cursor to get to the next page. For example, you can use the query parameters **limit=50&cursor=c_abc** to limit the response to 50 items a page, starting with the position c_abc in the dataset.

### Offset Pagination
**Request:** `GET /v1/widgets?limit=50&page=2`

**Response:**
```json
{
  "items": [
    { "id": "w_12345", "name": "Example Widget" }
  ],
  "page": 2,
  "limit": 50,
  "total": 317
}
```

### Cursor Pagination
**Request:** `GET /v1/widgets?limit=50&cursor=c_abc`

**Response:**
```json
{
  "items": [
    { "id": "w_12345", "name": "Example Widget" }
  ],
  "next_cursor": "c_def",
  "prev_cursor": "c_xyz"
}
```

---

# Getting Started
To get started using the <Name of API>, do the following:
- [Set up your account](#set-up-your-account)
- [Get an API Key](#get-an-api-key)

## Set up your account
{Describes how to set up your account, either free or fee-based, in order to use the API.}

## Get an API Key
{Describes how to get an API key.}

# API Reference: Requests and Responses
{Intro about that these are common requests and responses used by the API, etc.}

## Actions
- [Action 1](#Action-1)
- [Action 2](#Action-2)
- [Action 3](#Action-3)

## Action 1
---
{Description}

### URL

{Method}  http(s): / / {domain} / resources

### Sample Request

{Method} http(s)://{domain}/resources?query1=value1&query2=value2

Header1: Value1

Header2: Value2

{

  "element1": "value1",
  
  "element2":  "value2"
  
}

## Query Parameters

|Parameter      |Description|Type  |Required|Notes|
|:--------------|:----------|:-----|:-------|-----| 
|{Text}         |{Text}     |{Text}|{Text}  |{Text}|
|{Text}         |{Text}     |{Text}|{Text}  |{Text}|
|{Text}         |{Text}     |{Text}|{Text}  |{Text}|
|{Text}         |{Text}     |{Text}|{Text}  |Valid values include:<ul><li>**Value**:{Description of value}</li><li>**Value**:{Description of value}</li><li>**Value**: {Description of value}</li></ul>

## Headers

|Header Name    |Description|Required|Notes|
|:--------------|:----------|:-------|-----| 
|{Text}         |{Text}     |{Text}  |{Text}|
|{Text}         |{Text}     |{Text}  |{Text}|
|{Text}         |{Text}     |{Text}  |{Text}|
|{Text}         |{Text}     |{Text}  |{Text}|

## POST or PUT Body

|Element        |Description|Type  |Required|Notes|
|:--------------|:----------|:-----|:-------|-----| 
|{Text}         |{Text}     |{Text}|{Text}  |{Text}|
|{Text}         |{Text}     |{Text}|{Text}  |{Text}|
|{Text}         |{Text}     |{Text}|{Text}  |{Text}|
|{Text}         |{Text}     |{Text}|{Text}  |{Text}|

## Sample Response
{

  "element1": "value1",
  
  "element2":  "value2"
  
}

## Response Elements

|Element        |Description|Type    |Notes|
|:--------------|:----------|:-------|-----| 
|{Text}         |{Text}     |{Text}  |{Text}|
|{Text}         |{Text}     |{Text}  |{Text}|
|{Text}         |{Text}     |{Text}  |{Text}|
|{Text}         |{Text}     |{Text}  |{Text}|
