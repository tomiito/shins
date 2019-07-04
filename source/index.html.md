---
title: Awesome Title
language_tabs:
  - shell: HTTP
  - javascript: JavaScript
  - java: Java
  - node: NodeJS
  - php: PHP
  - csharp: 'C#'
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="awesome-title">Awesome Title v0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

My API

Base URLs:

* <a href="https://api.notihub.com">https://api.notihub.com</a>

<h1 id="awesome-title-users">Users</h1>

## getUsers

<a id="opIdgetUsers"></a>

> Code samples

```shell
curl --request GET \
  --url https://api.notihub.com/v1/users \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com/v1/users",
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
  .url("https://api.notihub.com/v1/users")
  .get()
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```node
var unirest = require("unirest");

var req = unirest("GET", "https://api.notihub.com/v1/users");

req.headers({
  "accept": "application/json"
});

req.end(function (res) {
  if (res.error) throw new Error(res.error);

  console.log(res.body);
});

```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com/v1/users');
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

```csharp
var client = new RestClient("https://api.notihub.com/v1/users");
var request = new RestRequest(Method.GET);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`GET /v1/users`

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
    ]
  }
]
```

<h3 id="getusers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|Inline|

<h3 id="getusers-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ExternalUserDTO](#schemaexternaluserdto)]|false|none|none|
|» id|string|false|none|none|
|» email|string|false|none|none|
|» phone|string|false|none|none|
|» firebaseTokens|[string]|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## getAllUsers

<a id="opIdgetAllUsers"></a>

> Code samples

```shell
curl --request GET \
  --url https://api.notihub.com/v1/users/all \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com/v1/users/all",
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
  .url("https://api.notihub.com/v1/users/all")
  .get()
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```node
var unirest = require("unirest");

var req = unirest("GET", "https://api.notihub.com/v1/users/all");

req.headers({
  "accept": "application/json"
});

req.end(function (res) {
  if (res.error) throw new Error(res.error);

  console.log(res.body);
});

```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com/v1/users/all');
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

```csharp
var client = new RestClient("https://api.notihub.com/v1/users/all");
var request = new RestRequest(Method.GET);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`GET /v1/users/all`

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
    ]
  }
]
```

<h3 id="getallusers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|Inline|

<h3 id="getallusers-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[ExternalUserDTO](#schemaexternaluserdto)]|false|none|none|
|» id|string|false|none|none|
|» email|string|false|none|none|
|» phone|string|false|none|none|
|» firebaseTokens|[string]|false|none|none|

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
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|
|email|string|false|none|none|
|phone|string|false|none|none|
|firebaseTokens|[string]|false|none|none|

