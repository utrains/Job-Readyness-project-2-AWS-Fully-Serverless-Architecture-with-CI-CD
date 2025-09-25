# AWS Fully Serverless Architecture with CI/CD

## **Introduction:**

Enter the world of serverless computing, where developers are freed from server management. Deploying code becomes a breeze, with a focus on deploying functions rather than wrestling with servers. Originally synonymous with FaaS, serverless technology began with **AWS Lambda** from **Amazon Web Services**. It has now evolved to cover various managed services like databases and storage, expanding its scope beyond its initial function-centric approach.

Despite its name, serverless doesn’t mean a server-free existence. Instead, it signals a shift in responsibility — developers no longer need to manage, provision, or see the underlying servers. This allows them to concentrate on crafting efficient code without the distractions of server intricacies.

# Serverless-api

This Cloud Native API is designed to run on AWS Infrastructure while making use of AWS serverless services like Secrets Manager, Lambda functions, API Gateway, etc.

## Prerequisites for running the application locally

```javascript
// install dependencies
npm install
// start the server script
npm start
// run test cases
npm test
```

## Endpoint URLs

```javascript
// 1. Route to check if the server is healthy
GET /healthz
// 2. GET route to retrieve user details
GET /v1/user/{userId}
// 3. POST route to add a new user to the database
POST /v1/user
// 4. PUT route to update user details
PUT /v1/user/{userId}
```

### Sample JSON Response for GET

```json
{
  "id": 1,
  "first_name": "Jane",
  "last_name": "Doe",
  "username": "jane.doe@example.com",
  "account_created": "2016-08-29T09:12:33.001Z",
  "account_updated": "2016-08-29T09:12:33.001Z"
}
```

### Sample JSON Request for POST

```json
{
  "username": "jane.doe@example.com",
  "password": "password",
  "first_name": "Jane",
  "last_name": "Doe",  
}
```

### Sample JSON Request for PUT

```json
{
  "password": "password",
  "first_name": "Jane",
  "last_name": "Doe",  
}
```

## Endpoint URLs

```javascript
// 1. GET route to retrieve product details
GET /v1/product/{productId}
// 2. POST route to add a new product to the database
POST /v1/product
// 3. PUT route to update product details
PUT /v1/product/{productId}
// 4. PATCH route to update product details partially
PUT /v1/product/{productId}
// 5. DELETE route to delete product details
PUT /v1/product/{productId}
```

### Sample JSON Response for GET

```json
{
  "id": 1,
  "name": null,
  "description": null,
  "sku": null,
  "manufacturer": null,
  "quantity": 1,
  "date_added": "2016-08-29T09:12:33.001Z",
  "date_last_updated": "2016-09-29T09:12:33.001Z",
  "owner_user_id": 1
}
```

### Sample JSON Request for POST

```json
{
  "name": null,
  "description": null,
  "sku": null,
  "manufacturer": null,
  "quantity": 1
}
```

### Sample JSON Request for PUT

```json
{
  "name": null,
  "description": null,
  "sku": null,
  "manufacturer": null,
  "quantity": 1
}
```

### Sample JSON Request for PATCH

```json
{
  "name": null,
  "description": null,
  "sku": null,
  "manufacturer": null,
  "quantity": 1
}
```
