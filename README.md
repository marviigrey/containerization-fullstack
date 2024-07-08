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

## Running Locally

Run:
```
docker-compose up -d
```

## Access the containers locally
On your browser, you can access the following pages:

### Frontend
Load `localhost` in your browser to access the frontend.
![frontend](<Screenshot 2024-07-08 at 20.04.52.png>)

### Backend
Load `localhost/api` in your browser to access the backend.
![backend](<Screenshot 2024-07-08 at 20.14.57.png>)

### Backend Docs
Load `localhost/docs` in your browser to access the backend docs.
![backend-docs](<Screenshot 2024-07-08 at 20.04.30.png>)

### Backend Redoc
Load `localhost/redoc` in your browser to access the backend redoc.
![redoc](<Screenshot 2024-07-08 at 20.04.37.png>)

### Adminer
Load `db.localhost` or `localhost:8080` in your browser to access Adminer.
![adminer1](<Screenshot 2024-07-08 at 19.59.52.png>)
<img width="1196" alt="Screenshot 2024-07-08 at 20 18 29" src="https://gist.github.com/assets/89241109/99bafaae-1099-441c-80cc-cd1367cb1a11">

The login creds are:
| Value | Credential |
|----------|----------|
| System | PostgreSQL |
| Server | db   |
| Username | app   |
| Password | password   |
| Database | app   |
|||

### Proxy Manager GUI

Load `proxy.localhost` or `localhost:8090` in your browser to access Nginx Proxy Manager GUI.

![alt text](<Screenshot 2024-07-08 at 20.04.04.png>)
![alt text](<Screenshot 2024-07-08 at 20.03.51.png>)

The default login creds for Nginx Proxy Manager are:
| Value | Credential |
|----------|----------|
| Email | admin@example.com |
| Password | changeme |
|||