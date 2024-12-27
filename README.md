Here's an improved README for the **Xwiggy** project:

---

# Xwiggy 🍔🍕  
**A Modern Food Ordering System built with Angular, Spring Boot, and MySQL.**  
Xwiggy implements the MVC architecture and provides a seamless user experience for customers and merchants, including food ordering, cart management, payments, and menu customization.

---

## Table of Contents
1. [About the Project](#about-the-project)  
2. [Features](#features)  
3. [Technologies Used](#technologies-used)  
4. [Pre-Requisites](#pre-requisites)  
5. [Installation](#installation)  
6. [Running the Project](#running-the-project)  
   - [On Host Machine](#on-host-machine)  
   - [Using Vagrant Box](#using-vagrant-box)  
7. [REST API Endpoints](#rest-api-endpoints)  
8. [Screenshots](#screenshots)  
9. [Author](#author)

---

## About the Project
Xwiggy is a food ordering system that uses Angular (v8) for the frontend, Spring Boot (v2.1.6) for the backend, and MySQL for database support. It allows users to browse food menus, place orders, and make payments. Merchants can manage their menus and update food inventory seamlessly.

---

## Features
### User Features:
- Login and Registration.
- Browse available food items with quantity details.
- Add items to the cart and place orders.
- Payment integration with card details (simulated).  
- Automatic updates of the database and menu after purchase.

### Merchant Features:
- Login and Registration for merchants.
- Manage menu items (add/update quantities).
- Real-time updates without page refresh.

### Additional:
- RESTful APIs for server-client communication.
- Vagrant-based deployment for ease of development.
- Database initialization scripts for rapid setup.

---

## Technologies Used
- **Frontend:** Angular 8 with Routing  
- **Backend:** Spring Boot 2.1.6  
- **Database:** MySQL  
- **API:** Java Persistence API (JPA) with RESTful endpoints  
- **DevOps:** Vagrant and Oracle VirtualBox for VM-based deployment  

---

## Pre-Requisites
- Java 8 or higher  
- MySQL Server  
- Node.js and npm  
- Vagrant and Oracle VirtualBox (for VM-based deployment)  

---


---

## Running the Project
### On Host Machine
1. **Frontend Setup:**  
   - Navigate to `xwiggy-app`:  
     ```bash
     cd xwiggy-app
     ```
   - Build and serve the Angular app:  
     ```bash
     ng build
     ng serve
     ```
   - Access the frontend at: `http://localhost:4200`

2. **Backend Setup:**  
   - Start your MySQL server and create the database:
     ```bash
     mysql -u root -p
     source src/main/resources/dbScripts/ddl.sql
     ```
   - Update `src/main/resources/application.properties` if the MySQL port differs.  
   - Start the Spring Boot application:  
     ```bash
     cd xwiggy-back
     mvn spring-boot:run
     ```
   - Access the backend at: `http://localhost:8080`

---


## REST API Endpoints
| **Endpoint**       | **Method** | **Functionality**                              |
|---------------------|------------|-----------------------------------------------|
| `/login`            | POST       | Validates login and returns user object.      |
| `/register`         | POST       | Registers a new user or merchant.             |
| `/checkUserName`    | POST       | Checks if a username already exists.          |
| `/menu`             | GET        | Fetches the list of available food items.     |
| `/cart`             | POST       | Calculates total cost of items in the cart.   |
| `/changeDB`         | GET        | Updates database after a purchase.            |

--- 

**Note:** This project is in an early stage and may have bugs. Contributions are welcome! 🚀