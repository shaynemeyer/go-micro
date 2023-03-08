# Go Microservices

A collection of Microservices that demonstrates how to build microservices with the Go programming language. These microservices can be deployed in different ways.

The main branch is intended for local development only. This branch demonstrates how this stack can be deployed to Kubernetes. This is a work in progress. The choices made here are simple and so far are for learning purposes only.

## Running Locally

- Make sure you have Docker installed.
- Make sure you have minikube.
- Make sure you have kubectl.

## Start Services with Make

Make sure you have Docker running.

### Start Services & Website

```bash
cd project/
minikube start --nodes=2
kubectl apply -f k8s
kubectl get pods
kubectl get svc
kubectl status
```

#### Start Postgres Container

```bash
docker-compose -f postgres.yml up -d
```

- Web -> [http://frontend.info](http://frontend.info)

### Stop Services & Website

```bash
multikube stop
docker-compose -f postgres.yml down
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

- Update the Makefile to support K8s workflow.
- Tests
- Documentation
- More useful UI.
