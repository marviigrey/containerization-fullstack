# Use an image with curl pre-installed to streamline the build
FROM python:3.11.1-slim-bullseye

# Update package lists and install curl for Poetry installation
RUN apt-get update && apt-get install -y curl

# Download and install Poetry
RUN curl -sSL https://install.python-poetry.org | python -

# Add Poetry to the system PATH to make it easily accessible
ENV PATH="${PATH}:/root/.local/bin"

# Set the working directory inside the container
WORKDIR /backend

# Copy only Poetry configuration files to leverage Docker layer caching
COPY pyproject.toml poetry.lock ./

# Install project dependencies using Poetry
RUN poetry install

# Copy the rest of the application code into the container
COPY . .

# Set the PYTHONPATH environment variable so Python can find your app module
ENV PYTHONPATH=/backend

# Run prestart script
RUN poetry run bash ./prestart.sh

# Expose the port the FastAPI application will run on
EXPOSE 8000

# Define the default command to run when the container starts
CMD ["poetry", "run", "uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]