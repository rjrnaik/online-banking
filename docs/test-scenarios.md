# UI Scenarios

1. Login with valid credentials
2. Login with invalid credentials
3. View accounts summary
4. View transactions for an account
5. Transfer funds internally
6. Schedule a bill payment
7. Verify success messages and updated balances

# API Scenarios
1. GET /accounts/{id} → 200
2. GET /transactions?accountId → 200
3. POST /payments → 201
4. Negative:
   1. 401 unauthorized
   2. 403 forbidden
   3. 422 insufficient funds

# End-to-End Scenarios (UI + API)
1. Create account via API → verify UI dashboard
2. Perform transfer in UI → validate via API
3. Make payment via API → validate via DB + UI