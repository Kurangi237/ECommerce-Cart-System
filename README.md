                                                             🛒 E-Commerce Cart System (Java Console Application)
📌 Overview:
This is a simple Java console-based E-Commerce Cart System that allows users to browse products, add/remove items from a shopping cart, view their cart, and proceed to checkout.
It demonstrates Object-Oriented Programming (OOP) concepts such as classes, objects, encapsulation, collections (List, Map), and streams.

✨ Features:
📦 View Product Catalog – Browse a list of available products.
➕ Add Products to Cart – Add items with specific quantities.
➖ Remove Products from Cart – Remove an item using its ID.
🛍 View Cart – See cart items, quantities, subtotals, and total price.
💳 Checkout – Generate the final bill and clear the cart.
🚪 Exit Option – Quit the system safely.

🗂 Project Structure:
ECommerceCartSystem.java
│
├── class Product
│     ├── id (int)
│     ├── name (String)
│     ├── price (double)
│
├── class Cart
│     ├── addItem(Product, quantity)
│     ├── removeItem(Product)
│     ├── viewCart()
│     ├── checkout()
│
└── public class ECommerceCartSystem (Main)
      ├── main() → runs the console menu

🛠️ Technologies Used
Language: Java
Collections: List, Map, HashMap
Concepts: OOP, Streams, Console I/O

▶️ How to Run
1. Clone or download the project file.
2. Open in any IDE (Eclipse, IntelliJ, VS Code) or use command line.
3. Compile: javac ECommerceCartSystem.java
4. Run: java ECommerceCartSystem

📖 Sample Menu:
========= E-Commerce Cart =========
1. View Products
2. Add to Cart
3. Remove from Cart
4. View Cart
5. Checkout
6. Exit
Enter your choice: 

💡 Example Run:
--- Product Catalog ---
1. Laptop - ₹50000.0
2. Smartphone - ₹25000.0
3. Headphones - ₹2000.0
4. Keyboard - ₹1500.0
5. Mouse - ₹700.0

Enter Product ID to add: 2
Enter quantity: 1
1 x Smartphone added to cart.

--- Cart Items ---
Smartphone x 1 = ₹25000.0
Total: ₹25000.0

🚀 Future Enhancements
✅ Discount coupons
✅ Multiple user accounts
✅ Save cart data to file/DB
✅ Add categories & search functionality

👨‍💻 Author
Developed by [Bala Venkatarao Kurangi] – A simple project to demonstrate Java OOP and collections.
