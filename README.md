# API Test Suite — Restful Booker

Automated API test suite built with Postman and Newman.

## What's covered
- Full CRUD operations (GET, POST, PUT, PATCH, DELETE)
- Token-based authentication
- Positive and negative test scenarios
- Request chaining with dynamic variables
- 26 assertions across 9 requests

## Tech stack
- Postman
- Newman (CLI runner)
- GitHub Actions (CI/CD)

## How to run locally

Install Newman:
```bash
npm install -g newman
```

Run the collection:
```bash
newman run "Practice - Claude.postman_collection.json" --environment "Restful Booker.postman_environment.json"
```
