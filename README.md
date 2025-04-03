# Full-Stack Application (React, Node.js, MongoDB) with Docker

## Table of Contents
1. [Project Description](#project-description)
2. [How to Run Locally](#how-to-run-locally)
3. [Technologies](#technologies)
4. [Project Structure](#project-structure)

## Project Description
This is a full-stack application containing:
- **Frontend**: A React application for user interaction.
- **Backend**: A Node.js API using Express.js for handling requests.
- **Database**: MongoDB as the database to store and manage data.
Users can retrieve, add, and delete tasks (goals) via a backend API. The application is fully dockerized, ensuring seamless deployment in containerized environments. 
Docker Compose is used to manage multiple containers efficiently, making it easy to set up and run the project.

## How to Run Locally
To run the application locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Slav666/docker-compose-app/repository.git
   cd repository
   
2. **Environment variables:** 
The application requires environment variables to be configured in order to run correctly.
These variables are stored in two separate .env files: backend.env for the backend, and mongo.env for MongoDB.(see the Project Structure)

   **backend.env**
    This file contains the environment variables for the backend (Node.js application) that connects to the MongoDB database.
        MONGODB_USERNAME=username
        MONGODB_PASSWORD=password
    Make sure to replace username and password with the appropriate values for your MongoDB connection.

   **mongo.env**
    This file contains the environment variables for MongoDB initialization.
        MONGO_INITDB_ROOT_USERNAME=username
        MONGO_INITDB_ROOT_PASSWORD=password
     Again, replace username and password with your desired MongoDB root credentials.

4. **Build and run the containers using Docker Compose:**
   Make sure Docker and Docker Compose are installed on your computer.
   Run the following command in the directory where the docker-compose.yml file is located:
   ```bash
   docker-compose up --build

## Technologies
This project uses the following technologies:
          Frontend: React, Next.js (depending on your setup)
          Backend: Node.js, Express.js
          Database: MongoDB
          Docker: Docker, Docker Compose
          
## Project Structure

            ├── backend/               # Directory containing the backend code (Node.js)
            ├── frontend/              # Directory containing the frontend code (React)
            ├── env/                   # Directory containing .env files (ignored by Git)
            │   ├── backend.env        # Environment variables for the backend
            │   └── mongo.env          # Environment variables for MongoDB initialization
            ├── docker-compose.yml     # Docker Compose configuration file
            └── README.md              # This file


