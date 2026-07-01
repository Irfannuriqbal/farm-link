# Farm Link

Farm Link is a Laravel-based agricultural marketplace application designed to help users browse products, read updates, and interact through comments, while giving administrators the tools to manage users and product listings.

## Overview

This project combines a public storefront with role-based administration. Visitors can explore product pages and informational content, while authenticated users can access profile features and submit comments. Administrators manage products, users, and the dashboard from a protected backend.

## Key Features

- Public landing page and informational pages such as About, Contact, News, Shop, Cart, and Checkout.
- Product catalog with detail pages for individual items.
- Comment system tied to product content.
- Authentication and profile management.
- Role-based access control for `admin` and `user` accounts.
- Admin dashboard for managing users and products.

## Tech Stack

- Laravel 10
- PHP 8.1+
- MySQL or compatible SQL database
- Laravel Breeze for authentication scaffolding
- Spatie Laravel Permission for role and permission management
- Vite, Tailwind CSS, and Alpine.js for frontend assets

## Requirements

- PHP 8.1 or newer
- Composer
- Node.js and npm
- A database server such as MySQL or MariaDB

## Installation

1. Clone the repository.
2. Install PHP dependencies.
3. Install frontend dependencies.
4. Copy `.env.example` to `.env` and configure your database connection.
5. Generate an application key.
6. Run migrations and seeders.

```bash
composer install
npm install
cp .env.example .env
php artisan key:generate
php artisan migrate --seed
```

## Run the Application

Start the Laravel development server and the frontend build watcher in separate terminals.

```bash
php artisan serve
npm run dev
```

## Build for Production

```bash
npm run build
```

## Project Structure

- `app/Models` contains core domain models such as product, comment, and user.
- `app/Http/Controllers` contains application logic for the public site and admin dashboard.
- `database/migrations` defines the schema for users, products, comments, and permissions.
- `resources/views` contains the Blade templates for the public and admin interfaces.
- `routes/web.php` defines the main web routes and role-protected areas.

## Notes

- The project uses role-based middleware to separate admin and user access.
- Seeders are available for initial roles, permissions, and sample data.

## License

This project is open-sourced under the MIT license.
