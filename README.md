# Phoenix-Video-Rentals

Phoenix Video is a movie rental inventory management system that helps businesses track movie availability, manage rentals and returns, and maintain accurate inventory record





# Tech Stack with Reasoning:

### Python

####  High-level coding language with design philosphy based on code readability and indentation.

-  Easier compared to most OO languages for learning and debugging.
-  Easy code readability ensures anyone with python knowledge can understand the logic.
-  High-level coding language with the ability to handle complex details allowing our team to focus more on the logic and less on syntax.
-  Very flexible coding language that can be front-end or back-end. Used as backend at companies such as Netflix, Instagram, and Spotify.

### Django

#### High-level Python web framework

- Automatically intergratted with a admin panel which fulfils our need for an interface to edit and add movies to the rental system.
- Has inventory tracking allowing admins to view inventory statuses and ensures accurate tracking of inventory.
- Allows Administrators to not only use standard SQL code but also allows us to interact with the database with python code as well.
- Built in security ensuring users are authenticated and can login securely. Furthermore, roles ensuring that administrators and users on the site can use it at they intend.
    - EX: Admin can be able to configure the website while a user will only be allowed to do simple movie renting. )

### Postgresql

#### Open-source relational database management system (RDBMS) emphasizing extensibility and SQL compliance. 

- Benifit 1
- Benefit 2
- Benefit 3
- Benefit 4



## Database Design
This page documents the database design for the Phoenix Video Rental system. The design supports customer management, movie rentals, inventory tracking, payments, and movie genres while keeping the structure simple and easy to understand.

### ER Diagram
Entity Relationship (ER) Diagram

<img width="766" height="596" alt="ER Diagram" src="https://github.com/user-attachments/assets/e300f9f7-5402-428e-8ce2-18aa82d3e5db" />


### The ER diagram illustrates:

Primary keys (PK) for uniquely identifying records

Foreign keys (FK) showing how tables are related

One-to-many and many-to-many relationships between entities

 

### Overview
The database is designed to track who rents movies, which movie copies are available, and how payments are handled. Each table has a clear purpose, and relationships ensure data stays accurate and connected.

### Tables and Their Purpose
Customers
Stores customer contact information.

Each customer is identified by a unique customer_id.

Customers can have multiple rentals over time.

Movies
Stores movie details such as title, release year, runtime, MPAA rating, and description.

Each movie is identified by movie_id.

Inventory
Tracks individual copies of movies.

Each inventory record represents one physical copy.

Status indicates whether the copy is Available, Rented, or Unavailable.

Inventory items are linked to a specific movie.

Rentals
Records each rental transaction.

Links a customer to a specific inventory copy.

Tracks rental, due, and return dates.

Payments
Stores payment information for rentals.

Each payment is linked to a rental.

Tracks payment date, amount, method, and status.

Genres
Stores movie genre names (e.g., Action, Comedy, Drama).

Movie_Genre
Connects movies and genres.

Allows movies to belong to multiple genres and genres to include multiple movies.

Table Relationships
A customer can have many rentals.

A movie can have many inventory copies.

An inventory copy can be rented many times over its lifetime.

A rental can have one or more payments.

Movies and genres have a many-to-many relationship using the Movie_Genre table.

Why This Design Works
Keeps rental operations organized and easy to track.

Prevents duplicate or inconsistent data.

Makes it easy to check availability of movie copies.

Supports payment tracking without overcomplicating the system.

Scales well if more features are added later.




## Update database & user identification design

<img width="766" height="761" alt="Phoenix video rental ER Diagram drawio" src="https://github.com/user-attachments/assets/97f4700b-2fda-4c18-bcb4-eda35e0e2841" />

The database design was updated to include a User's table to support user identification and authentication within the system. The Rentals table now includes a processed_by foreign key referencing users.user_id to track which employee processed each rental transaction.

This updated design also supports future features planned for later development phases, including offline data storage, Google login and verification, and user profile customization. The current schema allows these features to be integrated without requiring major structural changes to the database.


## Design email notification system

The Phoenix Video Rental system will include an email notification feature to automatically notify customers about important rental events. Email notifications will be triggered by specific system actions and will use customer email addresses stored in the Customers table.

The system will send notifications for the following events:

Rental confirmation when a movie is rented

Due date reminders before a rental are due

Overdue notices if a rental is not returned on time

Payment confirmation after a successful payment

Email messages will be generated using predefined templates and populated with rental, movie, and customer information from the database. The notification service will run through the application backend and will be designed so it can integrate with a standard email service provider during implementation.

