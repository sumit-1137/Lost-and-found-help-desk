# Lost and Found Help Desk

## Overview

The **Lost and Found Help Desk** is a web-based application designed to help college students and staff report, search for, and recover lost belongings in a simple and organized way. On large campuses, students frequently misplace items such as ID cards, wallets, mobile phones, laptops, books, water bottles, keys, and other personal belongings. Traditional notice boards and word-of-mouth methods are often slow and ineffective. This system provides a centralized digital platform where users can report lost or found items, making the recovery process faster and more efficient.

The platform improves communication between students, faculty, and campus administration while reducing the chances of permanently losing valuable items. It also minimizes manual work for college authorities by maintaining a searchable database of reported items.

---

# Problem Statement

Students and staff often lose personal belongings on campus. Existing methods of finding lost items rely on physical notice boards, social media groups, or visiting multiple departments, which are time-consuming and unreliable.

The **Lost and Found Help Desk** solves this issue by allowing users to:

- Report lost items instantly.
- Submit found item information.
- Search available records.
- Contact the person who reported an item.
- Track the status of claims.
- Allow administrators to verify and manage reports.

---

# Objectives

The primary objectives of this project are:

- Create a centralized platform for reporting lost and found items.
- Reduce the time required to recover lost belongings.
- Provide a user-friendly interface for students and staff.
- Prevent duplicate reports through efficient management.
- Improve transparency and communication.
- Allow administrators to monitor all activities.
- Maintain a secure and organized database.

---

# Key Features

## User Registration and Login

- Student registration using college email.
- Secure login authentication.
- Password encryption.
- Profile management.
- Password reset functionality.

---

## Lost Item Reporting

Users can submit detailed information including:

- Item name
- Category
- Description
- Color
- Brand
- Date lost
- Location where lost
- Upload multiple images
- Additional identifying information

---

## Found Item Reporting

Anyone who finds an item can submit:

- Item details
- Place where found
- Date found
- Images
- Current storage location
- Contact details

---

## Smart Search System

Users can search items using:

- Item name
- Category
- Date
- Location
- Color
- Brand
- Keywords

Advanced filters make searching faster and more accurate.

---

## Claim Request

Students can request ownership of an item by providing:

- Proof of ownership
- Item description
- Additional identifying information

The administrator reviews and approves or rejects the request.

---

## Notifications

The system sends notifications when:

- A matching item is found
- Claim status changes
- Administrator approves/rejects requests
- New reports match previous submissions

---

## Admin Dashboard

The administrator can:

- Manage users
- Verify reports
- Remove fake reports
- Approve claims
- Manage categories
- View statistics
- Generate reports

---

# System Modules

## Student Module

Features include:

- Registration
- Login
- Report Lost Item
- Report Found Item
- Search Items
- Submit Claims
- View Claim Status
- Edit Profile

---

## Administrator Module

Features include:

- Secure Login
- User Management
- Lost Item Management
- Found Item Management
- Claim Verification
- Report Generation
- Dashboard Analytics
- Database Management

---

# Technology Stack

## Frontend

- HTML5
- CSS3
- JavaScript
- Bootstrap
- React.js (Optional)

---

## Backend

- Node.js
- Express.js

or

- PHP (Laravel)

or

- Python (Django/Flask)

---

## Database

- MySQL
- MongoDB

---

## Authentication

- JWT Authentication
- Session Management
- Password Hashing

---

## Cloud Storage

- Cloudinary
- Firebase Storage
- AWS S3

---

# Database Design

### Users Table

| Field | Type |
|--------|------|
| User ID | Integer |
| Name | Varchar |
| Email | Varchar |
| Password | Varchar |
| Phone | Varchar |
| Role | Student/Admin |

---

### Lost Items Table

| Field | Type |
|--------|------|
| Item ID | Integer |
| User ID | Integer |
| Item Name | Varchar |
| Category | Varchar |
| Description | Text |
| Location | Varchar |
| Date Lost | Date |
| Image | Varchar |
| Status | Pending/Matched/Claimed |

---

### Found Items Table

| Field | Type |
|--------|------|
| Item ID | Integer |
| User ID | Integer |
| Item Name | Varchar |
| Category | Varchar |
| Description | Text |
| Location Found | Varchar |
| Date Found | Date |
| Image | Varchar |
| Status | Available/Claimed |

---

### Claims Table

| Field | Type |
|--------|------|
| Claim ID | Integer |
| Item ID | Integer |
| User ID | Integer |
| Claim Reason | Text |
| Status | Pending/Approved/Rejected |

---

# Workflow

```text
User Registration
        │
        ▼
Secure Login
        │
        ▼
Report Lost Item
        │
        ▼
Database Stores Information
        │
        ▼
Another User Reports Found Item
        │
        ▼
System Matches Similar Items
        │
        ▼
Notification Sent
        │
        ▼
Claim Request
        │
        ▼
Admin Verification
        │
        ▼
Item Returned Successfully
