---
title: Awesome Title
language_tabs:
  - http: http
  - node: node
  - java: java
  - php: php
  - ruby: ruby
  - python: python
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

```http
GET https://api.notihub.com/v1/users HTTP/1.1
Host: api.notihub.com
Accept: application/json

```

```java
URL obj = new URL("https://api.notihub.com/v1/users");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.notihub.com/v1/users', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.notihub.com/v1/users',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.notihub.com/v1/users', params={

}, headers = headers)

print r.json()

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

```http
GET https://api.notihub.com/v1/users/all HTTP/1.1
Host: api.notihub.com
Accept: application/json

```

```java
URL obj = new URL("https://api.notihub.com/v1/users/all");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    
    );

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.notihub.com/v1/users/all', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'https://api.notihub.com/v1/users/all',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.notihub.com/v1/users/all', params={

}, headers = headers)

print r.json()

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

