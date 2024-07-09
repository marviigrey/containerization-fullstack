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

## Prerequisites
- Docker and Docker Compose installed on your machine
- Node.js (version 14.x or higher) and npm (version 6.x or higher) for local frontend setup
- Python 3.8 or higher and Poetry for local backend setup
- PostgreSQL for database setup
## Local Setup
### Backend
1. **Navigate to the backend directory**:
    ```sh
    cd backend
    ```
2. **Install dependencies using Poetry**:
    ```sh
    poetry install
    ```
3. **Set up the database with the necessary tables**:
    ```sh
    poetry run bash ./prestart.sh
    ```
4. **Run the backend server with a specific IP address**:
    ```sh
    poetry run uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
    ```
5. **Update configuration**:
   Ensure you update the necessary configurations in the `.env` file, particularly the database configuration.
### Frontend
1. **Navigate to the frontend directory**:
    ```sh
    cd frontend
    ```
2. **Install dependencies**:
    ```sh
    npm install
    ```
3. **Run the development server with a specific IP address**:
    ```sh
    npm run dev -- --host 0.0.0.0 --port 3000
    ```
4. **Configure API URL**:
   Ensure the API URL is correctly set in the `.env` file.
   
## Docker Setup with Docker Compose

1. **Build and start the services**:
    ```sh
    docker-compose up --build
    ```
2. **Stop the services**:
    ```sh
    docker-compose down
    ```
### Notes
- Before running the `docker-compose up` command, under the Docker Compose config for the backend, there is a `platform` specification. The Docker image is dependent on the system you are running the `docker-compose up` command on. Use the below to apply the patch based on your system:

| Platform | Patch |
|----------|----------|
| Mac M1   | linux/arm64    |
| Linux    | linux/amd64    |
| Mac Intel Chip | linux/amd64 |

- Ensure the `.env` files in both `frontend` and `backend` directories are correctly configured.
- The `docker-compose.yml` file defines the services for the frontend, backend, PostgreSQL, proxy manager, Adminer, and Nginx.

## Access the containers locally
On your browser, you can access the following pages:

### Frontend
Load `localhost` in your browser to access the frontend.
<img width="1196" alt="Screenshot 2024-07-08 at 20 04 52" src="https://github.com/FavourDaniel/containerization-hng/assets/89241109/1ecfb7b7-40ed-4d0c-9573-98012eb59f50">


### Backend
Load `localhost/api` in your browser to access the backend.
<img width="1196" alt="Screenshot 2024-07-08 at 20 14 57" src="https://github.com/FavourDaniel/containerization-hng/assets/89241109/a633aa16-d3c7-4174-a08a-66296889373d">

### Backend Docs
Load `localhost/docs` in your browser to access the backend docs.
<img width="1196" alt="Screenshot 2024-07-08 at 20 04 30" src="https://github.com/FavourDaniel/containerization-hng/assets/89241109/18a8b680-dd28-4009-ba56-b076f24146a8">

### Backend Redoc
Load `localhost/redoc` in your browser to access the backend redoc.
<img width="1196" alt="Screenshot 2024-07-08 at 20 04 37" src="https://github.com/FavourDaniel/containerization-hng/assets/89241109/c127015e-524d-41b4-9df7-e916ebcd22b4">


### Adminer
Load `db.localhost` or `localhost:8080` in your browser to access Adminer.
<img width="1196" alt="Screenshot 2024-07-08 at 19 59 52" src="https://github.com/FavourDaniel/containerization-hng/assets/89241109/36b54ad5-7a1e-4fd1-95bf-830529ee1c03">
<img width="1196" alt="Screenshot 2024-07-08 at 20 18 29" src="https://github.com/FavourDaniel/containerization-hng/assets/89241109/6c71b1c7-7820-4ff8-8d93-eec85739af39">

The login creds are:
| Value | Credential |
|----------|----------|
| System | PostgreSQL |
| Server | db   |
| Username | app   |
| Password | password   |
| Database | app   |

### Proxy Manager GUI

Load `proxy.localhost` or `localhost:8090` in your browser to access Nginx Proxy Manager GUI.
<img width="1196" alt="Screenshot 2024-07-08 at 20 04 04" src="https://github.com/FavourDaniel/containerization-hng/assets/89241109/83abdf29-a785-4ece-baec-5a5377176135">
<img width="1196" alt="Screenshot 2024-07-08 at 20 03 51" src="https://github.com/FavourDaniel/containerization-hng/assets/89241109/a8e89846-95df-4d6b-bbf3-4aa8a15fafd2">


The default login creds for Nginx Proxy Manager are:
| Value | Credential |
|----------|----------|
| Email | admin@example.com |
| Password | changeme |
