import java.util.*;

class Product {
    private int id;
    private String name;
    private double price;

    public Product(int id, String name, double price) {
        this.id = id;
        this.name = name;
        this.price = price;
    }

    public int getId() { return id; }
    public String getName() { return name; }
    public double getPrice() { return price; }

    @Override
    public String toString() {
        return id + ". " + name + " - ₹" + price;
    }
}

class Cart {
    private Map<Product, Integer> items = new HashMap<>();

    public void addItem(Product product, int quantity) {
        items.put(product, items.getOrDefault(product, 0) + quantity);
        System.out.println(quantity + " x " + product.getName() + " added to cart.");
    }

    public void removeItem(Product product) {
        if (items.containsKey(product)) {
            items.remove(product);
            System.out.println(product.getName() + " removed from cart.");
        } else {
            System.out.println("Item not found in cart.");
        }
    }

    public void viewCart() {
        if (items.isEmpty()) {
            System.out.println("Cart is empty.");
            return;
        }
        double total = 0;
        System.out.println("\n--- Cart Items ---");
        for (Map.Entry<Product, Integer> entry : items.entrySet()) {
            Product p = entry.getKey();
            int qty = entry.getValue();
            double subtotal = p.getPrice() * qty;
            System.out.println(p.getName() + " x " + qty + " = ₹" + subtotal);
            total += subtotal;
        }
        System.out.println("Total: ₹" + total);
    }

    public void checkout() {
        if (items.isEmpty()) {
            System.out.println("Cart is empty. Add items before checkout.");
            return;
        }
        double total = 0;
        for (Map.Entry<Product, Integer> entry : items.entrySet()) {
            total += entry.getKey().getPrice() * entry.getValue();
        }
        System.out.println("\nCheckout successful! Total bill: ₹" + total);
        items.clear();
    }
}

public class ECommerceCartSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Sample product catalog
        List<Product> products = new ArrayList<>();
        products.add(new Product(1, "Laptop", 50000));
        products.add(new Product(2, "Smartphone", 25000));
        products.add(new Product(3, "Headphones", 2000));
        products.add(new Product(4, "Keyboard", 1500));
        products.add(new Product(5, "Mouse", 700));

        Cart cart = new Cart();

        boolean exit = false;
        while (!exit) {
            System.out.println("\n========= E-Commerce Cart =========");
            System.out.println("1. View Products");
            System.out.println("2. Add to Cart");
            System.out.println("3. Remove from Cart");
            System.out.println("4. View Cart");
            System.out.println("5. Checkout");
            System.out.println("6. Exit");
            System.out.print("Enter your choice: ");
            int choice = sc.nextInt();

            switch (choice) {
                case 1:
                    System.out.println("\n--- Product Catalog ---");
                    for (Product p : products) {
                        System.out.println(p);
                    }
                    break;
                case 2:
                    System.out.print("Enter Product ID to add: ");
                    int id = sc.nextInt();
                    System.out.print("Enter quantity: ");
                    int qty = sc.nextInt();
                    Product productToAdd = products.stream()
                            .filter(p -> p.getId() == id)
                            .findFirst()
                            .orElse(null);
                    if (productToAdd != null) {
                        cart.addItem(productToAdd, qty);
                    } else {
                        System.out.println("Invalid Product ID.");
                    }
                    break;
                case 3:
                    System.out.print("Enter Product ID to remove: ");
                    int removeId = sc.nextInt();
                    Product productToRemove = products.stream()
                            .filter(p -> p.getId() == removeId)
                            .findFirst()
                            .orElse(null);
                    if (productToRemove != null) {
                        cart.removeItem(productToRemove);
                    } else {
                        System.out.println("Invalid Product ID.");
                    }
                    break;
                case 4:
                    cart.viewCart();
                    break;
                case 5:
                    cart.checkout();
                    break;
                case 6:
                    exit = true;
                    System.out.println("Thank you for shopping with us!");
                    break;
                default:
                    System.out.println("Invalid choice. Try again.");
            }
        }
        sc.close();
    }
}
