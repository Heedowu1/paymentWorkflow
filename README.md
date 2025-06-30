# 💳 Payment Checkout Workflow - Postman Collection

This Postman collection simulates a complete **payment checkout process**, including user authentication, transaction initiation, authorization, and validation. It's ideal for testing a fintech API's core payment functionalities in a controlled environment.

## 📁 Collection Overview

The collection contains multiple endpoints that mimic a payment workflow:

| Endpoint Name | Method | Description |
|---------------|--------|-------------|
| `signin` | POST | Authenticates a user and returns access/refresh tokens |
| `invalid signin with wrong password` | POST | Attempts signin with incorrect credentials |
| `initiate transaction` | POST | Begins a new transaction with valid data |
| `initiate transaction with invalid account number` | POST | Attempts a transaction with a wrong account number |
| `authorize transaction` | POST | Authorizes a transaction using a PIN |
| `invalid pin` | POST | Attempts authorization with an invalid PIN |
| `validate transaction` | GET | Verifies the status of a previously authorized transaction |

## 🧪 Test Scripts

Each request is equipped with **test scripts** to validate:
- HTTP status codes (`200`, `400`, `401`, `422`)
- Response time is below `2000ms`
- Expected response structure (e.g., `accessToken`, `trxRef`, `sessionID`)

## 🧾 Environment Variables

| Key | Value |
|-----|-------|
| `url` | `https://49a32bfc-7c40-467a-8e63-ab08377054f1.mock.pstmn.io` |
| `accessToken` | JWT token used for bearer authentication |

> 🔐 Make sure to **update `accessToken` and `url`** as required before running the requests against your actual environment.

## ✅ How to Use

1. **Import Collection**
   - Open Postman → `File > Import` → Select the JSON file (e.g., `payment-checkout.postman_collection.json`)

2. **Set Up Environment**
   - Go to `Environments` in Postman.
   - Create a new environment.
   - Add:
     - `url` as base URL
     - `accessToken` as your current auth token
   - Select this environment from the dropdown in the top-right corner.

3. **Run Collection**
   - Use the **Runner** or send requests manually.
   - Check test results in the **Test Results tab** for each request.

## 🚫 Error Simulation

This collection includes requests that simulate:
- Wrong password
- Invalid account number
- Invalid transaction PIN

These help test the API’s error handling under various conditions.

---

## 🔗 Postman Share Link

You can access the shared workspace and collection via:

👉 [Open in Postman](https://hng-11.postman.co/workspace/IDOWU-WORKSPACE~c097ca22-4934-42aa-9753-e50b0ca4280e/collection/36393272-f521b228-a55a-4bbd-b7f8-c12dfe64d79c?action=share&source=collection_link&creator=36393272)

---

## 👩‍💻 Author

**Idowu Adekunle**  
Postman workspace: `IDOWU-WORKSPACE`  
Collection exported on: _2025-06-30_

---

