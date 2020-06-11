# API OPENHAB MOBILE APP
## I. ADD NEW DEVICE
### 1. Diagram
![Diagram](/addnewdevicediagram.png)
### 2. Detail
#### a. Get: supported binding
**Response Class:** (Status 200)
**Response Content Type:** application/json
**Curl:** 
```curl -X GET --header "Accept: application/json" "http://192.168.100.47:8080/rest/bindings"```
**Request URL:**
```http://<ip>:8080/rest/bindings```
