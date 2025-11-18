# Customer
Represents a bank user.

| Field    | Type      | Description        |
| -------- | --------- | ------------------ |
| id       | UUID/Long | Unique customer id |
| username | String    | Login username     |
| password | String    | Encrypted password |
| fullName | String    | Display name       |

# Account
Represents a bank account belonging to a customer.

| Field       | Type       | Description      |
| ----------- | ---------- | ---------------- |
| id          | UUID/Long  | Account ID       |
| customerId  | Long       | Owner            |
| accountType | Enum       | CHEQUING/SAVINGS |
| balance     | BigDecimal | Current balance  |

# Transaction
Represents financial activity.

| Field     | Type          | Description                         |
| --------- | ------------- | ----------------------------------- |
| id        | UUID/Long     | Transaction ID                      |
| accountId | Long          | Related account                     |
| type      | Enum          | DEPOSIT/WITHDRAWAL/TRANSFER/PAYMENT |
| amount    | BigDecimal    | Amount                              |
| timestamp | LocalDateTime | When happened                       |

# Payment
Represents a bill or scheduled payment.

| Field      | Type       | Description          |
| ---------- | ---------- | -------------------- |
| id         | UUID       | Payment id           |
| customerId | Long       | Owner                |
| payee      | String     | Utility/company name |
| amount     | BigDecimal | Payment amount       |
| date       | LocalDate  | Scheduled date       |

# Transfer
Represents internal transfer request.

| Field     | Type          | Description                         |
| --------- | ------------- | ----------------------------------- |
| id        | UUID/Long     | Transaction ID                      |
| accountId | Long          | Related account                     |
| type      | Enum          | DEPOSIT/WITHDRAWAL/TRANSFER/PAYMENT |
| amount    | BigDecimal    | Amount                              |
| timestamp | LocalDateTime | When happened                       |


