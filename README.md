# API Proxy Server
This project is an API proxy server that enables users to make requests to an external API through a local server. By routing requests through the proxy server, users can add additional functionality, such as caching, logging, and authentication, without modifying the client application.

## Features
- Proxy requests to an external API
- Caching of responses to improve performance
- Logging of request and response data for debugging
- Authentication of requests using API keys or OAuth 2.0 tokens
- Rate limiting to prevent abuse and ensure fair usage

## Getting Started
To use the API proxy server, you will need to have Node.js and npm installed on your local machine. Once you have these dependencies installed, follow these steps:

1.  Clone the repository to your local machine.
2.  Install the required packages by running npm install.
3.  Create a .env file in the root directory of the project with the following variables:
4.  API_BASE_URL: the base URL of the external API you wish to proxy
5.  API_KEY: the API key required for authentication (if applicable)
6.  OAUTH_CLIENT_ID: the client ID required for OAuth 2.0 authentication (if applicable)
7.  OAUTH_CLIENT_SECRET: the client secret required for OAuth 2.0 authentication (if applicable)
8.  Start the server by running npm start.

## Usage
To make requests through the API proxy server, use the URL of the local server (http://localhost:3000 by default) as the base URL for your requests. All requests to the local server will be proxied to the external API with the appropriate headers and parameters.

## Caching
By default, the API proxy server will cache responses to GET requests to improve performance. Cached responses will be stored in memory and will expire after a set time period (30 seconds by default). To disable caching, set the DISABLE_CACHE environment variable to true.

## Logging
The API proxy server will log request and response data to the console by default. To disable logging, set the DISABLE_LOGGING environment variable to true.

## Authentication
If the external API requires authentication, you can include the API key or OAuth 2.0 token in the request headers. The API proxy server will automatically add the required headers to proxied requests. If authentication is not required, simply omit the API_KEY, OAUTH_CLIENT_ID, and OAUTH_CLIENT_SECRET environment variables.

## Rate Limiting
To prevent abuse and ensure fair usage, the API proxy server includes rate limiting functionality. By default, requests are limited to 100 requests per minute per IP address. To customize the rate limiting behavior, modify the RATE_LIMIT_WINDOW_MS and RATE_LIMIT_MAX_REQUESTS environment variables.

## Contributing
Contributions to this project are welcome! If you find a bug or have an idea for a new feature, please create a new issue or submit a pull request with your changes.

This project is licensed under the MIT license, which allows for free use, modification, and distribution of the software. See the LICENSE file for more details.
