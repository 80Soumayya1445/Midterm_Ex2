# Node.js Docker Application

This is a simple Node.js application containerized using Docker. The application uses Express.js to serve a basic API with health check endpoints.

## Features

- Express.js web server
- JSON response with timestamp and hostname
- Health check endpoint
- Docker containerization

## Prerequisites

- Docker installed on your system

## Building the Docker Image

To build the Docker image, run the following command in the project directory:

```bash
docker build -t node-docker-app .
```

## Running the Container

To run the container, use the following command:

```bash
docker run -p 3000:3000 node-docker-app
```

The application will be available at http://localhost:3000

## API Endpoints

- `GET /`: Returns a JSON response with a message, timestamp, and hostname
- `GET /health`: Returns a health status JSON response

## Environment Variables

- `PORT`: Port to run the server on (default: 3000)

## Docker Commands

### Build the image
```bash
docker build -t node-docker-app .
```

### Run the container
```bash
docker run -p 3000:3000 node-docker-app
```

### Run in detached mode
```bash
docker run -d -p 3000:3000 node-docker-app
```

### View logs
```bash
docker logs <container-id>
```

### Stop the container
```bash
docker stop <container-id>
```

## Testing the Application

Once the container is running, you can test the endpoints:

```bash
# Test the main endpoint
curl http://localhost:3000/

# Test the health endpoint
curl http://localhost:3000/health
