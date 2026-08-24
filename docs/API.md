# Vitalbet API Documentation

## Base URL
```
http://localhost:5000/api/v1
```

## Authentication
All protected endpoints require a JWT token in the Authorization header:
```
Authorization: Bearer <token>
```

## Endpoints

### Authentication

#### Register User
```
POST /auth/register
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "password123",
  "firstName": "John",
  "lastName": "Doe"
}
```

#### Login
```
POST /auth/login
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "password123"
}
```

Response:
```json
{
  "token": "eyJhbGciOiJIUzI1NiIs...",
  "user": {
    "id": "123",
    "email": "user@example.com",
    "firstName": "John",
    "lastName": "Doe"
  }
}
```

### Bets

#### Get All Bets
```
GET /bets
Authorization: Bearer <token>
```

#### Place a Bet
```
POST /bets
Authorization: Bearer <token>
Content-Type: application/json

{
  "eventId": "event123",
  "amount": 50,
  "odds": 1.75,
  "betType": "single"
}
```

#### Get Bet History
```
GET /bets/history
Authorization: Bearer <token>
```

### Sports Events

#### Get All Events
```
GET /events
```

#### Get Event Details
```
GET /events/:eventId
```

#### Get Live Odds
```
GET /events/:eventId/odds
```

### Account

#### Get User Profile
```
GET /account/profile
Authorization: Bearer <token>
```

#### Update Profile
```
PUT /account/profile
Authorization: Bearer <token>
Content-Type: application/json

{
  "firstName": "John",
  "lastName": "Doe",
  "phone": "+1234567890"
}
```

#### Get Balance
```
GET /account/balance
Authorization: Bearer <token>
```

#### Deposit Funds
```
POST /account/deposit
Authorization: Bearer <token>
Content-Type: application/json

{
  "amount": 100,
  "paymentMethod": "card"
}
```

## Error Responses

### 400 Bad Request
```json
{
  "error": "Invalid request",
  "message": "Detailed error message"
}
```

### 401 Unauthorized
```json
{
  "error": "Unauthorized",
  "message": "Token expired or invalid"
}
```

### 404 Not Found
```json
{
  "error": "Not Found",
  "message": "Resource not found"
}
```

### 500 Internal Server Error
```json
{
  "error": "Server Error",
  "message": "An unexpected error occurred"
}
```
