
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
https://github.com/hycst/cst8915-lab5/blob/main/docker-compose.yml

## Challenges and Learnings

When wprking on lab5, I learned how to containerize microservices using Docker:
  -  Used Docker Compose to orchestrate multiple containers.
  -  Built and pushed Docker images to Docker Hub.
  -  Configured services to communicate inside the Docker network.
