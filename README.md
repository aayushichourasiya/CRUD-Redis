# Redis CRUD Application using Spring Boot

This is a simple Spring Boot application demonstrating CRUD operations using Redis as the in-memory data store. It uses Spring Data Redis and Jedis for Redis interaction.

---

## Tech Stack

- Java
- Spring Boot
- Spring Data Redis
- Jedis
- Lombok

---

## Features

- Add product to Redis
- Get all products
- Get product by ID
- Delete product by ID

---

## Project Structure

- `RedisConfig.java` – Redis configuration using `JedisConnectionFactory` and `RedisTemplate`
- `Product.java` – Redis entity with `@RedisHash`
- `ProductDAO.java` – Repository layer using `RedisTemplate` operations
- `RedisController.java` – REST endpoints for CRUD operations

---

## Prerequisites

- Java 11+
- Maven
- Redis server installed and running locally on port 6379

---

## Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/your-username/redis-crud-app.git
   cd redis-crud-app
   
2. **Start Redis**<br>
    Make sure Redis is running locally on localhost:6379

    For Mac (Homebrew):

      ```bash
      brew install redis
      brew services start redis

3. **Run the Application**
     ```bash
     ./mvnw spring-boot:run

## API Endpoints
**Create Product**
    
    ```bash
    POST /product
    Content-Type: application/json
    {
      "id": 1,
      "name": "Laptop",
      "qty": 5,
      "price": 75000
    }

**Get All Products**
    
    ```bash
    GET /product

**Get Product by ID**

    ```bash
    GET /product/{id}

**Delete Product by ID**

    ```bash
    Delete Product by ID

---

## Notes

- Redis stores products in a hash with the key "Product"
- Data is not persistent by default unless Redis persistence is enabled
- Use Postman or curl to test endpoints

---

## Author
Auyushi Chourasiya




