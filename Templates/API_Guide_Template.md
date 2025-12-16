# Overview

The {Name of API} allows you to {describe what it allows you to do}. You can use the {Name of API} to {describe examples, use cases, etc.}.

The {Name of API} is organized around REST. It has resource-oriented URLs, form-encoded request bodies, returns JSON-encoded responses, and uses standard HTTP response codes and authentication. 

## Rate limits
There are a limited number of REST API requests that you can make within a specific amount of time. This limit helps prevent abuse and denial-of-service attacks, and ensures that the API is available for all users.

The rate limits are different, depending on whether you are an authenticated or unauthenticated user:

- Rate limit for _authenticated_ users: You can use a personal access token to make API requests. Additionally, you can authorize an OAuth app to make API requests on your behalf. When using a personal access token, you have a personal rate limit of 6,000 requests per hour. Requests made on your behalf have a higher rate limit of 16,000 requests per hour.
  
- Rate limit for _unauthenticated_ users: You can only make unauthenticated requests if you are only retrieving public data. The primary rate limit for unauthenticated requests is 50 requests per hour.

## Key concepts
{Explain key concepts of the API, including terms specific to the API. For each concept, write a paragraph.}

## Workflow
{Explain the order of common tasks to do using the API. Add a workflow diagram.}

## Architecture
{Explain the main system components of the API and how they fit together. Add an architectural diagram.}

# Getting Started
To get started using the <Name of API>, do the following:
- [Register in the development portal](#register-in-the-development-portal)
- [Get an App Key](#get-an-app-key)

## Register in the development portal
{Describes how to register in the dev portal.}

## Get an App Key
{Describes how to get an app key.}

# Authentication
{Describe the authentication method(s) used for the API.}

# Requests & Responses
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
