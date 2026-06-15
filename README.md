# Football Ticket Booking System - Database Design & SQL Queries

## Overview & Objectives

This assignment is designed to evaluate your understanding of database table design, ERD relationships, and intermediate-to-advanced SQL queries. You will work with a simplified **Football Ticket Booking System** database.

## Database Design & Business Logic

The system manages football fans purchasing tickets, upcoming tournament matches, and individual ticket booking receipts.

### Business Logic & Schema Architecture

Your database design must handle these real-world scenarios by implementing the following exact table fields:

### 1. Users Table

This table tracks all administrative staff and customers who use the platform.

| **Field Name** | **What the Field Does**                                          |
| -------------- | ---------------------------------------------------------------- |
| `user_id`      | Unique identification number for each registered user.           |
| `full_name`    | Stores the first and last name of the user.                      |
| `email`        | Stores the user's mail address used for login.                   |
| `role`         | Defines access permissions (`Ticket Manager` or `Football Fan`). |
| `phone_number` | Stores the contact mobile number of the fan.                     |

### 2. Matches Table

This table catalogs the tournament events, stadium logistics, and baseline ticket inventory pricing.

| **Field Name**        | **What the Field Does**                                                                   |
| --------------------- | ----------------------------------------------------------------------------------------- |
| `match_id`            | Unique identification number for each football match.                                     |
| `fixture`             | Tracks the two competing teams (e.g., _Real Madrid vs Barcelona_).                        |
| `tournament_category` | The league or cup title (e.g., _Champions League_, _Premier League_).                     |
| `base_ticket_price`   | The foundational price for a single standard entry seat.                                  |
| `match_status`        | Current ticket availability state (`Available`, `Selling Fast`, `Sold Out`, `Postponed`). |

### 3. Bookings Table

This transactional table records individual ticket purchases by linking users to their chosen matches.

| **Field Name**   | **What the Field Does**                                                        |
| ---------------- | ------------------------------------------------------------------------------ |
| `booking_id`     | Unique tracking transaction number for the ticket purchase.                    |
| `user_id`        | Links the booking directly to the user who made the purchase.                  |
| `match_id`       | Links the booking directly to the specific match being attended.               |
| `seat_number`    | The specific allocated seat identifier in the stadium (e.g., `A-12`).          |
| `payment_status` | Tracks financial resolution (`Pending`, `Confirmed`, `Cancelled`, `Refunded`). |
| `total_cost`     | The calculated final invoice price based on the base price and seat quantity.  |

## ERD Design

Design an Entity Relationship Diagram (ERD) for the Football Ticket Booking System.

### Required Tables

1. Users
2. Matches
3. Bookings

### Relationship Requirements

- **One to Many:** One User → Many Bookings (A single football fan can buy tickets for multiple matches throughout the season).
- **Many to One:** Many Bookings → One Match (A major derby match can be associated with thousands of individual booking records from different fans).
- **One to One (logical):** Each individual row in the booking table maps exactly one user to one match for that specific reserved seating choice.

### ERD Includes

- Primary Keys (PK)
- Foreign Keys (FK)
- Relationship cardinality (e.g., Crow’s Foot notation)
- Status fields (e.g., booking payment status, match ticket status)

### SQL Query Test

- Seven problems are solved and given in a sql file.

### THeory Questions

3 questins are answered in video format and uploaded it to youtube for sharing. The questions are structures closed questions and Answers are precise and specific. The medium of instruction and answer all are in English.
