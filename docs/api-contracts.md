# Account
GET /accounts/{id}
GET /customers/{customerId}/accounts
POST /accounts/transfer

# Transaction
GET /transactions?accountId=xyz

# Payment
POST /payments
GET /payments?customerId=xyz

# Auth
POST /auth/login

401 – unauthorized
403 – forbidden
404 – not found
422 – invalid request (e.g., insufficient balance)