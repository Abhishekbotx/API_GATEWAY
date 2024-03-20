# API Gateway

The API Gateway serves as a central entry point for client requests, providing a unified interface to access various microservices in the system. It plays a crucial role in managing routing, authentication, rate limiting, and logging to ensure secure and efficient communication between clients and microservices.

## Features

### 1. Authentication Middleware:

The Authentication Middleware validates authentication tokens provided by clients to ensure secure communication with different services. This layer verifies the authenticity of tokens before allowing access to protected resources.

### 2. Proxy Middleware:

The Proxy Middleware leverages the `http-proxy-middleware` library to proxy requests from the API Gateway to corresponding microservices. By abstracting service discovery and routing complexities, it enables seamless communication between clients and microservices.

### 3. Rate Limiting and Logging:

- **Rate Limiting:** Implements rate limiting to restrict the number of requests a client can make within a specified time window. This helps prevent abuse of system resources and enhances system stability and security.
  
- **Logging:** Utilizes the Morgan library for logging HTTP requests and responses. This logging mechanism provides valuable insights for debugging, monitoring, and auditing system activities, ensuring smooth operation and quick resolution of issues.

## Usage

To use the API Gateway, follow these steps:

1. **Installation**: Clone the repository and install dependencies using `npm install`.

2. **Configuration**: Edit the `.env` file with appropriate configuration settings, including service endpoints, authentication parameters, and logging options.

3. **Start the Server**: Run `npm start` to start the API Gateway server.

4. **Access Endpoints**: Use the defined endpoints to interact with the microservices through the API Gateway.

## Dependencies

- **Express**: Fast, unopinionated, minimalist web framework for Node.js.
- **http-proxy-middleware**: Middleware for proxying requests with Node.js.
- **morgan**: HTTP request logger middleware for Node.js.
- **express-rate-limit**: Rate limiting middleware for Express applications.