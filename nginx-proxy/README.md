# Nginx Reverse Proxy with Docker

This project demonstrates a simple load balancer using Docker and Nginx.

## Architecture

Browser → Nginx Proxy → App1 / App2

The Nginx container distributes traffic to two backend containers.

## Technologies Used

- Docker
- Docker Compose
- Nginx
- Git
- GitHub

## Project Structure

nginx-proxy/
│
├── docker-compose.yml
├── nginx.conf
└── README.md

## Run the Project

Clone the repository:

git clone https://github.com/YOUR_USERNAME/nginx-proxy.git

Move into the project:

cd nginx-proxy

Start containers:

docker compose up -d

Check containers:

docker ps

Open browser:

http://localhost:8081

## Expected Result

Requests go through the Nginx reverse proxy and are forwarded to app1 or app2.