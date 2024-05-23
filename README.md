# Java-API

This project is a Spring Boot application that demonstrates CRUD operations for categories and products. It also showcases pagination and a one-to-many relationship between categories and products.

## Requirements

- Java 11 or later
- Maven 3.6.3 or later
- MySQL Database

## Setup Instructions

1. **Clone the Repository**

    ```bash
    git clone https://github.com/Anirudha2001/Java-API.git
    cd Java-API
    ```

2. **Configure Database**

    Create a database in MySQL:

    ```sql
    CREATE DATABASE category_product_db;
    ```

    Update `src/main/resources/application.properties` with your MySQL database configuration:

    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/category_product_db
    spring.datasource.username=your_username
    spring.datasource.password=your_password
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect
    ```

3. **Build and Run the Application**

    Use Maven to build and run the application:

    ```bash
    mvn clean install
    mvn spring-boot:run
    ```

4. **Test the APIs**

    You can test the APIs using Postman or any other API testing tool. The available endpoints are:

   # Product APIs

### Post - Add Product
Endpoint: `http://localhost:8080/api/v1/products`

### Get - Get all Products
Endpoint: `http://localhost:8080/api/v1/products`

### Get - Get Product by Id
Endpoint: `http://localhost:8080/api/v1/products/{productId}`

### Put - Update Product by Id
Endpoint: `http://localhost:8080/api/v1/products/{productId}`

### Delete - Delete Product by Id
Endpoint: `http://localhost:8080/api/v1/products/{productId}`

### Get - List of all products that belong to a particular categoryId
Endpoint: `http://localhost:8080/api/v1/products/categories/{categoryId}`

# Category APIs

### Post - Add Category
Endpoint: `http://localhost:8080/api/v1/categories`

### Get - Get all categories
Endpoint: `http://localhost:8080/api/v1/categories`

### Get - Get Category by Id
Endpoint: `http://localhost:8080/api/v1/categories/{categoryId}`

### Put - Update Category by Id
Endpoint: `http://localhost:8080/api/v1/categories/{categoryId}`

### Delete - Delete Category by Id
Endpoint: `http://localhost:8080/api/v1/categories/{categoryId}`

