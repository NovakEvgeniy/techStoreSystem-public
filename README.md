# techStoreSystem

**techStoreSystem is a web-based e-commerce application for selling computer technology and hardware in Germany and the UK.**

**Keywords:** Java, Spring Boot, Spring MVC, Spring Data JPA, Hibernate, MySQL, Maven, HTML5,CSS3, JavaScript, AJAX, REST API, Client-Side Rendering (CSR), Feature-BasedArchitecture, Modular Monolith, Layered Architecture, UI-First Development, Internet Store, E-Commerce, Computer Technology Store, Computer Hardware Store, Online Computer Store, Tech Store System, Product Catalog, Computer Hardware Catalog, Gaming Hardware Store, Gaming PC Store, Gaming Laptops, Desktop PCs, Graphics Cards, GPUs, Computer Components, Product Management, Product Specifications, Shopping Cart, Online Checkout, Order Management, Payment Processing, Customer Reviews, Product Reviews, Promotions, FAQ, Site Content, Admin Panel, E-Commerce Administration, Germany Online Store, UK Online Store, EUR GBP Pricing, English German Localization.

## 1.  About the Project

### 1.1. Purpose

- The **techStoreSystem** is a web-based application for managing an online computer technology and hardware store.

### 1.2. System Users

- The current MVP version supports two user types:
- **User with the ADMIN role** — manages products, catalog data, orders, reviews, promotions, FAQ and site content.
- **User with the CUSTOMER role** — browses the store, views products and specifications, uses the shopping cart and checkout, and can place orders.
- The current MVP is a demonstration version; therefore, access to the application and its role-specific functionality is not restricted by user accounts, login credentials, or passwords.


### 1.3. Scope - The system is designed for:

- managing the product catalog, including categories, brands, products, prices, descriptions, and technical specifications;
- managing product images and multilingual product information (EN / DE);
- providing product browsing, searching, filtering, and viewing of product details;
- managing shopping carts and customer orders;
- supporting checkout and online payment through Stripe and PayPal;
- managing customer reviews, promotions, FAQ, and website content;
- providing customers with information about delivery, payment, returns, guarantees, and company contacts;
- supporting administration of the online store through an administrative panel;
- supporting online sales of computer hardware in the German and UK markets;
- providing a modern, responsive, and user-friendly e-commerce experience for customers.

## 2. System Data

### 2.1. Input Data

- Category data
- Brand data
- Product data
- Product images
- Product prices in EUR / GBP
- Product descriptions and technical specifications
- Multilingual product data (EN / DE)
- Customer data
- Shopping cart data
- Order data
- Payment method data
- Customer review data
- Promotion data
- FAQ data
- Website content data

### 2.2. Output Data

- Product catalog
- Product details and technical specifications
- Shopping cart
- Order confirmation
- Customer order data
- Payment information
- Customer reviews
- Promotions and special offers
- FAQ and website content
- Administrative management data

## 3. Architecture

### 3.1. Frontend

- **Web Interface Architecture:** Client-Side Rendering (CSR) application based on feature modules
- **Rendering:** Client-side rendering using JavaScript and HTML templates
- **Technology Stack:** HTML5, CSS3, JavaScript (ES6), AJAX (Fetch API)
- **Client–Server Communication:** Asynchronous communication with backend REST API endpoints using AJAX requests

### 3.2. Backend

- **Architecture:** Feature-Based Modular Monolith with layered architecture (Entity, Controller, Service, Repository)
- **Database:** MySQL, Spring Data JPA, Hibernate
- **Security:** Custom session-based authentication without Spring Security
- **Technology Stack:** Java 21, Spring Boot, Spring Data JPA, Hibernate, Maven

## 3. Architecture

### 3.1. Frontend

- Web Interface Architecture: Client-Side Rendering (CSR) application based on feature modules
- Rendering: Client-side rendering using JavaScript and HTML templates
- Technology Stack: HTML5, CSS3, JavaScript (ES6), AJAX (Fetch API)
- Client–Server Communication: Asynchronous communication with backend REST API endpoints using AJAX requests

### 3.2. Backend

- Architecture: Feature-Based Modular Monolith with layered architecture (Controller → Service → Repository → Entity)
- Domain Model: Plain Java domain classes separated from persistence entities
- Persistence: Spring Data JPA with separate persistence entities and repositories
- Database: MySQL
- Technology Stack: Java 21, Spring Boot, Spring Data JPA, Hibernate, Maven
- Security: In this demonstration MVP version, custom session-based authentication is used without Spring Security


## 4. Launch and Deployment

### 4.1. Prerequisites

-   Java 21
-   Maven 3.6+
-   MySQL 8.0+

### 4.2. Run the Project Using the Executable JAR File

#### 4.2.1. Create the Database

- Create a new database named `tech_store` using the following SQL command:

```sql
CREATE DATABASE tech_store
CHARACTER SET utf8mb4
COLLATE utf8mb4_unicode_ci;
```

#### 4.2.2. Create an External application.properties File

- Create a file named application.properties in the same folder where the executable JAR will be placed.
- Add the following configuration:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/tech_store
spring.datasource.username=YOUR_MySQL_USERNAME
spring.datasource.password=YOUR_MySQL_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.database-platform=org.hibernate.dialect.MySQLDialect
```
- Replace `YOUR_MySQL_USERNAME` and `YOUR_MySQL_PASSWORD` with your own MySQL username and password.
- The application uses Hibernate (`spring.jpa.hibernate.ddl-auto=update`), which automatically creates all required database tables when the application is started for the first time.

#### 4.2.3. Download the Executable JAR

- Download the executable JAR from the link below and place it in the same folder as `application.properties`

👉 [** Download techStoreSystem-0.0.1-SNAPSHOT.jar**](https://github.com/NovakEvgeniy/techStoreSystem-public/releases/download/v1.0.0/techStoreSystem-0.0.1-SNAPSHOT.jar)

#### 4.2.4. Run the Application

- Run the following command from the folder containing both files: 

``` bash
java -jar techStoreSystem-0.0.1-SNAPSHOT.jar
```

#### 4.2.5. Launch in the Browser

-   **URL: http://localhost:8080/**

## 5. Getting Started

### 5.1. User Roles Functions

#### 5.1.1  **Administrator Guide**

- The **Administrator** creates and maintains the store reference data in the following order of established relationships:
- **1.** Categories — Create and manage product categories. All data are entered manually.
- **2.** Brands — Create and manage product brands. All data are entered manually.
- **3.** Products — Create and manage products, including names, models, descriptions, prices, categories, brands, and active status. All data are entered manually.
- **4.** Product Specifications — Add and manage technical specifications for products. Products are selected from the existing product database, while specification values are entered manually.
- **5.** Site Content — Create and manage website pages and content.
- **6.** FAQ — Create and manage frequently asked questions and answers.
- **7.** Promotions — Create and manage promotions and special offers.
- **8.** Reviews — View and manage customer reviews.
- **9.** Orders — View and manage customer orders created through the checkout process.

#### 5.1.2  **Customer Guide**

- The **Customer** uses the store to browse products and place orders:
- **1.** Catalog — Browse the available products and filter them by category, brand, and price.
- **2.** Product Details — View product information, images, descriptions, prices, and technical specifications.
- **3**. Cart — Add products to the shopping cart, change quantities, and review the selected products.
- **4**. Checkout — Enter customer and delivery information, select a payment method, and place an order.
- **5.** Payment — Select Stripe or PayPal as the online payment method.
- **6.** Order Confirmation — Receive confirmation after successfully placing an order.

## 6. Application Access and Limitations

- The current MVP version is available for demonstration, and the main store functionality is accessible to all visitors.
- The current MVP operates without authentication, login credentials, passwords, or user accounts. Customer order history is not implemented in the current MVP version.

## 7. Future Development

- The application is intended as an MVP for demonstration, evaluation, and further development.
- A conventional access control system with user registration, authentication, authorization, and role-based access can be added according to the customer's requirements.
- Other additional features and system modifications can be implemented according to future customer requirements.

## 8. Licensing

-   This software is proprietary.
-   The source code is closed and represents the intellectual property of the author.

## 9. Commercial Use

-   Source code and extended project versions are provided by agreement.

## 10. Contacts
 
-   **Author:** **Evgeniy Novak**
-   **Email:** **novakevgeniy1953@gmail.com**
-   **GitHub:** **https://github.com/NovakEvgeniy?tab=repositories**




