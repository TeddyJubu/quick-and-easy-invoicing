# quick-and-easy-invoicing

## Laravel Billing & Invoicing System

This is a self-hosted billing and invoicing application built with Laravel, designed for freelancers and small businesses. The goal is to provide a simple, fast, and efficient way to manage customers, create professional invoices, and track payments without recurring subscription fees.

## ✨ Key Features

This application comes with a rich set of features to streamline your billing process:

*   **Secure Authentication**: Role-based access control (Admin vs. User) powered by Laravel Breeze.
*   **Customer Management**: Full CRUD (Create, Read, Update, Delete) functionality for your client list, including contact and address details.
*   **Dynamic Invoicing**: Easily create invoices with multiple line items, automatic calculations for subtotals, taxes, and totals.
*   **PDF Generation**: Generate and download professional, brandable PDF invoices for your clients using DOMPDF.
*   **Informative Dashboard**: Get a quick overview of your business with key metrics like total revenue, outstanding payments, and overdue invoices.
*   **Recurring Billing**: Set up templates for recurring invoices (monthly, quarterly, etc.) and generate them automatically with a scheduled command.
*   **Status Tracking**: Manage the lifecycle of your invoices with statuses like Draft, Sent, Paid, Overdue, and Cancelled.

## 💻 Technology Stack

The project leverages a modern and robust tech stack:

*   **Backend**: PHP 8.1+ / Laravel 10.x
*   **Database**: MySQL
*   **Authentication**: Laravel Breeze
*   **PDF Engine**: `barryvdh/laravel-dompdf`
*   **Frontend**: Blade Templates, Tailwind CSS (via Breeze)

## 🚀 Getting Started

Follow these steps to get a local copy up and running.

### Prerequisites

*   PHP 8.1+
*   Composer
*   Node.js & NPM
*   A local MySQL server

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/laravel-billing-system.git
    cd laravel-billing-system
    ```

2.  **Install dependencies:**
    ```bash
    composer install
    npm install
    ```

3.  **Set up your environment file:**
    ```bash
    cp .env.example .env
    ```
    Next, generate your application key.
    ```bash
    php artisan key:generate
    ```

4.  **Configure your database:**
    Open the `.env` file and update the `DB_*` variables with your MySQL database credentials.
    ```
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=billing_system
    DB_USERNAME=root
    DB_PASSWORD=your_password
    ```

5.  **Run database migrations and seeders:**
    This will create all the necessary tables and populate them with sample data for testing.
    ```bash
    php artisan migrate --seed
    ```

6.  **Compile frontend assets:**
    ```bash
    npm run dev
    ```

7.  **Start the development server:**
    ```bash
    php artisan serve
    ```
    Your application will be available at `http://localhost:8000`.

## ✅ Running Tests

To ensure the application is working correctly, you can run the full suite of feature and unit tests.

```bash
php artisan test
```

## 🤝 Contributing

Contributions are welcome! To maintain a clean and manageable codebase, please follow these guidelines:

