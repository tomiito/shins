---
title: API Docs
language_tabs:
  - shell: curl
  - javascript: JavaScript
  - java: Java
  - php: PHP
  - python: Python
  - csharp: 'C#'
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="api-docs">API Docs v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Docs to be filled...

Base URLs:

* <a href="https://api.notihub.com/">https://api.notihub.com/</a>

<h1 id="api-docs-users">Users</h1>

## 1

<a id="opId1"></a>

> Code samples

```shell
curl --request GET \
  --url https://api.notihub.com//v1/users/string \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/users/string",
  "method": "GET",
  "headers": {
    "accept": "application/json"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```java
OkHttpClient client = new OkHttpClient();

Request request = new Request.Builder()
  .url("https://api.notihub.com//v1/users/string")
  .get()
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/users/string');
$request->setMethod(HTTP_METH_GET);

$request->setHeaders(array(
  'accept' => 'application/json'
));

try {
  $response = $request->send();

  echo $response->getBody();
} catch (HttpException $ex) {
  echo $ex;
}
```

```python
import requests

url = "https://api.notihub.com//v1/users/string"

headers = {'accept': 'application/json'}

response = requests.request("GET", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/users/string");
var request = new RestRequest(Method.GET);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`GET /v1/users/{userId}`

get

<h3 id="1-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|userId|path|string|true|none|

> Example responses

> default Response

```json
{
  "id": "string",
  "email": "string",
  "phone": "string",
  "firebaseTokens": [
    "string"
  ],
  "createdAt": "2019-07-04T19:08:18Z"
}
```

<h3 id="1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|[ExternalUserDTO](#schemaexternaluserdto)|

<aside class="success">
This operation does not require authentication
</aside>

## 2

<a id="opId2"></a>

> Code samples

```shell
curl --request GET \
  --url https://api.notihub.com//v1/users \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/users",
  "method": "GET",
  "headers": {
    "accept": "application/json"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```java
OkHttpClient client = new OkHttpClient();

Request request = new Request.Builder()
  .url("https://api.notihub.com//v1/users")
  .get()
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/users');
$request->setMethod(HTTP_METH_GET);

$request->setHeaders(array(
  'accept' => 'application/json'
));

try {
  $response = $request->send();

  echo $response->getBody();
} catch (HttpException $ex) {
  echo $ex;
}
```

```python
import requests

url = "https://api.notihub.com//v1/users"

headers = {'accept': 'application/json'}

response = requests.request("GET", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/users");
var request = new RestRequest(Method.GET);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`GET /v1/users`

<h3 id="2-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|none|
|size|query|integer(int32)|false|none|

> Example responses

> default Response

```json
[
  {
    "id": "string",
    "email": "string",
    "phone": "string",
    "firebaseTokens": [
      "string"
    ],
    "createdAt": "2019-07-04T19:08:18Z"
  }
]
```

<h3 id="2-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|Inline|

<h3 id="2-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ExternalUserDTO](#schemaexternaluserdto)]|false|none|none|
|» id|string|false|none|none|
|» email|string|false|none|none|
|» phone|string|false|none|none|
|» firebaseTokens|[string]|false|none|none|
|» createdAt|string(date-time)|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## 3

<a id="opId3"></a>

> Code samples

```shell
curl --request POST \
  --url https://api.notihub.com//v1/users \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/users",
  "method": "POST",
  "headers": {
    "accept": "application/json"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```java
OkHttpClient client = new OkHttpClient();

Request request = new Request.Builder()
  .url("https://api.notihub.com//v1/users")
  .post(null)
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/users');
$request->setMethod(HTTP_METH_POST);

$request->setHeaders(array(
  'accept' => 'application/json'
));

try {
  $response = $request->send();

  echo $response->getBody();
} catch (HttpException $ex) {
  echo $ex;
}
```

```python
import requests

url = "https://api.notihub.com//v1/users"

headers = {'accept': 'application/json'}

response = requests.request("POST", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/users");
var request = new RestRequest(Method.POST);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`POST /v1/users`

> Example responses

> default Response

```json
{
  "id": "string",
  "email": "string",
  "phone": "string",
  "firebaseTokens": [
    "string"
  ],
  "createdAt": "2019-07-04T19:08:18Z"
}
```

<h3 id="3-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|[ExternalUserDTO](#schemaexternaluserdto)|

<aside class="success">
This operation does not require authentication
</aside>

## 4

<a id="opId4"></a>

> Code samples

```shell
curl --request PUT \
  --url https://api.notihub.com//v1/users/string \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/users/string",
  "method": "PUT",
  "headers": {
    "accept": "application/json"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```java
OkHttpClient client = new OkHttpClient();

Request request = new Request.Builder()
  .url("https://api.notihub.com//v1/users/string")
  .put(null)
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/users/string');
$request->setMethod(HTTP_METH_PUT);

$request->setHeaders(array(
  'accept' => 'application/json'
));

try {
  $response = $request->send();

  echo $response->getBody();
} catch (HttpException $ex) {
  echo $ex;
}
```

```python
import requests

url = "https://api.notihub.com//v1/users/string"

headers = {'accept': 'application/json'}

response = requests.request("PUT", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/users/string");
var request = new RestRequest(Method.PUT);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`PUT /v1/users/{userId}`

<h3 id="4-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|userId|path|string|true|none|

> Example responses

> default Response

```json
{
  "id": "string",
  "email": "string",
  "phone": "string",
  "firebaseTokens": [
    "string"
  ],
  "createdAt": "2019-07-04T19:08:18Z"
}
```

<h3 id="4-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|[ExternalUserDTO](#schemaexternaluserdto)|

<aside class="success">
This operation does not require authentication
</aside>

## 5

<a id="opId5"></a>

> Code samples

```shell
curl --request PUT \
  --url https://api.notihub.com//v1/users/string/patch \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/users/string/patch",
  "method": "PUT",
  "headers": {
    "accept": "application/json"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```java
OkHttpClient client = new OkHttpClient();

Request request = new Request.Builder()
  .url("https://api.notihub.com//v1/users/string/patch")
  .put(null)
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/users/string/patch');
$request->setMethod(HTTP_METH_PUT);

$request->setHeaders(array(
  'accept' => 'application/json'
));

try {
  $response = $request->send();

  echo $response->getBody();
} catch (HttpException $ex) {
  echo $ex;
}
```

```python
import requests

url = "https://api.notihub.com//v1/users/string/patch"

headers = {'accept': 'application/json'}

response = requests.request("PUT", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/users/string/patch");
var request = new RestRequest(Method.PUT);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`PUT /v1/users/{userId}/patch`

<h3 id="5-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|userId|path|string|true|none|

> Example responses

> default Response

```json
{
  "id": "string",
  "email": "string",
  "phone": "string",
  "firebaseTokens": [
    "string"
  ],
  "createdAt": "2019-07-04T19:08:18Z"
}
```

<h3 id="5-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|[ExternalUserDTO](#schemaexternaluserdto)|

<aside class="success">
This operation does not require authentication
</aside>

## 6

<a id="opId6"></a>

> Code samples

```shell
curl --request DELETE \
  --url https://api.notihub.com//v1/users/string \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/users/string",
  "method": "DELETE",
  "headers": {
    "accept": "application/json"
  }
}

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

```java
OkHttpClient client = new OkHttpClient();

Request request = new Request.Builder()
  .url("https://api.notihub.com//v1/users/string")
  .delete(null)
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/users/string');
$request->setMethod(HTTP_METH_DELETE);

$request->setHeaders(array(
  'accept' => 'application/json'
));

try {
  $response = $request->send();

  echo $response->getBody();
} catch (HttpException $ex) {
  echo $ex;
}
```

```python
import requests

url = "https://api.notihub.com//v1/users/string"

headers = {'accept': 'application/json'}

response = requests.request("DELETE", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/users/string");
var request = new RestRequest(Method.DELETE);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`DELETE /v1/users/{userId}`

<h3 id="6-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|userId|path|string|true|none|

> Example responses

<h3 id="6-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|None|

<h3 id="6-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocSexternaluserdto">ExternalUserDTO</h2>

<a id="schemaexternaluserdto"></a>

```json
{
  "id": "string",
  "email": "string",
  "phone": "string",
  "firebaseTokens": [
    "string"
  ],
  "createdAt": "2019-07-04T19:08:18Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|
|email|string|false|none|none|
|phone|string|false|none|none|
|firebaseTokens|[string]|false|none|none|
|createdAt|string(date-time)|false|none|none|

<h2 id="tocSexternaluserinputdto">ExternalUserInputDTO</h2>

<a id="schemaexternaluserinputdto"></a>

```json
{
  "email": "string",
  "phone": "string",
  "firebaseTokens": [
    "string"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|false|none|none|
|phone|string|false|none|none|
|firebaseTokens|[string]|false|none|none|

