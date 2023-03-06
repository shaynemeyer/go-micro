# Go Microservices

A collection of Microservices that demonstrates how to build microservices with the Go programming language. These microservices can be deployed in different ways. The main branch is intented for local development only. I will build other branches to demonstration how they can be deployed to Kubernetes or Docker Swarm. This is a work in progress so it should not be considered production grade. The choices made here are simple and for learning purposes only so far.

## Services

- Frontend - Web UI
- Broker Service - Broker that handles connections to services
- Authentication Service - handles authentication
- Logger Service - handles logging
- Mail Service - handles sending emails
- Listener Service - handles listening for events for RabbitMQ

### Other

- project - Make & docker-compose for all projects
