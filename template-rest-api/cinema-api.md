### GET /api/cinemas
- Response Success (200 OK)
```json
{
  "statusCode": 200,
  "data": [
    { "id": "1", "name": "Cinema XXI", "location": "Jakarta" },
    { "id": "2", "name": "Cinema CGV", "location": "Bandung" }
  ]
}
```

### GET /api/cinemas/{cinemaId}
- Response Success (200 OK)
```json
{
  "statusCode": 200,
  "data": {
    "id": "1",
    "name": "Cinema XXI",
    "location": "Jakarta",
    "seats": 100
  }
}
```

- Response Failure (404 Not Found - Cinema not found)
```json
{
  "statusCode": 404,
  "message": "Cinema not found."
}
```