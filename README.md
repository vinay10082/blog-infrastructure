# Blog Infrastructure

This repository contains the infrastructure configuration for the microservices blog project. It orchestrates the backend services and sets up an API Gateway.

## Components
- **API Gateway (Nginx)**: Proxies requests to the appropriate backend microservice based on the URL path (`/api/posts` and `/api/comments`).

## Configuration
The ports can be configured via the `.env` file in this directory:
```env
API_GATEWAY_PORT=8080
POST_SERVER_PORT=8081
COMMENT_SERVER_PORT=8082
```

## Running the Infrastructure
Make sure your `.env` file is populated, then run:
```bash
docker compose up -d --build
```
