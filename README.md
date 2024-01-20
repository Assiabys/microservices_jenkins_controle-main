# Author  BOUALI Adnane , BENYOUS Assia , 5MG-G2
#  Spring Cloud, React, CI, CD 

ce repository est un systeme de gestion pour distributeur de vehicule

The architecture supports the following technologies: 

  * Frameworks - Spring Boot, Spring Cloud, Feign, Eureka, Resilience4j.
  * UI - React Native or React Native Web to build as a mobile app or hybrid app (web + mobile)
  * Firebase, AWS Amplify, or Hasura (using GraphQL subscriptions) to send messages in realtime
  * Cloudinary or Firebase storage for sending messages with image or video content
  * Serverless functions like AWS Lambda or Firebase Functions for notifications
  * Cloudinary or Firebase storage for uploading pictures or video
  * Algolia for lightning-fast vehicle searching
  * Databases - H2, MySQL, MariaDB, PostgreSQL, MongoDB
  * API Management : Spring REST Docs, Swagger
  * Security: JWT (JSON Web Token) with OIDC, OpenID Connect with MITREid Connect, OAuth 2.0,  “UAA” (User Account and Authentication) server.
  * Message brokers - Apache Kafka, RabbitMQ, and Redis Streams
  * Services communicate asynchronously using domain events, and command/reply messages.
  * Cloud - AWS, Pivotal Cloud Foundry (PCF), Google Compute Platform (GCP), OpenStack, VMware vSphere,  Heroku, Netlify
  * Server Side - Spring Boot, Spring Security, Maven, Hibernate, Liquibase, Cucumber, ArchUnit, Gatling, Elasticsearch, Kafka, Elastic Stack, Prometheus
  * Client Side - HTML5, Bootstrap, TypeScript, Angular, React.
  * CI / CD - Jenkins, Travis CI, Github Workflows, Docker, Docker Compose, Kubernetes, Minikube, Minishift, OpenShift, Jenkins X, KOTS, ECS (Elastic Container Service), EKS (Elastic Kubernetes Service)


# Architecture

The following diagram shows the targert platform architecture.:

![Targert platform architecture](/docs/images/Targert-platform-architecture.png)

Since an auto dealership application uses the Microservice architecture pattern for vehicle details data is spread over multiple services. For example,

- Vehicle Service - basic information about the vehicle
- Transaction service - purchase history for vehicle, vehicle price
- Dealership service - vehicle availability,Order processing, stock

Consequently, the code that displays the vehicle details needs to fetch information from all of these services.


## Building and running the application

This is a Maven project. However, you  need to have installed :
  - Java Development Kit >= 11
  - React "^16.13.1"
  - Docker
  - Maven
  - Kubernates CLI
  - Minikube
  - Minishift
  - Ansible
  - Jenkins


# Modules:

- [x] config-service
- [x] discovery-service
- [x] gateway-service
- [x] config-repo
- [x] vehicle-service
- [x] vehicle-ui-web
- [ ] vehicle-ui-mobile
- [ ] dealership-service
- [ ] transaction-service
- [X] admin-dashboard
- [ ] Shell Scripts  files (startRabbit, startDevVault, set-local-env-git, install-letsencrypt-cert, create-services, create-release-branch)
- [ ] RabbitMq 
- [ ] Kafka
- [ ] UI AngularJS
- [ ] CI / CD - Jenkins
- [ ] CI / CD - Github Workflows 
- [ ] CI / CD - Travis CI
- [ ] CI / CD - Kubernetes (config, configmap, deployment, service, support-bundle, replicated-app)
- [ ] CI / CD - Docker, Docker Compose
- [ ] CI / CD - Jenkins X
- [ ] Auth-server
- [ ] IaC

# Important endpoints

Run locally with Maven, Visual Studio Code, STS, Eclipse or IntelliJ:

:point_right: Gateway http://localhost:8080  
:point_right: Eureka Discovery Dashboard http://localhost:8761  
:point_right: Config Server http://localhost:7761  
:point_right: Spring Admin Dashboard http://localhost:9761  
:point_right: Vehicle service http://localhost:8081  
:point_right: Dealership service http://localhost:8082  
:point_right: Transaction service http://localhost:8083  
:point_right: RabbitMq (username/password: guest/guest) http://localhost:15000 



Run with docker-compose:

:point_right: Gateway http://localhost:5080  
:point_right: Eureka Discovery Dashboard http://localhost:5761  
:point_right: Config Server http://localhost:5760  
:point_right: Spring Admin Dashboard http://localhost:5761  
:point_right: Vehicle service http://localhost:5081  
:point_right: Dealership service http://localhost:5082  
:point_right: Transaction service http://localhost:5083  
:point_right: RabbitMq (username/password: guest/guest) http://localhost:15000 




### Vehicle service

To run locally:
  ```shell
  $ cd vehicle-service
  $ java -jar target/vehicle-service-0.0.1.BUILD-SNAPSHOT.jar
  ```

### Dealership service

To run locally:
```shell
cd dealership-service
java -jar target/dealership-service-0.0.1.BUILD-SNAPSHOT.jar
```
### Transaction service

To run locally:
```shell
cd transaction-service
java -jar target/transaction-service-0.0.1.BUILD-SNAPSHOT.jar
```

### Gateway Server

To run locally:
```shell
cd gateway-service
java -jar target/gateway-service-0.0.1.BUILD-SNAPSHOT.jar
```

###  Discovery server

To run locally:
```shell
cd discovery-service
java -jar target/discovery-service-0.0.1.BUILD-SNAPSHOT.jar
```

###  Admin server

To run locally:
```shell
cd admin-service
java -jar target/admin-service-0.0.1.BUILD-SNAPSHOT.jar
```


