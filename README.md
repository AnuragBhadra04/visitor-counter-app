# visitor-counter-app
This project follows a two-container Docker architecture. The Flask web application handles HTTP requests from users, communicates with the Redis database to store and update the visitor count, and returns the updated count as an HTML response. Both containers communicate over a Docker network, ensuring fast, lightweight, and scalable operation.

# Visitor Counter App using Flask & Redis

A simple Dockerized web application that counts the number of visitors using a Python Flask application and a Redis database.

## Project Architecture

The project follows a two-container Docker architecture:

- **Flask Container:** Handles HTTP requests, connects to Redis, updates the visitor count, and returns the HTML page.
- **Redis Container:** Stores the visitor count in memory for fast data access.
- **Docker Network:** Enables communication between the Flask and Redis containers.

## Architecture Flow

```
User Browser
      │
HTTP Request (Port 5000)
      │
Flask Container (app.py)
      │
TCP Connection (Port 6379)
      │
Redis Container
      │
Stores Visitor Count
      │
Returns Updated Count
      │
Flask Displays HTML Page
```

## Features

- Dockerized application
- Python Flask web server
- Redis in-memory database
- Visitor counter
- Lightweight and fast
- Easy to deploy

## Technologies Used

- Python
- Flask
- Redis
- Docker
- Docker Compose

## Project Structure

```
.
├── app.py
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
├── templates/
│   └── index.html
└── README.md
```

## How to Run

1. Clone the repository

```bash
git clone <repository-url>
cd visitor-counter
```

2. Build and start the containers

```bash
docker-compose up --build
```

3. Open your browser

```
http://localhost:5000
```

## How It Works

1. The user opens the application in a web browser.
2. Flask receives the HTTP request.
3. Flask connects to the Redis database.
4. Redis increments and stores the visitor count.
5. Flask returns an HTML page displaying the updated visitor count.

## Author

**Anurag Bhadra**
