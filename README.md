
# CST8915 Lab 5 – Containerizing the Algonquin Pet Store with Docker

**Course:** CST8915 Full-stack Cloud-native Development  
**Professor:** Ramy Mohamed  
**Student:** Hesheng Yang  

---

### Demo Video

[https://youtube.com/YOUR_VIDEO_LINK_HERE](https://youtu.be/RbzBeJSHF7g)

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

## Technologies Used

- Docker – containerization platform
- Docker Compose – multi-container orchestration
- RabbitMQ – messaging system between services
- Node.js – backend implementation for the order-service
- Python – backend implementation for the product-service
- Vue.js – frontend user interface

## Challenges and Learnings

When wprking on lab5, I learned how to containerize microservices using Docker:
  -  Used Docker Compose to orchestrate multiple containers.
  -  Built and pushed Docker images to Docker Hub.
  -  Configured services to communicate inside the Docker network.
