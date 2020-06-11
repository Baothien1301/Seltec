# API OPENHAB MOBILE APP
## I. ADD NEW DEVICE
### 1. Diagram
![Diagram](/addnewdevicediagram.png)
### 2. Detail
#### a. Get: supported binding
* **Response Class:** (Status 200)

* **Response Content Type:** application/json

* **Parameters:** 

    |Parameter|Value|Decription|Parameter Type|Data Type|
    |---------|-----|----------|--------------|---------|
    |Accept-Language||language |    header    |  string |

* **Curl:** 

    ```curl -X GET --header "Accept: application/json" "http://<ip>:8080/rest/bindings"```

* **Request URL:**

    ```http://<ip>:8080/rest/bindings```

* **Response Body:**

    ```
        [{
        "author": "Zachariah",
        "description": "This is the binding for HIKVISION.",
        "id": "hikvision",
        "name": "HIKVISION Binding"
        },
        {
        "author": "Select Technology Company",
        "description": "This is the binding for LifeSmart.",
        "id": "lifesmart",
        "name": "LifeSmart Binding"
        }]
    ```

* **Response Code:** 

    ```200```

* **Response Headers:**

    ```
    {
    "content-length": "380",
    "content-type": "application/json",
    "server": "Jetty(9.4.20.v20190813)"
    }
    ```
    
#### b. POST: Scan with {bindingID}
* **Response Class:** (Status 200)

* **Response Content Type:** text/plain

* **Parameters:** 

    |Parameter|Value|Decription|Parameter Type|Data Type|
    |---------|-----|----------|--------------|---------|
    |bindingId|lifesmart|language|    header  |  string |

* **Curl:** 

    ```curl -X POST --header "Content-Type: application/json" --header "Accept: text/plain" "http://<ip>:8080/rest/discovery/bindings/{bindingId}/scan"```

* **Request URL:**

    ```http://<ip>:8080/rest/discovery/bindings/{bindingId}/scan```

* **Response Body:**

    ```120```

* **Response Code:** 

    ```200```

* **Response Headers:**

    ```
    {
    "access-control-allow-origin": "http://192.168.100.47:8080",
    "content-length": "3",
    "content-type": "text/plain",
    "server": "Jetty(9.4.20.v20190813)"
    }
    ```


