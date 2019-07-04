---
title: Awesome Title
language_tabs:
  - shell: curl
  - node: NodeJS
  - java: Java
toc_footers: []
includes: []
search: false
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

```node
var http = require("https");

var options = {
  "method": "GET",
  "hostname": "api.notihub.com",
  "port": null,
  "path": "/v1/users",
  "headers": {
    "accept": "application/json"
  }
};

var req = http.request(options, function (res) {
  var chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    var body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.end();
```

```java
HttpResponse<String> response = Unirest.get("https://api.notihub.com/v1/users")
  .header("accept", "application/json")
  .asString();
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

```node
var http = require("https");

var options = {
  "method": "GET",
  "hostname": "api.notihub.com",
  "port": null,
  "path": "/v1/users/all",
  "headers": {
    "accept": "application/json"
  }
};

var req = http.request(options, function (res) {
  var chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    var body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.end();
```

```java
HttpResponse<String> response = Unirest.get("https://api.notihub.com/v1/users/all")
  .header("accept", "application/json")
  .asString();
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

