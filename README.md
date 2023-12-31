A complete full-stack application with ReactJS for the frontend and Spring Boot 3 with Spring Security for the backend. The application will have JWT authentication for user login.

JWT (JSON Web Token) is a stateless token used for authentication. In this stateless application, the backend will not maintain any session or create any cookies. Instead, the backend will rely on the JWT to authenticate each request from the frontend. The JWT will contain some basic information, such as the user ID, first name, last name, roles, and expiration date.

The process of JWT authentication will involve the following steps:

1. Backend Generation of Token: The backend will generate the JWT when a user logs in or registers.

2. Frontend Storage of Token: Once generated by the backend, the frontend will store the JWT in the local storage of the user's browser. This token will be used for each subsequent request to the backend.

3. Token in HTTP Header: To authenticate each request, the frontend will send the JWT in the HTTP header, specifically in the Authorization header. The Authorization header will contain the token in the form of a Bearer token.

4. Public and Authenticated Requests: The backend will handle two types of requests: public requests (login and registration) that do not require authentication and authenticated requests that need a valid JWT for access.

5. JWT Parsing Filter: To ensure that each authenticated request contains a valid JWT, the backend will use a filter that reads and parses the token before reaching the controller.
