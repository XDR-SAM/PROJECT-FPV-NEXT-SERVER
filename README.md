
# Project FPV Backend

This is the backend server for Project FPV, a web application for FPV drone enthusiasts. It's built with Node.js, Express, and MongoDB, and uses Firebase for authentication.
## Live link : 
 https://project-fpv-next-client.vercel.app

## Features

*   **User Authentication:** Secure user authentication using Firebase Authentication.
*   **User Management:** Syncs Firebase users with a local MongoDB database.
*   **Blog Posts:** Full CRUD functionality for blog posts.
*   **Likes and Views:** Users can like and view blog posts.
*   **API:** A RESTful API for all resources.
*   **Deployment:** Configured for deployment on Vercel.

## Tech Stack

*   **Backend:** Node.js, Express.js
*   **Database:** MongoDB with Mongoose
*   **Authentication:** Firebase Admin SDK
*   **Validation:** express-validator
*   **CORS:** cors
*   **Environment Variables:** dotenv

## API Endpoints

### Auth

*   `POST /api/auth/sync`: Syncs a Firebase user with the MongoDB database.
*   `GET /api/auth/me`: Gets the currently authenticated user.
*   `GET /api/auth/verify`: Verifies a Firebase token.

### Blog Posts

*   `GET /api/blogs`: Gets all blog posts.
*   `GET /api/blogs/:id`: Gets a single blog post by ID.
*   `POST /api/blogs`: Creates a new blog post.
*   `PUT /api/blogs/:id`: Updates a blog post.
*   `DELETE /api/blogs/:id`: Deletes a blog post.
*   `GET /api/blogs/user/my-posts`: Gets all blog posts by the currently authenticated user.
*   `POST /api/blogs/:id/like`: Likes or unlikes a blog post.

### Stats

*   `GET /api/stats`: Gets community stats.
*   `GET /api/categories`: Gets popular categories.

### Health Check

*   `GET /api/health`: Checks the health of the server.

## Getting Started

### Prerequisites

*   Node.js
*   npm
*   MongoDB
*   Firebase project

### Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/XDR-SAM/PROJECT-FPV-EXPRESS-SERVER.git
    ```

2.  Install the dependencies:

    ```bash
    npm install
    ```

3.  Create a `.env` file in the root directory and add the following environment variables:

    ```
    MONGODB_URI=<your-mongodb-uri>
    PORT=5000
    NODE_ENV=development
    CORS_ORIGIN=http://localhost:3000
    FIREBASE_TYPE=<your-firebase-type>
    FIREBASE_PROJECT_ID=<your-firebase-project-id>
    FIREBASE_PRIVATE_KEY_ID=<your-firebase-private-key-id>
    FIREBASE_PRIVATE_KEY=<your-firebase-private-key>
    FIREBASE_CLIENT_EMAIL=<your-firebase-client-email>
    FIREBASE_CLIENT_ID=<your-firebase-client-id>
    FIREBASE_AUTH_URI=<your-firebase-auth-uri>
    FIREBASE_TOKEN_URI=<your-firebase-token-uri>
    FIREBASE_AUTH_PROVIDER_CERT_URL=<your-firebase-auth-provider-cert-url>
    FIREBASE_CLIENT_CERT_URL=<your-firebase-client-cert-url>
    ```

### Usage

1.  Start the server:

    ```bash
    npm start
    ```

2.  The server will be running on `http://localhost:5000`.

### Development

1.  Start the server in development mode:

    ```bash
    npm run dev
    ```

2.  The server will automatically restart when you make changes to the code.

## Deployment

This project is configured for deployment on Vercel. To deploy, simply push your code to a Git repository and import it into Vercel.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.
