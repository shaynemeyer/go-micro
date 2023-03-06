# Go Microservices

A collection of Microservices that demonstrates how to build microservices with the Go programming language. These microservices can be deployed in different ways.

The main branch is intended for local development only. I will build other branches to demonstrate how they can be deployed to Kubernetes or Docker Swarm. This is a work in progress. The choices made here are simple and so far are for learning purposes only.

## Running Locally

- Make sure you have Docker installed.
- Make sure you have Go installed.
- Make sure you have Make installed.

## Start Services with Make

Make sure you have Docker running.

### Start Services & Website

```bash
cd project/
make up_build # Start the services
make start # Start the website
```

- Web -> [http://localhost](http://localhost)
- MailHog -> [http://localhost:8025](http://localhost:8025)

### Stop Services & Website

```bash
make down # Stop the services
make stop # Stop the website
```

## Services

- Frontend - Web UI
- Broker Service - Broker that handles connections to services
- Authentication Service - handles authentication
- Logger Service - handles logging
- Mail Service - handles sending emails
- Listener Service - handles listening for events for RabbitMQ

### Other

- project - Make & docker-compose for all projects

## Todos

- Tests
- Documentation
- More useful UI.
