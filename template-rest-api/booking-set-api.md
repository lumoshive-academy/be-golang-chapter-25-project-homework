### POST /api/booking
- Request Body
```json
{
  "cinemaId": "1",
  "seatId": "A1",
  "date": "2024-11-15",
  "time": "18:00",
  "paymentMethod": "credit_card"
}
```

- Response Success (201 Created)
```json
{
  "statusCode": 201,
  "message": "Booking confirmed.",
  "booking": {
    "bookingId": "abc123",
    "seatId": "A1",
    "cinemaId": "1",
    "date": "2024-11-15",
    "time": "18:00",
    "paymentMethod": "credit_card"
  }
}
```

- Response Failure (409 Conflict - Seat already booked)
```json
{
  "statusCode": 409,
  "message": "The selected seat is already booked."
}
```