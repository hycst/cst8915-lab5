
# CST8915 Lab 5 – Containerizing the Algonquin Pet Store with Docker

**Course:** CST8915 Full-stack Cloud-native Development  
**Professor:** Ramy Mohamed  
**Student:** Hesheng Yang  

---

### Demo Video

https://youtu.be/RbzBeJSHF7g

---

### Docker Hub Images

The following images were built and pushed to Docker Hub.

| Service | Docker Hub Repository |
|-------|-----------------------|
| Order Service |https://hub.docker.com/repository/docker/hycst/8915-lab5-order-service |
| Product Service | https://hub.docker.com/repository/docker/hycst/8915-lab5-product-service |
| Store Front | https://hub.docker.com/repository/docker/hycst/8915-lab5-store-front|

---

### Running the Application

docker compose up

###  docker-compose.yaml (individual file in repo)

services:

  rabbitmq:
    image: rabbitmq:3-management
    ports:
      - "5672:5672"
      - "15672:15672"
    environment:
      - RABBITMQ_DEFAULT_USER=myuser
      - RABBITMQ_DEFAULT_PASS=mypassword

  order-service:
    image: hycst/8915-lab5-order-service:latest
    ports:
      - "3000:3000"
    environment:
      - RABBITMQ_CONNECTION_STRING=amqp://myuser:mypassword@rabbitmq:5672/
      - PORT=3000
    depends_on:
      - rabbitmq

  product-service:
    image: hycst/8915-lab5-product-service:latest
    ports:
      - "3030:3030"
    environment:
      - PORT=3030

  store-front:
    image: hycst/8915-lab5-store-front:latest
    ports:
      - "80:80"
    environment:
      - VUE_APP_ORDER_SERVICE_URL=http://order-service:3000
      - VUE_APP_PRODUCT_SERVICE_URL=http://product-service:3030
    depends_on:
      - product-service
      - order-service

## Challenges and Learnings

When wprking on lab5, I learned how to containerize microservices using Docker:
  -  Used Docker Compose to orchestrate multiple containers.
  -  Built and pushed Docker images to Docker Hub.
  -  Configured services to communicate inside the Docker network.
