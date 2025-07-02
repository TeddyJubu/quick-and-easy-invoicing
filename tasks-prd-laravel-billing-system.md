# tasks-prd-laravel-billing-system.md

## Relevant Files

- `app/Models/User.php` - Extended user model with roles and company settings
- `app/Models/Customer.php` - Customer model with contact and address information
- `app/Models/Invoice.php` - Main invoice model with calculations and status management
- `app/Models/InvoiceItem.php` - Line items for invoices with pricing calculations
- `app/Models/RecurringInvoice.php` - Template for recurring billing schedules
- `app/Http/Controllers/CustomerController.php` - CRUD operations for customer management
- `app/Http/Controllers/InvoiceController.php` - Invoice creation, editing, and PDF generation
- `app/Http/Controllers/DashboardController.php` - Dashboard metrics and overdue reporting
- `app/Http/Requests/StoreCustomerRequest.php` - Customer validation rules
- `app/Http/Requests/StoreInvoiceRequest.php` - Invoice validation with line items
- `database/migrations/2025_01_01_000001_create_customers_table.php` - Customer schema
- `database/migrations/2025_01_01_000002_create_invoices_table.php` - Invoice schema with relationships
- `database/migrations/2025_01_01_000003_create_invoice_items_table.php` - Line items schema
- `database/seeders/DatabaseSeeder.php` - Sample data for testing
- `resources/views/customers/index.blade.php` - Customer listing with search/pagination
- `resources/views/invoices/create.blade.php` - Invoice creation form with dynamic line items
- `resources/views/invoices/pdf.blade.php` - PDF template with company branding
- `resources/views/dashboard.blade.php` - Main dashboard with key metrics
- `tests/Feature/CustomerTest.php` - Customer CRUD functionality tests
- `tests/Feature/InvoiceTest.php` - Invoice creation and PDF generation tests
- `config/dompdf.php` - PDF generation configuration


## Notes

- Use **Laravel Breeze** for authentication scaffolding with role-based middleware[^1]
- Implement **proper database relationships** with foreign key constraints for data integrity[^1]
- Follow **conventional commit format** for each completed task (feat, fix, refactor)[^2]
- Run **full test suite** before marking parent tasks complete[^2]
- Use **feature branches** for major functionality to isolate changes[^1]


## Tasks

### **1.0 Project Setup \& Authentication**

- **1.1** Create new Laravel project and install Laravel Breeze for authentication
- **1.2** Configure database connection and run initial migrations
- **1.3** Extend User model with role field and company settings
- **1.4** Create role-based middleware for Admin/User access control
- **1.5** Set up basic layout with navigation for authenticated users


### **2.0 Customer Management**

- **2.1** Create Customer model and migration with name, email, phone, billing/shipping addresses
- **2.2** Generate CustomerController with resource routes and CRUD operations
- **2.3** Create customer validation request classes with proper rules
- **2.4** Build customer index view with search, pagination, and action buttons
- **2.5** Implement customer create/edit forms with address fields
- **2.6** Add soft deletes to customer model for data retention


### **3.0 Invoice Creation \& Management**

- **3.1** Create Invoice model and migration with customer relationship and status tracking
- **3.2** Create InvoiceItem model and migration for line items with pricing
- **3.3** Generate InvoiceController with proper form handling and calculations
- **3.4** Build invoice creation form with dynamic line item addition/removal
- **3.5** Implement automatic invoice numbering and total calculations
- **3.6** Create invoice listing view with status filters and search functionality
- **3.7** Add invoice status management (Draft, Sent, Paid, Overdue, Cancelled)


### **4.0 PDF Generation \& Branding**

- **4.1** Install and configure DOMPDF package for PDF generation
- **4.2** Create PDF template with company branding (logo, colors, contact info)
- **4.3** Implement downloadPDF method in InvoiceController with proper headers
- **4.4** Add company settings model for branding customization
- **4.5** Create settings page for logo upload and brand color configuration


### **5.0 Dashboard \& Overdue Reporting**

- **5.1** Create DashboardController with key metrics calculations
- **5.2** Build dashboard view with revenue, outstanding, and overdue widgets
- **5.3** Implement overdue invoice detection with aging calculations
- **5.4** Create overdue invoices report with filtering and export options
- **5.5** Add recent activity feed showing latest invoice actions


### **6.0 Recurring Billing Implementation**

- **6.1** Create RecurringInvoice model for billing templates and schedules
- **6.2** Add recurring billing setup form with frequency options (monthly, quarterly, annual)
- **6.3** Implement Artisan command for generating recurring invoices automatically
- **6.4** Create recurring invoice management interface for editing templates
- **6.5** Add email notifications for generated recurring invoices


### **7.0 Custom Fields Support**

- **7.1** Create CustomField model for storing field definitions per entity type
- **7.2** Add custom field management interface for admins
- **7.3** Extend customer and invoice forms to display custom fields dynamically
- **7.4** Update PDF templates to include custom field values
- **7.5** Implement validation for required custom fields


### **8.0 Testing \& Quality Assurance**

- **8.1** Write feature tests for customer CRUD operations with validation
- **8.2** Create invoice functionality tests including PDF generation
- **8.3** Add unit tests for calculation methods and business logic
- **8.4** Implement dashboard metrics testing with sample data
- **8.5** Set up GitHub Actions for automated testing and code quality checks
- **8.6** Create comprehensive documentation and deployment guide

**Ready to start implementation?** The tasks are structured to build your MVP incrementally, with each parent task delivering working functionality. Reply with **"Start task 1.1"** to begin with project setup, and I'll guide you through each step using Laravel best practices and proper testing workflows[^1][^2].

