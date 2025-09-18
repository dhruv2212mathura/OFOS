# 🍽️ Online Food Ordering System (PHP + MySQL)

This is a dynamic web-based food ordering system developed using PHP and MySQL. The platform enables users to browse dishes, add items to the cart, place orders, and manage their accounts. Admins can manage restaurants, dishes, and view customer orders through a secure backend interface.

---

## 🎯 Project Purpose

To build a full-stack food ordering platform that demonstrates:

- Dynamic content rendering with PHP & MySQL
- User authentication and session management
- Real-time cart and order processing
- Admin dashboard for managing food, orders, and restaurants

---

## 🔑 Key Features

- **User Registration & Login**: Secure authentication with session handling
- **Restaurant & Dish Browsing**: View available restaurants and their menus
- **Cart & Checkout System**: Add dishes to cart and place orders
- **Order History**: View past orders with timestamps
- **Admin Panel**: Manage dishes, restaurants, and delete orders
- **Logout Functionality**: Secure session termination

---

## 🧱 System Architecture

| Component | Technology        |
|----------|--------------------|
| Frontend | HTML, CSS, Bootstrap |
| Backend  | PHP                |
| Database | MySQL              |
| Server   | Apache (via XAMPP) |

---

## 📂 Project Structure

```
📁 online-food-ordering/
├── index.php               # Landing page with dish and restaurant listings
├── login.php               # User login
├── logout.php              # Session logout
├── registration.php        # User registration
├── checkout.php            # Cart & checkout logic
├── your_orders.php         # Displays user's order history
├── delete_orders.php       # Admin deletes past orders
├── dishes.php              # Admin view to manage dishes
├── restaurants.php         # Admin view to manage restaurants
├── product-action.php      # Handles cart operations (add, remove)
├── 01 LOGIN DETAILS.txt    # Admin login credentials
```

---

## 🧮 Core Logic

### Add to Cart:
```php
$_SESSION["cart_item"][$code] = array(
  'name' => $product["title"],
  'price' => $product["price"],
  'quantity' => $quantity
);
```

### Secure Session Handling:
```php
session_start();
if (!isset($_SESSION['user_id'])) {
  header("Location: login.php");
}
```

---

## 🗃️ Database Schema (High-Level)

- **Users**: Stores registered user information
- **Restaurants**: Contains restaurant names and details
- **Dishes**: Menu items associated with restaurants
- **Orders**: Tracks which user ordered what and when

---

## 🖥️ How to Use

1. Clone or download the repository.
2. Import the database `.sql` file (not included here) into phpMyAdmin.
3. Place the project folder in your XAMPP `htdocs` directory.
4. Start Apache and MySQL from the XAMPP control panel.
5. Visit `http://localhost/online-food-ordering` in your browser.
6. Register a user account or log in as admin (`admin` / `codeastro`).
7. Browse restaurants, add dishes to cart, and place orders.

---

## 📷 User Interface

- Dish grid with images, prices, and “Add to Cart”
- Admin dashboard for viewing orders and managing menu
- Responsive design with Bootstrap

![Chat UI](Project_Files/screenshot1.png)
![Chat UI](Project_Files/screenshot2.png)


![Chat UI](Project_Files/screenshot3.png)


![Chat UI](Project_Files/screenshot4.png)


![Chat UI](Project_Files/screenshot5.png)


---

## 🧰 Tools Used

- **PHP 7.4+**
- **MySQL 5.7+**
- **XAMPP**
- **Bootstrap 4**
- **VS Code**

---

## 🧠 Learnings

- Session management with PHP
- Dynamic cart and checkout system
- CRUD operations with MySQL
- Role-based access for admin and users

---

## 📬 Contact

Feel free to contribute or report issues via GitHub. For further questions, you can reach out via email or LinkedIn.
