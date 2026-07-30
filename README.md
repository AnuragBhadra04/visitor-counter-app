# visitor-counter-app
This project follows a two-container Docker architecture. The Flask web application handles HTTP requests from users, communicates with the Redis database to store and update the visitor count, and returns the updated count as an HTML response. Both containers communicate over a Docker network, ensuring fast, lightweight, and scalable operation.
