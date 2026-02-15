# 🏨 AirBnb Backend Application (Dev Project)

A **Spring Boot–based backend application** that powers a simplified AirBnB-like platform.
The system supports **hotel listing, room management, booking, dynamic pricing, authentication, and payment workflows**, designed with clean architecture and scalability in mind.

## 🚀 Features

* 🔐 **Authentication & Authorization**

  * JWT-based authentication
  * Role-based access (Admin / User)

* 🏨 **Hotel & Room Management**

  * Create and manage hotels
  * Room inventory and availability tracking
  * Admin room controls

* 🔎 **Search & Browse**

  * Hotel search with pricing details
  * Availability-based browsing

* 📅 **Booking System**

  * Room booking and guest handling
  * Booking status tracking
  * Inventory updates on booking

* 💰 **Dynamic Pricing Engine**

  * Strategy-based pricing implementation
  * Surge, occupancy, urgency, and holiday pricing support

* 💳 **Payments Integration**

  * Stripe-based checkout flow
  * Webhook handling for payment updates

* 🧾 **Global API Handling**

  * Unified API responses
  * Centralized exception handling

## 🧱 Tech Stack

* **Java 17**
* **Spring Boot**
* **Spring Security (JWT)**
* **Spring Data JPA**
* **PostgreSQL**
* **Stripe API**
* **Maven**

## 📁 Project Structure

```
src/main/java/com/codingshuttle/projects/airBnbApp
│
├── advice          → Global response & exception handling
├── config          → CORS, Mapper, Stripe configuration
├── controller      → REST API controllers
├── dto             → Request & response DTOs
├── entity          → JPA entities & enums
├── exception       → Custom exceptions
├── repository      → Spring Data JPA repositories
├── security        → JWT & security configuration
├── service         → Business logic layer
├── strategy        → Dynamic pricing strategies
└── util            → Utility classes
```

## 🔐 Security

* JWT tokens are used for securing APIs
* Role-based endpoint access
* Sensitive keys are injected via **environment variables**

## ⚙️ Configuration

### `application.properties` (example)

```properties
spring.application.name=airBnbApp

spring.datasource.url=jdbc:postgresql://localhost:5432/airbnb
spring.datasource.username=YOUR_DB_USERNAME
spring.datasource.password=YOUR_DB_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

server.servlet.context-path=/api/v1

jwt.secretKey=YOUR_JWT_SECRET

frontend.url=http://localhost:8080

stripe.secret.key=${STRIPE_SECRET_KEY}
stripe.webhook.secret=${STRIPE_WEBHOOK_SECRET}
```

## ▶️ Running the Application

### Prerequisites

* Java 17+
* Maven
* PostgreSQL
* Stripe test account (for payments)

### Steps

```bash
# clone repository
git clone <your-repo-url>

# move into project
cd airBnbApp

# run application
./mvnw spring-boot:run
```

The backend will start at:

```
http://localhost:8080/api/v1
```

## 🧪 Testing

* Unit and integration tests are under:

```
src/test/java
```

Run tests using:

```bash
./mvnw test
```

## 📌 Notes

* This project is intended for **learning and development purposes**
* Designed with **clean layering and extensibility**
* Pricing logic follows **Strategy Pattern**
* Easy to extend for microservices or frontend integration

## 📄 License

This project is for **educational and development use only**.
