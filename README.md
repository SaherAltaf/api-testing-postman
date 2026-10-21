# API Testing with Postman – Restful Booker

API tests for [Restful Booker](https://restful-booker.herokuapp.com), a free practice API for hotel bookings.

## What Is Tested
| # | Request | What it checks |
|---|---|---|
| 1 | Health Check | API is up (status 201) |
| 2 | Create Token | Valid login returns a token |
| 3 | Create Token – Wrong Password | Returns "Bad credentials" and no token |
| 4 | Create Booking | Booking is created and its ID is saved |
| 5 | Get Booking | Correct booking data comes back |
| 6 | Update Booking | Full update works with a valid token |
| 7 | Update Booking – No Token | Request is blocked (status 403) |
| 8 | Partial Update | Only the changed field is updated |
| 9 | Delete Booking | Booking is deleted (status 201) |
| 10 | Get Deleted Booking | Deleted booking is not found (status 404) |

The token and booking ID are saved in collection variables, so all requests run as one complete flow.

## How to Run
**In Postman**
1. Click **Import** and select `restful-booker.postman_collection.json`
2. Open the collection and click **Run**
3. Click **Run Restful Booker API Tests** to see Pass/Fail for every test

**From the command line (Newman)**
```bash
npm install -g newman
newman run restful-booker.postman_collection.json
```

## Tools Used
Postman · Newman · JavaScript (test scripts)
