

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
