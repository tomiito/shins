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

<h1 id="api-docs-customers">Customers</h1>

## Search Customers

<a id="opIdgetUsers"></a>

> Code samples

```shell
curl --request GET \
  --url https://api.notihub.com//v1/customers/search \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/customers/search",
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
  .url("https://api.notihub.com//v1/customers/search")
  .get()
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/customers/search');
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

url = "https://api.notihub.com//v1/customers/search"

headers = {'accept': 'application/json'}

response = requests.request("GET", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/customers/search");
var request = new RestRequest(Method.GET);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`GET /v1/customers/search`

<h3 id="search-customers-parameters">Parameters</h3>

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
    "createdAt": "2019-07-10T17:48:17Z"
  }
]
```

<h3 id="search-customers-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|Inline|

<h3 id="search-customers-responseschema">Response Schema</h3>

Status Code **default**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[Customer](#schemacustomer)]|false|none|none|
|» id|string|false|none|none|
|» email|string|false|none|none|
|» phone|string|false|none|none|
|» firebaseTokens|[string]|false|none|none|
|» createdAt|string(date-time)|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## Get Customer

<a id="opIdget"></a>

> Code samples

```shell
curl --request GET \
  --url https://api.notihub.com//v1/customers/string \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/customers/string",
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
  .url("https://api.notihub.com//v1/customers/string")
  .get()
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/customers/string');
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

url = "https://api.notihub.com//v1/customers/string"

headers = {'accept': 'application/json'}

response = requests.request("GET", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/customers/string");
var request = new RestRequest(Method.GET);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`GET /v1/customers/{customerId}`

<h3 id="get-customer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|customerId|path|string|true|none|

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
  "createdAt": "2019-07-10T17:48:17Z"
}
```

<h3 id="get-customer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|[Customer](#schemacustomer)|

<aside class="success">
This operation does not require authentication
</aside>

## Update Customer

<a id="opIdupdate"></a>

> Code samples

```shell
curl --request PUT \
  --url https://api.notihub.com//v1/customers/string \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/customers/string",
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
  .url("https://api.notihub.com//v1/customers/string")
  .put(null)
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/customers/string');
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

url = "https://api.notihub.com//v1/customers/string"

headers = {'accept': 'application/json'}

response = requests.request("PUT", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/customers/string");
var request = new RestRequest(Method.PUT);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`PUT /v1/customers/{customerId}`

<h3 id="update-customer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|customerId|path|string|true|none|

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
  "createdAt": "2019-07-10T17:48:17Z"
}
```

<h3 id="update-customer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|[Customer](#schemacustomer)|

<aside class="success">
This operation does not require authentication
</aside>

## Delete Customer

<a id="opIddelete"></a>

> Code samples

```shell
curl --request DELETE \
  --url https://api.notihub.com//v1/customers/string \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/customers/string",
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
  .url("https://api.notihub.com//v1/customers/string")
  .delete(null)
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/customers/string');
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

url = "https://api.notihub.com//v1/customers/string"

headers = {'accept': 'application/json'}

response = requests.request("DELETE", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/customers/string");
var request = new RestRequest(Method.DELETE);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`DELETE /v1/customers/{customerId}`

<h3 id="delete-customer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|customerId|path|string|true|none|

> Example responses

<h3 id="delete-customer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|None|

<h3 id="delete-customer-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## Create Customer

<a id="opIdpost"></a>

> Code samples

```shell
curl --request POST \
  --url https://api.notihub.com//v1/customers/create \
  --header 'accept: application/json'
```

```javascript
var settings = {
  "async": true,
  "crossDomain": true,
  "url": "https://api.notihub.com//v1/customers/create",
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
  .url("https://api.notihub.com//v1/customers/create")
  .post(null)
  .addHeader("accept", "application/json")
  .build();

Response response = client.newCall(request).execute();
```

```php
<?php

$request = new HttpRequest();
$request->setUrl('https://api.notihub.com//v1/customers/create');
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

url = "https://api.notihub.com//v1/customers/create"

headers = {'accept': 'application/json'}

response = requests.request("POST", url, headers=headers)

print(response.text)
```

```csharp
var client = new RestClient("https://api.notihub.com//v1/customers/create");
var request = new RestRequest(Method.POST);
request.AddHeader("accept", "application/json");
IRestResponse response = client.Execute(request);
```

`POST /v1/customers/create`

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
  "createdAt": "2019-07-10T17:48:17Z"
}
```

<h3 id="create-customer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|default|Default|default response|[Customer](#schemacustomer)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocScustomer">Customer</h2>

<a id="schemacustomer"></a>

```json
{
  "id": "string",
  "email": "string",
  "phone": "string",
  "firebaseTokens": [
    "string"
  ],
  "createdAt": "2019-07-10T17:48:17Z"
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

<h2 id="tocScustomerinput">CustomerInput</h2>

<a id="schemacustomerinput"></a>

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

