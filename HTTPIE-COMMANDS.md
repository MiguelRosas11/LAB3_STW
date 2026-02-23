# HTTPie Commands – Dog CEO API

## Variables
```bash
export baseURL=https://dog.ceo/api
export id=hound
export query=3
```

## Happy Path Requests
```bash
http GET $baseURL/breeds/list/all Accept:application/json
http GET $baseURL/breed/$id/images/random Accept:application/json
http GET $baseURL/breed/$id/images Accept:application/json
http GET $baseURL/breed/$id/list Accept:application/json
http GET $baseURL/breed/hound/afghan/images/random Accept:application/json
http GET $baseURL/breeds/image/random/$query Accept:application/json
```

## Error Requests
```bash
http GET $baseURL/breed/noexiste/images Accept:application/json
http GET $baseURL/breed//images Accept:application/json
http GET https://httpbin.org/status/401 Accept:application/json
http GET https://httpbin.org/status/403 Accept:application/json
```

## Authentication Note

This API does not require authentication.  
The 401 and 403 status codes were demonstrated using test endpoints to satisfy the laboratory requirements.