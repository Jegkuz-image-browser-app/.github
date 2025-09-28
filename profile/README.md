# Version №1
## Hi there 👋
🚀 Social Platform (Microservices Edition) <br>
Welcome to the Image Sharing Platform repository, a platform built on a microservices architecture. <br>
The goal of this project is to create a focused, Instagram-like application centered on image publishing, viewing, and generating personalized user feeds based on subscriptions.

## Architecture Overview
Architecture: Microservices (Shared Database Pattern) <br>
The project is divided into three core, independent services and a configuration repository. <br>
Services interact via REST API and initially use a shared database model. <br>

### Back-end & Core
Language: Java 17 <br>
Framework: Spring Boot 3
- Authentication Service:
Registration, login, and management of user sessions/tokens (e.g., JWT).
- User Service:
User profiles (name, username). Manages subscriptions and unsubscriptions.
- Post Service:
Handles publishing, likes, comments, and views of posts. Generates the personalized user feed.

### Data & Storage
PostgreSQL (Relational DB): Primary database for transactional data (users, subscriptions, posts, likes). <br>
MongoDB (Document DB): Planned for storing post data (images, likes, comments) for better scalability. <br>
MinIO (Object Storage): Stores and retrieves all profile and post images. <br>

<img width="1428" height="665" alt="image" src="https://github.com/user-attachments/assets/958b7251-55c6-4a5f-a35a-6a921f94d3fe" />

### Front-end
ReactJS. <br>
Tailwind.

## Set Up

Install Docker. (https://www.docker.com/products/docker-desktop/) <br>

Create a directory locally that will contain all the repositories.
Open CMD and first clone infra repository using: <br>
```git clone https://github.com/Jegkuz-image-browser-app/infra.git``` <br>

Go into ```infra``` folder and copy the rest of the services into it: <br>
```git clone https://github.com/Jegkuz-image-browser-app/post_service.git``` <br>
```git clone https://github.com/Jegkuz-image-browser-app/user_service.git``` <br>
```git clone https://github.com/Jegkuz-image-browser-app/authentication_service.git``` <br>

```
/ImageScroller (Root folder)
└── /infra
    ├── docker-compose.yaml
    ├── /auth-service
    ├── /user-service
    └── /post-service
```
