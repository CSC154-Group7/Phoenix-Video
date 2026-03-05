# CSC154 SP2026

# Phoenix Video Rental  
## Software Requirements Specification  
### Version 1

**Team Number:** Group7  
**Project Manager:** Krithika Krishnan  
**Team Members:** Yuki Fukushima, Brannon Christopher Copeland, Francis Giles, Makalo Charles  

---

# Revisions

| Version | Primary Author(s) | Description of Version | Date Completed |
|----------|------------------|------------------------|----------------|
| 1.0 | Group 7 | Initial version of SRS including project objectives, requirements, and use cases | Mar 03/26 |
| 1.1 | Group 7 | Added Use Case tables and formatted all requirements (BR, UR, FR, NFR, IR) | Mar 03/26 |

---

# Review History

| Reviewer | Version Reviewed | Date |
|------------|------------------|------|
| Instructor / Peer Reviewer | | |
| Instructor / Peer Reviewer | | |

---

# Table of Contents

1. Introduction  
2. Project Objectives  
3. Project Scope  
4. Project Overview  
5. Project Description  
6. User Stories  
7. Use Cases  
8. Project Assumptions and Dependencies  
9. Project Collaboration and Documentation  
10. Project Management  
11. Requirements Specification  
    - Business Requirements  
    - User Requirements  
    - Functional Requirements  
    - Non-Functional Requirements  
    - Implementation Requirements  

---

# 1. Introduction

## 1.1 Project Objectives

The objective of the Phoenix Video Rental System is to develop a web-based application that allows customers to browse, rent, and return movies online. The system will manage movie inventory, customer accounts, and rental transactions efficiently.

---

## 1.2 Project Scope

### Included Features
- User registration and login  
- Browse and search movies  
- Rent and return movies  
- Admin inventory management  

### Excluded Features
- Online movie streaming  
- Physical delivery services  
- Mobile application (Version 1)  

---

## 1.3 Project Overview

The project will follow Agile methodology with multiple sprints including planning, development, testing, and deployment. The final delivery will be a working web application with database integration and documentation.

---

# 2. Project Description

## 2.1 Project Features / Functions

- User registration and authentication  
- Movie browsing and search functionality  
- Movie rental and return tracking  
- Admin dashboard for inventory management  
- Rental history tracking  

---

# 3. User Stories

- As a customer, I want to create an account so that I can rent movies.  
- As a customer, I want to search for movies so that I can find titles easily.  
- As an admin, I want to manage movie inventory so that records stay updated.  
- As a customer, I want to view my rental history so that I can track past rentals.  

---

# 4. Use Cases

## UC1 – User Registration

- **Actor:** New Customer  
- **Precondition:** User does not already have an account  

### Main Flow
1. User enters personal information  
2. System validates the information  
3. System creates new account  
4. Confirmation message displayed  

### Alternate Flow
- If email already exists, system displays error message  

### Postcondition
- New user account stored in database  

---

## UC2 – Rent Movie

- **Actor:** Registered Customer  
- **Precondition:** User logged in and movie available  

### Main Flow
1. User searches for movie  
2. User selects movie  
3. User clicks Rent  
4. System updates inventory  
5. Confirmation message displayed  

### Alternate Flow
- If movie unavailable, system displays “Out of Stock”  

### Postcondition
- Rental transaction saved and inventory updated  

---

## UC3 – Manage Movie Inventory

- **Actor:** Admin  
- **Precondition:** Admin logged in  

### Main Flow
1. Admin selects Add/Edit movie  
2. Admin enters movie details  
3. System validates information  
4. System updates database  

### Alternate Flow
- If required fields missing, system shows validation error  

### Postcondition
- Movie inventory updated successfully  

---

# 5. Project Assumptions and Dependencies

- Users have internet access  
- Team uses GitHub and Jira  
- MySQL database available  

---

# 6. Project Collaboration and Documentation

The team will use:
- Jira for sprint tracking  
- GitHub for version control  
- Microsoft Teams for communication  
- Google Drive for document sharing  

---

# 7. Project Management

The team will follow Agile Scrum methodology with 3-week sprints, sprint planning meetings, and sprint retrospectives.

---

# 8. Requirements Specification

---

## 8.1 Business Requirements

| ID | Description | MoSCoW |
|----|------------|--------|
| BR1 | Provide online platform to manage rentals, customers, and payments | M |
| BR2 | Improve operational efficiency by reducing paperwork | M |
| BR3 | Ensure accurate tracking of inventory and transactions | M |
| BR4 | Enhance customer satisfaction with faster processing | S |
| BR5 | Provide management reporting capabilities | S |
| BR6 | Support future expansion (cloud, online payments) | C |
| BR7 | Give users suggestions based on previously rented items | C |
| BR8 | Add Website theming or accessibility options for those who prefer personalization or are disabled (background color, high contrast, screen reader) | C |
| BR9 | The Website should have a support bot that users can chat to if they encounter problems with the website or purchasing rentals | W |

---

## 8.2 User Requirements

| ID | Description | MoSCoW |
|----|------------|--------|
| UR1 | Secure user registration and login | M |
| UR2 | Manage customer records | M |
| UR3 | Manage movie records and genres | M |
| UR4 | Track inventory status | M |
| UR5 | Process rentals and returns | M |
| UR6 | View active and overdue rentals | M |
| UR7 | Track payment details | M |
| UR8 | View rental and payment history | S |
| UR9 | Generate basic reports | C |
| UR10 | Website theming & personalization | C |

---

## 8.3 Functional Requirements

| ID | Description | MoSCoW |
|----|------------|--------|
| FR1 | Authenticate users securely | M |
| FR2 | Manage customer records in database | M |
| FR3 | Manage movie records in database | M |
| FR4 | Manage inventory copies | M |
| FR5 | Auto-update inventory status | M |
| FR6 | Record rental transactions | M |
| FR7 | Calculate overdue status | M |
| FR8 | Record payment transactions | M |
| FR9 | View rental/payment history | S |
| FR10 | Generate basic reports | C |

---

## 8.4 Non-Functional Requirements

| ID | Description | MoSCoW |
|----|------------|--------|
| NFR1 | 99% availability during business hours | M |
| NFR2 | 3-second response time | M |
| NFR3 | Encrypt passwords and sensitive data | M |
| NFR4 | Role-based access control | M |
| NFR5 | Maintain data integrity | M |
| NFR6 | User-friendly interface | S |
| NFR7 | Support 50 concurrent users | S |
| NFR8 | Daily automated backups | C |

---

## 8.5 Implementation Requirements

| ID | Description | MoSCoW |
|----|------------|--------|
| IR1 | Use JavaScript/Python backend | M |
| IR2 | Use PostgreSQL database | M |
| IR3 | Use VS Code and GitHub | M |
| IR4 | Deploy on web server environment | M |
| IR5 | Follow Agile/Scrum methodology | S |
| IR6 | Future cloud deployment | C |

---