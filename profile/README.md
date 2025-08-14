# Salondora - Salon Booking Platform

## Overview

Salondora is a **full-featured salon booking platform** that connects customers with salons seamlessly. It includes:

- **Web application** for both **customers** and **salon admins**
- **Two dedicated mobile apps**: one for customers and one for salon admins
- **Single backend and database** powered by **PostgreSQL** and **Supabase**

The system enables customers to easily discover, book, and review salons, while giving salon owners a powerful management dashboard to handle bookings, services, and stylists.

---

## Key Features

### 1. Customer Side

- **Salon Browsing**: View a list of salons with details, ratings, and location.
- **Service Selection**: Choose services such as haircuts, beard trims, and more.
- **Stylist & Time Selection**:

  - Select a stylist who can perform all chosen services.
  - View available time slots for the selected stylist.

- **Authentication Flow**:

  - If logged in → proceed to booking confirmation.
  - If not logged in → redirect to login/signup.

- **Booking Management**:

  - View upcoming bookings.
  - Review completed bookings.

### 2. Salon Admin Side

- **Registration**:

  - Register as a salon by adding logo, address, and location.
  - Add services with prices and durations.
  - Add stylists and assign services to them.
  - Set weekly work schedules (e.g., Sunday: 8 AM - 6 PM).
  - Configure breaks and interval blocks.

- **Booking Management**:

  - Add walk-in or phone-call bookings directly into the system.
  - Manage all incoming online bookings.

- **Visibility Control**:

  - Newly registered salons must be approved by **Super Admin** before appearing to customers.

### 3. Super Admin Side

- Approve or reject newly registered salons.
- View all registered salons and their bookings.
- Monitor overall platform activity.

---

## System Architecture

### 1. Frontend

- **Web App**: React + Tailwind CSS (separate dashboards for customers and salon admins)
- **Mobile Apps**: Flutter(Dart)

### 2. Backend

- **Framework**: Node.js + Express
- **Database**: PostgreSQL
- **Auth & Storage**: Supabase
- **API**: RESTful endpoints shared between all clients

### 3. Infrastructure

- Single backend serving all platforms
- Role-based authentication (Customer, Salon Admin, Super Admin)
- Secure CRUD operations for services, stylists, bookings, and salon data

---

## Booking Flow (Customer Side)

1. Browse salons → click on a salon.
2. Select one or more services.
3. Choose a stylist who can perform all selected services.
4. Select date and view available slots.
5. Authenticate (if not already logged in).
6. Confirm booking.
7. View booking in "Upcoming Bookings".

---

## Salon Onboarding Flow (Salon Admin Side)

1. Register and submit salon details.
2. Add services with pricing.
3. Add stylists and assign services.
4. Set work schedules and breaks.
5. Submit for **Super Admin** approval.
6. Once approved, salon is visible to customers.

---

## Database & Backend Highlights

- **PostgreSQL** schema for:

  - Users (with roles)
  - Customers
  - Salons
  - Services
  - Stylists
  - Stylist Services
  - Bookings
  - Bookings Services
  - Work schedules
  - Break

- **Supabase** for authentication, authorization, and file storage (logos, images)

---

## Tech Stack

### Frontend

- **Web**: React, Tailwind CSS
- **Mobile**: Flutter(Dart)

### Backend

- Node.js, Express.js
- PostgreSQL (Supabase)
- JWT Authentication

### Tools & Services

- Supabase (Auth, Storage, Database)
- Cloud hosting for backend and frontend

---

## Future Enhancements

- Payment gateway integration for online payments
- AI-based stylist/service recommendations
- Advanced analytics for salon performance
- Multi-language and currency support

---

## License

This project is proprietary and maintained by **Vivora**. All rights reserved.
