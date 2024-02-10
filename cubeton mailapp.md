# Getting started with Api



### Send Email

Send an email using the Cubeton Mailapp API.

**Endpoint**: [https://mailapp.cubeton.cloud/api](https://mailapp.cubeton.cloud/api)

**HTTP Method**: `POST`

**Headers**:

- `Content-Type: application/json`
- `Authorization: Bearer <your auth token from dashboard>`

**Request Body**:

```javascript
{
  "mail": "where to send the mail - address",
  "subject": "Hi",
  "body": "Hello",
  "enableAds": false
}
```

- `mail` (string, required): The email address where the mail should be sent to.
- `subject` (string, required) subject of the email. 
- `body` (string, optional): The body/content of the email. HTML supported.
- `enableAds` (boolean, optional): Whether to enable ads in the email. Default value is false - costs 1 credits to send email without ads, otherwise 0.5 credits with ads.
- `template` (object, optional): see the docs page for template.

**Example 1 (using curl)** :

```sh
curl -X POST -H "Content-Type: application/json" -H "Authorization: Bearer <your auth token from dashboard>" -d '{"mail":"receiver email", "subject:": "Subject of email", "body": "body of email, HTML supported", "enableAds": true}' https://mailapp.cubeton.cloud/api
```

**Example 2 (python) :**

```python
import requests

url = 'https://mailapp.cubeton.cloud/api'
headers = {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer ABCDEFGHIK-d'
}
data = {
    'mail': 'where to send the mail - address',
    'subject': 'Hi',
    'body': 'Hello',
    'enableAds': False
}

response = requests.post(url, json=data, headers=headers)

if response.status_code == 200:
    print('Response:', response.json())
else:
    print('Error:', response.json())
 
```

**Example 3 (BJS) :** 

```javascript
HTTP.post({
  url: "https://mailapp.cubeton.cloud/api",
  success: '/onLoading',
  body: {
    mail: "where to send the mail - address",
    subject: "Hi",
    body: "Hello",
    enableAds: false
  },
  headers: {
    "Content-Type": "application/json",
    "Authorization": "Bearer <Your auth token from dashboard>"
  }
})
```

**Example 4 (RUBY)**:

```ruby
require 'net/http'
require 'uri'
require 'json'

uri = URI.parse("https://mailapp.cubeton.cloud/api")
http = Net::HTTP.new(uri.host, uri.port)
http.use_ssl = true

headers = {
  'Content-Type': 'application/json',
  'Authorization': 'Bearer ABCDEFGHIK'
}

data = {
  mail: "where to send the mail - address",
  subject: "Hi",
  body: "Hello",
  enableAds: false
}

response = http.post(uri.path, data.to_json, headers)
puts response.body
```

**Example 5 (PHP):**

```php
<?php
$url = 'https://mailapp.cubeton.cloud/api';
$data = array(
    'mail' => 'where to send the mail - address',
    'subject' => 'Hi',
    'body' => 'Hello',
    'enableAds' => false
);
$options = array(
    'http' => array(
        'header'  => "Content-Type: application/json\r\n" .
                     "Authorization: Bearer ABCDEFGHIK-d\r\n",
        'method'  => 'POST',
        'content' => json_encode($data),
    ),
);
$context  = stream_context_create($options);
$result = file_get_contents($url, false, $context);
if ($result === FALSE) { 
    /* Handle error */
}
var_dump($result);
?>
```

**Example 6 (Java):**

```java
import java.net.HttpURLConnection;
import java.net.URL;
import java.io.OutputStream;
import java.io.BufferedReader;
import java.io.InputStreamReader;

public class Main {
    public static void main(String[] args) {
        try {
            URL url = new URL("https://mailapp.cubeton.cloud/api");
            HttpURLConnection conn = (HttpURLConnection) url.openConnection();
            conn.setRequestMethod("POST");
            conn.setRequestProperty("Content-Type", "application/json");
            conn.setRequestProperty("Authorization", "Bearer ABCDEFGHIK-d");
            conn.setDoOutput(true);

            String jsonInputString = "{\"mail\":\"where to send the mail - address\",\"subject\":\"Hi\",\"body\":\"Hello\",\"enableAds\":false}";

            try(OutputStream os = conn.getOutputStream()) {
                byte[] input = jsonInputString.getBytes("utf-8");
                os.write(input, 0, input.length);
            }

            try(BufferedReader br = new BufferedReader(
                    new InputStreamReader(conn.getInputStream(), "utf-8"))) {
                StringBuilder response = new StringBuilder();
                String responseLine = null;
                while ((responseLine = br.readLine()) != null) {
                    response.append(responseLine.trim());
                }
                System.out.println(response.toString());
            }

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

**Example 7 (node.js)** :

```javascript
const axios = require('axios');

const data = {
  mail: "where to send the mail - address",
  subject: "Hi",
  body: "Hello",
  enableAds: false
};

const config = {
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer ABCDEFGHIK-d'
  }
};

axios.post('https://mailapp.cubeton.cloud/api', data, config)
  .then(response => {
    console.log('Response:', response.data);
  })
  .catch(error => {
    console.error('Error:', error.response.data);
  });
```
