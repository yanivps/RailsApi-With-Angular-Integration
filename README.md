Angular with Rails API Demo
===========================

##### Includes User credentials and OAuth2 authentication

Server side is a **Rails 5 api-only** application for managing Todo lists  
Main features:

*   Server is Token-based (JWT)
*   Server responds with JSON. Two-way conversion between rails snake_case to JavaScript camelCase, in request and response
*   Authentication with user credentials
*   Authentication with OAuth2. Google and Facebook built in. (Easy to add new providers!)
    *   No session / cookies are required in rails app
    *   Get 'authorization code' from the client and exchange it for an 'access token' with the OAuth server
    *   Use the 'access token' to get identity information, get or create app user and return an app token to the client
*   API versioning
*   JSON serializers with active model serializers
*   Pagination

Client side is an **Angular** application which access the Rails REST API  
Main Features:

*   Add JWT token to each request's 'Authorization' header
*   AuthModule - an authentication module which includes:
    *   Authentication with user credentials
    *   Authentication with OAuth2. Google and Facebook built in. (Easy to add new providers!)  
        Client redirects to OAuth provider to get an 'authorization code' and exchange it for an app token (JWT) with the server
*   Global error handling
*   Seperation for feature specific modules
