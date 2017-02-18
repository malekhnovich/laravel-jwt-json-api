# About

A simple yet efficient Laravel + JWT API which responds according to [jsonapi.org](http://jsonapi.org/) standards.

# Dependencies
```
"php": ">=5.6.4",
"laravel/framework": "5.4.*",
"tymon/jwt-auth": "^0.5.9"
```

# Installation
---

1. (Optional) Install Docker + docker-compose and run `docker-compose up`

2. Configure your .env appropriately for your environment

3. You can find all routes in `routes.php` and send all API requests to `http://localhost:8081/api/`

# Default routes
---

POST `http://localhost:8081/api/user/register`
```
{
  "data": {
    "type": "register",
    "attributes": {
      "name": "John Smith",
      "email": "john.smith@gmail.com",
      "password": "yourpassword"
    }
  }
}
```

POST `http://localhost:8081/api/user/login`
```
{
  "data": {
    "type": "authenticate",
    "attributes": {
      "email": "john.smith@gmail.com",
      "password": "yourpassword"
    }
  }
}
```

GET `http://localhost:8081/api/me`
```
{
  "data": [{
    "type": "user",
    "attributes": {
      "id": 1,
      "name": "Jean-Pierre",
      "email": "jeanpierre.gassin@gmail.com",
      "created_at": "2017-01-11 12:35:05",
      "updated_at": "2017-01-11 12:35:05"
    }
  }]
}
```
