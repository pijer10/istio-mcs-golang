# MICROSERVICE Architecture with Istio and Golang

Project of containerized microservice architecture and deployment on Kubernetes.
Microservices break down an application into smaller independent pieces.
Containerization with Kubernetes orchestration and management is designed to support microservices.
All microservices are written in Golang.

## Architecture Structure

The project consists of 3 different microservices:
* MicroS1
* MicroS2
* MicroS3

### MicroS1
* listening port 8090
* produce kafka msg to topic MS1-2

### MicroS2
* listening port 8087
* subscribe to kafka topic MS1-2
* writing messages to DB

### MicroS3
* listening port 8088
* pulling data from DB
* writting to Kafka topic MS3


## Plan
* Implementing a simple *http server*.
* Unit tests for test microservice.
* API tests with **POSTMAN**.
* Implementing HTTP verbs, _GET | POST | PUT | DELETE_.
* microservices talk to each other over gRPC + Protocol Buffers
* REST API developement. API service use Gorilla Mux to serve REST API response to the client and route them.
* promethes monitoring
* istio service mesh
* mTLS (istio)