# Awesome REST API example

This is an example of some REST API

# Running in development

```
git clone https://github.com/pshvets/REST-API.git
cd REST-API/
./gradlew bootRun
```

To check if up and running

```curl -X GET http://localhost:8080/actuator/health```

```{"status":"UP"}```

# Base Path
```
http://localhost:8080/api/v1/users
```

# Methods
## Create User
```
POST /createUser
```
```
{
  "name": "your_name",
  "email": "your_email"
}
```
 Response Example

```
{
  "id": "some_id",
  "name": "your_name",
  "email": "your_email"
}
```

## Get User

```
GET /getUser/{some_id}
```
 Response Example

```
{
  "id": "some_id",
  "name": "your_name",
  "email": "your_email"
}
```
## Get List of Users

```
GET /getUsers
```
 Response Example

```
[
  {
    "id": "some_id",
    "name": "your_name",
    "email": "your_email"
  },
  {
    "id": "some_id",
    "name": "your_name",
    "email": "your_email"
  }
]
```
## Delete User
```
GET /{some_id}/delete
```
 Response Example

```
200 OK
```
## Update User
```
POST /{some_id}/update
```
```
{
  "name": "your_new_name",
  "email": "your_new_email"
}
```
 Response Example

```
{
  "id": "some_id",
  "name": "your_new_name",
  "email": "your_new_email"
}
```