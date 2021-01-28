---
title: Agency Incoming API v1.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="agency-incoming-api">Agency Incoming API v1.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

API spec for agencies to process incoming requests from Freede.

Base URLs:

# Authentication

<h1 id="agency-incoming-api-accounts">Accounts</h1>

## get-account

<a id="opIdget-account"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /account/{accountNum} \
  -H 'Accept: application/json' \
  -H 'Freede-Verification-Key: string' \
  -H 'Freede-API-Version: string' \
  -H 'Freede-Verification-Token: string'

```

```http
GET /account/{accountNum} HTTP/1.1

Accept: application/json
Freede-Verification-Key: string
Freede-API-Version: string
Freede-Verification-Token: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Freede-Verification-Key':'string',
  'Freede-API-Version':'string',
  'Freede-Verification-Token':'string'
};

fetch('/account/{accountNum}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Freede-Verification-Key' => 'string',
  'Freede-API-Version' => 'string',
  'Freede-Verification-Token' => 'string'
}

result = RestClient.get '/account/{accountNum}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Freede-Verification-Key': 'string',
  'Freede-API-Version': 'string',
  'Freede-Verification-Token': 'string'
}

r = requests.get('/account/{accountNum}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Freede-Verification-Key' => 'string',
    'Freede-API-Version' => 'string',
    'Freede-Verification-Token' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/account/{accountNum}', array(
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

```java
URL obj = new URL("/account/{accountNum}");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Freede-Verification-Key": []string{"string"},
        "Freede-API-Version": []string{"string"},
        "Freede-Verification-Token": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/account/{accountNum}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /account/{accountNum}`

*Get account details*

Endpoint to get the account details from the agency

<h3 id="get-account-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Freede-Verification-Key|header|string|false|SHA256 Hash of Token and API key|
|Freede-API-Version|header|string|false|Freede Agency Incoming API Version|
|Freede-Verification-Token|header|string|false|Token Salt|
|accountNum|path|string|true|Agency account number|

> Example responses

<h3 id="get-account-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|No Content|None|

<h3 id="get-account-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="agency-incoming-api-consumers">Consumers</h1>

## put-consumer-consumerRef

<a id="opIdput-consumer-consumerRef"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /consumer/{consumerRef} \
  -H 'Content-Type: application/json' \
  -H 'Freede-Verification-Key: string' \
  -H 'Freede-API-Version: string' \
  -H 'Freede-Verification-Token: string'

```

```http
PUT /consumer/{consumerRef} HTTP/1.1

Content-Type: application/json

Freede-Verification-Key: string
Freede-API-Version: string
Freede-Verification-Token: string

```

```javascript
const inputBody = 'false';
const headers = {
  'Content-Type':'application/json',
  'Freede-Verification-Key':'string',
  'Freede-API-Version':'string',
  'Freede-Verification-Token':'string'
};

fetch('/consumer/{consumerRef}',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Freede-Verification-Key' => 'string',
  'Freede-API-Version' => 'string',
  'Freede-Verification-Token' => 'string'
}

result = RestClient.put '/consumer/{consumerRef}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Freede-Verification-Key': 'string',
  'Freede-API-Version': 'string',
  'Freede-Verification-Token': 'string'
}

r = requests.put('/consumer/{consumerRef}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Freede-Verification-Key' => 'string',
    'Freede-API-Version' => 'string',
    'Freede-Verification-Token' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/consumer/{consumerRef}', array(
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

```java
URL obj = new URL("/consumer/{consumerRef}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Freede-Verification-Key": []string{"string"},
        "Freede-API-Version": []string{"string"},
        "Freede-Verification-Token": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/consumer/{consumerRef}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /consumer/{consumerRef}`

*Update consumer demographics*

Endpoint to receive updated consumer demographics

> Body parameter

```json
false
```

<h3 id="put-consumer-consumerref-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Freede-Verification-Key|header|string|false|SHA256 Hash of Token and API key|
|Freede-API-Version|header|string|false|Freede Agency Incoming API Version|
|Freede-Verification-Token|header|string|false|Token Salt|
|consumerRef|path|string|true|none|

<h3 id="put-consumer-consumerref-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

## delete-consumer-consumerRef

<a id="opIddelete-consumer-consumerRef"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /consumer/{consumerRef} \
  -H 'Freede-Verification-Key: string' \
  -H 'Freede-API-Version: string' \
  -H 'Freede-Verification-Token: string'

```

```http
DELETE /consumer/{consumerRef} HTTP/1.1

Freede-Verification-Key: string
Freede-API-Version: string
Freede-Verification-Token: string

```

```javascript

const headers = {
  'Freede-Verification-Key':'string',
  'Freede-API-Version':'string',
  'Freede-Verification-Token':'string'
};

fetch('/consumer/{consumerRef}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Freede-Verification-Key' => 'string',
  'Freede-API-Version' => 'string',
  'Freede-Verification-Token' => 'string'
}

result = RestClient.delete '/consumer/{consumerRef}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Freede-Verification-Key': 'string',
  'Freede-API-Version': 'string',
  'Freede-Verification-Token': 'string'
}

r = requests.delete('/consumer/{consumerRef}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Freede-Verification-Key' => 'string',
    'Freede-API-Version' => 'string',
    'Freede-Verification-Token' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/consumer/{consumerRef}', array(
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

```java
URL obj = new URL("/consumer/{consumerRef}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Freede-Verification-Key": []string{"string"},
        "Freede-API-Version": []string{"string"},
        "Freede-Verification-Token": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/consumer/{consumerRef}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /consumer/{consumerRef}`

*Deregister consumer*

Endpoint to deregister consumer from Freede

<h3 id="delete-consumer-consumerref-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Freede-Verification-Key|header|string|false|SHA256 Hash of Token and API key|
|Freede-API-Version|header|string|false|Freede Agency Incoming API Version|
|Freede-Verification-Token|header|string|false|Token Salt|
|consumerRef|path|string|true|none|

<h3 id="delete-consumer-consumerref-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

## put-consumer-consumerRef-optins

<a id="opIdput-consumer-consumerRef-optins"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT /consumer/{consumerRef}/optins \
  -H 'Content-Type: application/json' \
  -H 'Freede-Verification-Key: string' \
  -H 'Freede-API-Version: string' \
  -H 'Freede-Verification-Token: string'

```

```http
PUT /consumer/{consumerRef}/optins HTTP/1.1

Content-Type: application/json

Freede-Verification-Key: string
Freede-API-Version: string
Freede-Verification-Token: string

```

```javascript
const inputBody = 'false';
const headers = {
  'Content-Type':'application/json',
  'Freede-Verification-Key':'string',
  'Freede-API-Version':'string',
  'Freede-Verification-Token':'string'
};

fetch('/consumer/{consumerRef}/optins',
{
  method: 'PUT',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Freede-Verification-Key' => 'string',
  'Freede-API-Version' => 'string',
  'Freede-Verification-Token' => 'string'
}

result = RestClient.put '/consumer/{consumerRef}/optins',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Freede-Verification-Key': 'string',
  'Freede-API-Version': 'string',
  'Freede-Verification-Token': 'string'
}

r = requests.put('/consumer/{consumerRef}/optins', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Freede-Verification-Key' => 'string',
    'Freede-API-Version' => 'string',
    'Freede-Verification-Token' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('PUT','/consumer/{consumerRef}/optins', array(
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

```java
URL obj = new URL("/consumer/{consumerRef}/optins");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Freede-Verification-Key": []string{"string"},
        "Freede-API-Version": []string{"string"},
        "Freede-Verification-Token": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "/consumer/{consumerRef}/optins", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /consumer/{consumerRef}/optins`

*Update consumer optins*

Endpoint to receive updated consumer optins

> Body parameter

```json
false
```

<h3 id="put-consumer-consumerref-optins-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Freede-Verification-Key|header|string|false|SHA256 Hash of Token and API key|
|Freede-API-Version|header|string|false|Freede Agency Incoming API Version|
|Freede-Verification-Token|header|string|false|Token Salt|
|consumerRef|path|string|true|Agency consumer reference|

<h3 id="put-consumer-consumerref-optins-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

## post-consumer-consumerRef-conversation

<a id="opIdpost-consumer-consumerRef-conversation"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /consumer/{consumerRef}/conversation \
  -H 'Content-Type: application/json' \
  -H 'Freede-Verification-Key: string' \
  -H 'Freede-API-Version: string' \
  -H 'Freede-Verification-Token: string'

```

```http
POST /consumer/{consumerRef}/conversation HTTP/1.1

Content-Type: application/json

Freede-Verification-Key: string
Freede-API-Version: string
Freede-Verification-Token: string

```

```javascript
const inputBody = 'false';
const headers = {
  'Content-Type':'application/json',
  'Freede-Verification-Key':'string',
  'Freede-API-Version':'string',
  'Freede-Verification-Token':'string'
};

fetch('/consumer/{consumerRef}/conversation',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Freede-Verification-Key' => 'string',
  'Freede-API-Version' => 'string',
  'Freede-Verification-Token' => 'string'
}

result = RestClient.post '/consumer/{consumerRef}/conversation',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Freede-Verification-Key': 'string',
  'Freede-API-Version': 'string',
  'Freede-Verification-Token': 'string'
}

r = requests.post('/consumer/{consumerRef}/conversation', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Freede-Verification-Key' => 'string',
    'Freede-API-Version' => 'string',
    'Freede-Verification-Token' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/consumer/{consumerRef}/conversation', array(
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

```java
URL obj = new URL("/consumer/{consumerRef}/conversation");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Freede-Verification-Key": []string{"string"},
        "Freede-API-Version": []string{"string"},
        "Freede-Verification-Token": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/consumer/{consumerRef}/conversation", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /consumer/{consumerRef}/conversation`

*Consumer conversation*

Endpoint to receive notice of consumer conversation. Can use Id to retrieve conversation details from Agency API

> Body parameter

```json
false
```

<h3 id="post-consumer-consumerref-conversation-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Freede-Verification-Key|header|string|false|SHA256 Hash of Token and API key|
|Freede-API-Version|header|string|false|Freede Agency Incoming API Version|
|Freede-Verification-Token|header|string|false|Token Salt|
|consumerRef|path|string|true|none|

<h3 id="post-consumer-consumerref-conversation-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="agency-incoming-api-forms">Forms</h1>

## post-forms

<a id="opIdpost-forms"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /forms \
  -H 'Content-Type: application/json' \
  -H 'Freede-Verification-Key: string' \
  -H 'Freede-API-Version: string' \
  -H 'Freede-Verification-Token: string'

```

```http
POST /forms HTTP/1.1

Content-Type: application/json

Freede-Verification-Key: string
Freede-API-Version: string
Freede-Verification-Token: string

```

```javascript
const inputBody = '{
  "type": "dispute",
  "form": null
}';
const headers = {
  'Content-Type':'application/json',
  'Freede-Verification-Key':'string',
  'Freede-API-Version':'string',
  'Freede-Verification-Token':'string'
};

fetch('/forms',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Freede-Verification-Key' => 'string',
  'Freede-API-Version' => 'string',
  'Freede-Verification-Token' => 'string'
}

result = RestClient.post '/forms',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Freede-Verification-Key': 'string',
  'Freede-API-Version': 'string',
  'Freede-Verification-Token': 'string'
}

r = requests.post('/forms', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Freede-Verification-Key' => 'string',
    'Freede-API-Version' => 'string',
    'Freede-Verification-Token' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/forms', array(
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

```java
URL obj = new URL("/forms");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Freede-Verification-Key": []string{"string"},
        "Freede-API-Version": []string{"string"},
        "Freede-Verification-Token": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/forms", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /forms`

*Consumer submitted form*

Endpoint to receive forms consumer has submitted

> Body parameter

```json
{
  "type": "dispute",
  "form": null
}
```

<h3 id="post-forms-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Freede-Verification-Key|header|string|false|SHA256 Hash of Token and API key|
|Freede-API-Version|header|string|false|Freede Agency Incoming API Version|
|Freede-Verification-Token|header|string|false|Token Salt|
|body|body|object|false|none|
|» type|body|string|false|none|
|» form|body|any|false|none|
|»» *anonymous*|body|any|false|none|
|»» *anonymous*|body|any|false|none|
|»» *anonymous*|body|any|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» type|dispute|
|» type|attorney|
|» type|bankruptcy|

<h3 id="post-forms-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="agency-incoming-api-registration">Registration</h1>

## post-registration

<a id="opIdpost-registration"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /registration \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Freede-Verification-Key: string' \
  -H 'Freede-API-Version: string' \
  -H 'Freede-Verification-Token: string'

```

```http
POST /registration HTTP/1.1

Content-Type: application/json
Accept: application/json
Freede-Verification-Key: string
Freede-API-Version: string
Freede-Verification-Token: string

```

```javascript
const inputBody = '{
  "first": "string",
  "last": "string",
  "address": "string",
  "address2": "string",
  "city": "string",
  "state": "string",
  "zip": "string",
  "phone": "string",
  "email": "user@example.com",
  "regcode": "string",
  "verify": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Freede-Verification-Key':'string',
  'Freede-API-Version':'string',
  'Freede-Verification-Token':'string'
};

fetch('/registration',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Freede-Verification-Key' => 'string',
  'Freede-API-Version' => 'string',
  'Freede-Verification-Token' => 'string'
}

result = RestClient.post '/registration',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Freede-Verification-Key': 'string',
  'Freede-API-Version': 'string',
  'Freede-Verification-Token': 'string'
}

r = requests.post('/registration', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Freede-Verification-Key' => 'string',
    'Freede-API-Version' => 'string',
    'Freede-Verification-Token' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/registration', array(
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

```java
URL obj = new URL("/registration");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
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

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Freede-Verification-Key": []string{"string"},
        "Freede-API-Version": []string{"string"},
        "Freede-Verification-Token": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/registration", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /registration`

*Register consumer*

Freede will submit this POST request when a consumer is attempting to register with the agency. Agency may perform their own validation checks and return a response.

> Body parameter

```json
{
  "first": "string",
  "last": "string",
  "address": "string",
  "address2": "string",
  "city": "string",
  "state": "string",
  "zip": "string",
  "phone": "string",
  "email": "user@example.com",
  "regcode": "string",
  "verify": true
}
```

<h3 id="post-registration-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Freede-Verification-Key|header|string|false|SHA256 Hash of Token and API key|
|Freede-API-Version|header|string|false|Freede Agency Incoming API Version|
|Freede-Verification-Token|header|string|false|Token Salt|
|body|body|object|false|Consumer registration information|
|» first|body|string|false|none|
|» last|body|string|false|none|
|» address|body|string|false|none|
|» address2|body|string|false|none|
|» city|body|string|false|none|
|» state|body|string|false|none|
|» zip|body|string|false|none|
|» phone|body|string|false|none|
|» email|body|string(email)|false|none|
|» regcode|body|string|true|none|
|» verify|body|boolean|true|none|

> Example responses

> 200 Response

```json
[]
```

<h3 id="post-registration-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Unauthorized|None|

<h3 id="post-registration-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» *anonymous*|any|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

