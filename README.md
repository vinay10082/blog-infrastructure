# Polyglot Microservices Blog Platform

This project is a microservice-based blog engine utilizing an API Gateway and polyglot backends. It is built using a multi-repo architecture.

### 🏗️ System Architecture Repositories:
* **[Infrastructure & Gateway (This Repo)](https://github.com/vinay10082/blog-infrastructure)**: Contains the NGINX API Gateway config and Docker Compose orchestration.
* **[Frontend Client](https://github.com/vinay10082/blog-frontend)**: The Angular 18 Single Page Application.
* **[Post Service](https://github.com/vinay10082/blog-post-server)**: The Java 26 / Spring Boot REST API handling core relational data and PostgreSQL.
* **[Comment Service](https://github.com/vinay10082/blog-comment-server)**: The Go REST API designed for high-concurrency comment processing.

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