# Accounting notebook

Web application, which tracks money flow of a single user.

## Setup

From root directory run
```javascript
npm ci
```
or 

```javascript
npm install
```

## Running the Application

```javascript
npm run start
```
By default, the application is run on http://localhost:7000. 
When the application is run you can test API using Postman.

## Running the Application with DEBUGGER

```javascript
npm run debug
```

## API endpoints

### To get transactions history

`curl -L -X GET 'http://localhost:7000/api/transactions-history'`

### To get the transaction by ID

`curl -L -X GET 'http://localhost:7000/api/transactions-history/{id}'`

### To get account balance

`curl -L -X GET 'http://localhost:7000/api/account-balance'`

### To send transaction

```
curl -L -X POST 'http://localhost:7000/api/transactions-history' \
-H 'Content-Type: application/json' \
--data-raw '{
    "type": "credit",
    "amount": 150
}'
```