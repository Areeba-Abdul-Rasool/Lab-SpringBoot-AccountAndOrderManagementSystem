# **Lab-SpringBoot-AccountAndOrderManagementSystem**

This repository contains a comprehensive Spring Boot application for managing user accounts, restaurant menu items, and orders. Designed for both administrators and regular users, the application emphasizes role-based access control, real-time validation, and seamless integration with an Oracle SQL database. The user-friendly interface is powered by Thymeleaf templates, offering intuitive navigation for all users.

---

## **Features**  
### **1. User Management**  
- **<span style="color:blue;">Account Creation</span>**: Users can create accounts with real-time validation for unique `userID` and `email`.  
- **<span style="color:blue;">Role-Based Access Control</span>**:  
  - **Super Admin**: Full control over user and admin management.  
  - **Admin**: Limited to managing regular users.  
  - **Regular Users**: Limited to personal profile and order management.  
- Automatic assignment of default roles (`User`) and recording of account creation timestamps.  

### **2. Restaurant Management**  
- **<span style="color:blue;">Manage Categories</span>**: Add, edit, and delete categories stored in the database.  
- **<span style="color:blue;">Manage Items</span>**: CRUD operations for restaurant menu items, with each item linked to a category via a foreign key.  

### **3. Order Management**  
- **<span style="color:blue;">User Features</span>**:  
  - Browse and view available items.  
  - Place orders with default "Cash on Delivery" payment method.  
  - Track order status using a unique `Order ID`.  
  - View complete order history.  
- **<span style="color:blue;">Admin Features</span>**:  
  - View all orders placed by users.  
  - Update order statuses ("Pending," "Processed," "Completed").  
  - Automatic stock management for completed orders.  

### **4. Profile Management**  
- Users can update personal details, such as passwords and contact information, through a secure interface.  

---

## **Technologies Used**  
- **Frontend**: Thymeleaf, HTML, CSS  
- **Backend**: Spring Boot, REST APIs  
- **Database**: MySQL Databe, Hibernate ORM  

---

## **How It Works**  
- The application ensures data consistency and security through role-based restrictions.  
- All sensitive actions (e.g., role assignment, order status updates) are limited to authorized users based on their roles.  
- The database schema includes well-defined relationships for seamless data handling between users, categories, items, and orders.  

---

## **Setup Instructions**  

1. Clone the repository:  
   ```bash
   git clone https://github.com/<your-username>/Lab-SpringBoot-AccountAndOrderManagementSystem.git
2. Navigate to the project directory and import it into IntelliJ or any Spring Boot-compatible IDE.
3. Configure the application.properties file with your Oracle database credentials.
4. Run the application using Maven or the IDE's Spring Boot run configuration: ./mvnw spring-boot:run
5. Open a browser and navigate to <span style="color:blue;"> http://localhost:8080</span> to access the application.
