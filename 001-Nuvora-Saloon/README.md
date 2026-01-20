# Nuvora Saloon Management System

A comprehensive web-based application for managing salon operations, built with **Laravel 11** and **Tailwind CSS**. This system streamlines appointment scheduling, service management, and barber coordination suitable for modern salon businesses.

## 📋 Project Overview

Nuvora Saloon provides a dual-interface platform:
*   **Customer Portal**: Allows users to view services, pricing, gallery, and book appointments online.
*   **Admin Dashboard**: Enables administrators to manage services, barbers, schedules, and view appointment history.

**Key Technologies:**
*   **Framework**: Laravel 11.x
*   **Frontend**: Tailwind CSS v3.x, Alpine.js, Blade Templates
*   **Build Tool**: Vite
*   **Database**: MySQL / SQLite (configurable)

## 🚀 Setup Instructions

Follow these steps to set up the project locally.

### Prerequisites
Ensure you have the following installed:
*   PHP >= 8.2
*   Composer
*   Node.js & NPM

### Installation

1.  **Clone/Unzip the Repository**
    ```bash
    git clone <repository_url>
    # or unzip the project folder
    cd Nuvora-Saloon-dev
    ```

2.  **Install Dependencies**
    ```bash
    # Backend
    composer install

    # Frontend
    npm install
    ```

3.  **Environment Configuration**
    Copy the example environment file and configure your database:
    ```bash
    cp .env.example .env
    ```
    Open `.env` and update your database credentials:
    ```ini
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=nuvora_db
    DB_USERNAME=root
    DB_PASSWORD=
    ```

4.  **Database Setup**
    ```bash
    php artisan key:generate
    php artisan migrate
    # Optional: Seed data if available
    # php artisan db:seed
    ```

5.  **Run the Application**
    You will need two terminal sessions running:
    
    *Terminal 1 (Vite Dev Server):*
    ```bash
    npm run dev
    ```
    
    *Terminal 2 (Laravel Server):*
    ```bash
    php artisan serve
    ```

    Access the application at: `http://localhost:8000`

## 📖 Usage Guide

### User Roles
*   **User**: Can browse services and book appointments.
*   **Admin**: Full access to the backend dashboard.

### Accessing the Dashboard
1.  Navigate to `/login` or `/register`.
2.  Log in with your credentials.
3.  Based on your role, you will be redirected to:
    *   **Admin Dashboard**: `/admin/dashboard`
    *   **User Dashboard**: `/user/dashboard`

### Common Admin Tasks
*   **Manage Services**: Add or edit salon services (prices, duration, description).
*   **Manage Barbers**: Add profiles for new staff members.
*   **Schedules**: View and manage booking slots.

## 🔧 Troubleshooting

*   **Styles not loading?** Ensure `npm run dev` is running.
*   **500 Error?** Check permissions on the `storage` and `bootstrap/cache` directories.
*   **Database error?** Ensure your database server is running and the `.env` credentials are correct.
