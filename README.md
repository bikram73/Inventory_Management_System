# Inventory Management System

A comprehensive inventory management system built with CodeIgniter PHP framework. This system allows you to manage products, categories, warehouses, orders, and generate reports for your business inventory.
 
## Features

- **Dashboard**: Overview of inventory statistics and key metrics
- **Product Management**: Add, edit, delete, and manage products
- **Category Management**: Organize products into categories
- **Warehouse Management**: Manage multiple warehouse locations
- **Order Management**: Track and manage orders
- **Company Management**: Handle company information
- **Member Management**: User management and permissions
- **Reports**: Generate various inventory reports
- **Authentication**: Secure login system with user roles

## System Requirements

- **PHP**: Version 5.6 or newer (PHP 7.x recommended)
- **Web Server**: Apache/Nginx with mod_rewrite enabled
- **Database**: MySQL 5.5 or newer
- **Browser**: Modern web browser (Chrome, Firefox, Safari, Edge)

## Installation

### 1. Download and Setup

1. Clone or download this repository to your web server directory
2. Extract the files to your web root directory (e.g., `htdocs`, `www`, `public_html`)

### 2. Database Setup

1. Create a new MySQL database named `inventorymgtci`
2. Import the database file:
   ```sql
   mysql -u your_username -p inventorymgtci < "DATABASE FILE/inventorymgtci.sql"
   ```
   Or use phpMyAdmin to import the `DATABASE FILE/inventorymgtci.sql` file

### 3. Configuration

1. **Database Configuration**:
   - Open `application/config/database.php`
   - Update the database settings:
   ```php
   $db['default'] = array(
       'hostname' => 'localhost',
       'username' => 'your_db_username',
       'password' => 'your_db_password',
       'database' => 'inventorymgtci',
   );
   ```

2. **Base URL Configuration**:
   - Open `application/config/config.php`
   - Update the base URL to match your installation:
   ```php
   $config['base_url'] = 'http://your-domain.com/your-project-folder/';
   ```

### 4. File Permissions

Set appropriate permissions for the following directories:
```bash
chmod 755 application/cache
chmod 755 application/logs
```

### 5. Web Server Configuration

**For Apache**: The `.htaccess` files are already included for URL rewriting.

**For Nginx**: Add this configuration to your server block:
```nginx
location / {
    try_files $uri $uri/ /index.php?$query_string;
}
```

## Default Login Credentials

After installation, you can log in with:
- **Email**: admin@gmail.com
- **Password**: Password@123

**Important**: Change these credentials immediately after first login for security.

## Usage

### Accessing the System

1. Open your web browser
2. Navigate to your installation URL
3. Log in with the default credentials
4. Start managing your inventory!

### Main Modules

1. **Dashboard**: View inventory overview and statistics
2. **Products**: Manage your product catalog
3. **Categories**: Organize products into categories
4. **Warehouses**: Manage storage locations
5. **Orders**: Track customer orders and inventory movements
6. **Reports**: Generate inventory reports and analytics
7. **Settings**: Configure system settings and user permissions

## File Structure

```
├── application/
│   ├── controllers/     # Application controllers
│   ├── models/         # Database models
│   ├── views/          # View templates
│   ├── config/         # Configuration files
│   └── libraries/      # Custom libraries
├── assets/             # CSS, JS, images
├── system/             # CodeIgniter core files
├── DATABASE FILE/      # Database backup
└── index.php          # Main entry point
```

## Troubleshooting

### Common Issues

1. **Blank Page**: Check PHP error logs and ensure all file permissions are correct
2. **Database Connection Error**: Verify database credentials in `application/config/database.php`
3. **404 Errors**: Ensure mod_rewrite is enabled and `.htaccess` files are present
4. **Permission Denied**: Check file permissions for cache and logs directories

### Error Logs

Check the following locations for error logs:
- `application/logs/` - CodeIgniter logs
- Web server error logs (usually in `/var/log/apache2/` or `/var/log/nginx/`)

## Security Considerations

1. Change default admin credentials immediately
2. Keep PHP and database software updated
3. Set proper file permissions (avoid 777)
4. Use HTTPS in production
5. Regular database backups
6. Monitor access logs

## Version Information

- **CodeIgniter Version**: 3.x
- **PHP Version**: 5.6+ (7.x recommended)
- **Database**: MySQL 5.5+

---
