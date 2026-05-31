# API Test Suite — Restful Booker

![Newman API Tests](https://github.com/Delikanli13/api-testing-restful-booker/actions/workflows/newman.yml/badge.svg)

Automated API test suite for the [Restful Booker](https://restful-booker.herokuapp.com) API, built with Postman and Newman. Runs automatically on every push via GitHub Actions.

## What this project covers

- Full CRUD operations (GET, POST, PUT, PATCH, DELETE)
- Token-based authentication with automatic token chaining
- Request chaining using dynamic collection variables
- Positive and negative test scenarios
- Data-driven testing across multiple booking datasets
- JSON schema validation on GET and POST responses
- CI/CD pipeline via GitHub Actions

## Tech stack

| Tool | Purpose |
|---|---|
| Postman | API test authoring |
| Newman | CLI test runner |
| GitHub Actions | CI/CD pipeline |

## Test coverage

| Request | Method | Auth required | Assertions |
|---|---|---|---|
| Health Check | GET | ❌ | Status, response time |
| Get all bookings | GET | ❌ | Status, array structure |
| Create booking | POST | ❌ | Status, data, schema |
| Get single booking | GET | ❌ | Status, fields, schema |
| Negative test | GET | ❌ | 404 on invalid ID |
| Replace booking | PUT | ✅ | Status, updated values |
| Update booking | PATCH | ✅ | Status, partial update |
| Delete booking | DELETE | ✅ | Status 201 |

## How to run locally

**Prerequisites:** Node.js installed

**Install Newman:**
```bash
npm install -g newman
```

**Clone the repo:**
```bash
git clone https://github.com/Delikanli13/api-testing-restful-booker.git
cd api-testing-restful-booker
```

**Run the collection:**
```bash
newman run "Practice - Claude.postman_collection.json" \
  --environment "Restful Booker.postman_environment.json" \
  --iteration-data bookings-data.csv
```

## CI/CD

This suite runs automatically on every push to `main` via GitHub Actions. View the full run history in the [Actions tab](https://github.com/Delikanli13/api-testing-restful-booker/actions).