### POST /api/register
- Request Body
```json
{
  "username": "johndoe",
  "password": "password123",
  "email": "johndoe@example.com"
}
```

- Response Success (201 Created)
```json
{
  "statusCode": 201,
  "message": "User registered successfully."
}
```

- Response Failure (409 Conflict - Username already exists)
```json
{
  "statusCode": 409,
  "error": "Username already exists."
}
```

### POST /api/login
- Request Body
```json
{
  "username": "johndoe",
  "password": "password123"
}
```

- Response Success (200 OK)
```json
{
  "statusCode": 200,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```

- Response Failure (401 Unauthorized - Invalid credentials)
```json
{
  "statusCode": 401,
  "error": "Invalid username or password."
}
```

### POST /api/logout
- Response Success (200 OK)
```json
{
  "statusCode": 200,
  "message": "User logged out successfully."
}
```