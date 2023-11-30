# Google-API-

create a JWT when the user is logged in and use the JWT Bearer token authentication for the private endpoints.

The FastAPI application created in the previous guide uses a Starlette middleware to read the session cookies, we are going to limit the use of this middleware to just the login y auth endpoints. The rest of the application is going to run without middlewares.

$ Requirements
This guide assumes you already have installed in your system python3.8 (or newer).

All the steps to create the Google Credentials and the login and auth endpoint are defined in Use Google Login (OAuth) with FastAPI - Python.

Support for endpoints with different middlewaresPermalink
With FastAPI we can not set just an endpoint to use a middleware, it applies to all the routes. There is a way to resolve this, we can create two sub-apps and then mount both of them in our main app.

We are going to start developing on top of the last guide.

