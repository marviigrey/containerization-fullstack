# Full-Stack FastAPI and React Template

Welcome to the Full-Stack FastAPI and React template repository. This repository serves as a demo application for interns, showcasing how to set up and run a full-stack application with a FastAPI backend and a ReactJS frontend using ChakraUI.

## Project Structure

The repository is organized into two main directories:

- **frontend**: Contains the ReactJS application.
- **backend**: Contains the FastAPI application and PostgreSQL database integration.

Each directory has its own README file with detailed instructions specific to that part of the application.

## Getting Started

To get started with this template, please follow the instructions in the respective directories:

- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)

Ensure you have:

- docker engine and docker compose
- nodejs
- python
- postgresql

For both backend and frontend, create an image using the docker files in their respective directories.

Frontend: ensure the .env is properly configured with your domain name.
backend: The env file should contain the credentials of your postgresql and CORS origin. 
Docker-compose file contains the configuration of both the frontend backend database pointing to our domain names.

