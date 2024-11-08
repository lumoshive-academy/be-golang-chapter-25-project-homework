### GET /api/cinemas/{cinemaId}/seats?date={date}&time={time}
- Response Success (200 OK)
```json
{
  "statusCode": 200,
  "data": [
    { "seatId": "A1", "status": "available" },
    { "seatId": "A2", "status": "available" },
    { "seatId": "A3", "status": "booked" }
  ]
}
```

- Response Failure (404 Not Found - Cinema or schedule not found)
```json
{
  "statusCode": 404,
  "message": "No available seats found for the specified cinema and schedule."
}
```