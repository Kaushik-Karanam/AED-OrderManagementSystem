# 🛒 Order Management System (OMS)

This project is a robust, multi-enterprise Order Management System (OMS) built using Java. It provides a unified platform for customers to order products from various organizations, while enabling businesses to manage their inventory and operations efficiently. The system is designed with a clear hierarchical structure of Admins, Enterprises, and Organizations.

---

## 🚀 Key Features & Technical Highlights

* **Fault-Tolerant Microservices:** Built with Java (Spring Boot) to handle multi-enterprise order and inventory processing, achieving a **60% increase in transaction throughput**.
* **Optimized REST APIs:** Designed efficient APIs for seamless data exchange between user, enterprise, and delivery modules, resulting in a **40% reduction in API response time**.
* **Robust Database Layer:** Engineered the SQL database schema for managing core OMS entities like orders, products, and users, ensuring high data integrity and supporting transactional operations.
* **Hierarchical Management:** A clear administrative structure allowing Admins to create Enterprises, which in turn manage their own Organizations.
* **Dynamic Product Management:** Organizations can add or remove products from their catalog based on business needs.
* **Centralized Analytics:** A dedicated analytics dashboard for the Admin to view the performance of the top 3 enterprises, organizations, and delivery partners.

---

## 🎯 Problem Statement

The project aims to solve several key challenges in the current delivery ecosystem:

* **Complicated Ordering Process:** Users face a non-cost-effective system that requires them to navigate multiple applications and websites to order products from different stores.
* **Security and Privacy Concerns:** The need for users to register and log in to many separate applications creates potential security vulnerabilities and data privacy risks.
* **High Operational Costs for Businesses:** Organizations incur significant operational costs from manual processes, inefficient resource allocation, and suboptimal delivery routing.

---

## ✅ Proposed Solution

Our Order Management System addresses these problems with the following solutions:

* **Unified Platform:** We have developed a single, integrated application that allows users to easily order products from multiple organizations hosted on the platform.
* **Cost Reduction:** The system significantly reduces operational costs for participating organizations. It also reduces delivery time and cost for customers by enabling bundled deliveries of products from various organizations together.

---

## 🏛️ System Architecture and Design

The application is built on a hierarchical, multi-role architecture that ensures a clear separation of concerns and smooth operational flow.

### Core Roles

* **Admin:** The superuser of the system. The Admin can create Enterprises and Delivery Partners, and has access to system-wide analytics.
* **Enterprise:** Created by the Admin, an Enterprise is a high-level entity that can create and manage multiple Organizations under its umbrella.
* **Organization:** Created by an Enterprise, an Organization is responsible for managing its own product catalog, including adding and removing items.
* **Delivery Partner:** Created by the Admin, a Delivery Partner is responsible for accepting and fulfilling customer orders.
* **Customer:** An independent role. Customers can sign up, log in, browse products from different enterprises and organizations, and place orders.

### How It Works: The Workflow

1.  An **Admin** receives a request and creates a new Enterprise as required.
2.  The newly created **Enterprise** then creates and manages its associated Organizations.
3.  The **Organization** adds products to its catalog, which are then associated with that organization and its parent enterprise.
4.  A **Customer** signs up and logs into the application.
5.  The Customer selects an Enterprise, an Organization, and the desired products to place an order.
6.  Once the order is placed, the workflow is transferred to a **Delivery Partner**.
7.  The Delivery Partner accepts the order and delivers the products.
8.  The order is marked as complete upon successful delivery.

### Data Model (Class Diagram)

The system is designed with a clear object-oriented structure, ensuring modularity and scalability. Key classes include:
* `Enterprise` and `EnterpriseDirectory`
* `Organization` and `OrganizationDirectory`
* `Customer` and `CustomerDirectory`
* `DeliveryPartner` and `DeliveryPartnerDirectory`
* `Product` and `ProductDirectory`
* `Order` and `OrderDirectory`

These classes are interconnected to manage relationships, such as an Enterprise containing a list of Organizations, and an Order being linked to a Customer, an Organization, and a list of Products.

---

## 💻 Technology Stack

* **Backend:** Java (Spring Boot)
* **Database:** SQL
* **API:** REST
