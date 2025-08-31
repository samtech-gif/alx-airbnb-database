# Project Requirements

## 1. Project Overview

A web-based property booking platform where users can list properties, book them, make payments, leave reviews, and communicate via messages.  
**Roles:** Guest, Host, Admin

---

## 2. Functional Requirements

### User Management

-   Users can register, log in, and update their profile.
-   Roles: guest, host, admin.
-   Passwords are securely stored (hashed).

### Property Management

-   Hosts can create, update, and delete property listings.
-   Properties have attributes: name, description, location, price per night, created_at, updated_at.

### Booking System

-   Guests can book available properties.
-   Booking includes start and end dates, total price, and status (pending, confirmed, canceled).
-   Users can view their booking history.

### Payment

-   Guests can pay for bookings using credit card, PayPal, or Stripe.
-   Payments are linked to bookings and recorded with timestamp and amount.

### Review System

-   Guests can leave reviews and ratings (1–5) for properties they booked.
-   Reviews include comments and rating.

### Messaging

-   Users can send messages to each other.
-   Messages include sender, recipient, content, and timestamp.

---

## 3. Non-Functional Requirements

-   System must handle at least 1000 concurrent users.
-   Response time for pages should be < 2 seconds.
-   Must be mobile responsive.
-   Security: Passwords must be hashed; sensitive data encrypted.

---

## 4. Database / Technical Requirements

### Entities

-   User
-   Property
-   Booking
-   Payment
-   Review
-   Message

### Attributes

-   See ERD for detailed attributes (e.g., user_id, property_id, booking_id, etc.)

### Relationships

-   User → Property (host)
-   User → Booking (guest)
-   Booking → Payment
-   User → Review → Property
-   User → User (Messages)

---

## 5. ERD Diagram

![ERD](docs/ERD_Diagram.png)

> Editable version available at [ERD_Diagram.drawio](docs/ERD_Diagram.drawio)

---

## 6. Constraints & Indexing

-   Unique constraints on user emails.
-   Foreign key constraints as per ERD.
-   Primary keys indexed.
-   Additional indexing:
    -   User.email
    -   Property.property_id
    -   Booking.booking_id
