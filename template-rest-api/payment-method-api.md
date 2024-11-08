### GET /api/payment-methods
- Response Success (200 OK)
```json
{
  "statusCode": 200,
  "paymentMethods": [
    { "id": "1", "name": "Credit Card" },
    { "id": "2", "name": "Bank Transfer" },
    { "id": "3", "name": "Digital Wallet" }
  ]
}
```

### POST /api/pay
- Request Body
```json
{
  "bookingId": "abc123",
  "paymentMethod": "credit_card",
  "paymentDetails": {
    "cardNumber": "1234-5678-9012-3456",
    "expiryDate": "12/26",
    "cvv": "123"
  }
}
```

- Response Success (200 OK)
```json
{
  "statusCode": 200,
  "message": "Payment successful.",
  "transactionId": "txn789",
  "bookingId": "abc123"
}
```

- Response Failure (402 Payment Required - Payment failed)
```json
{
  "statusCode": 402,
  "error": "Payment failed due to insufficient funds."
}
```