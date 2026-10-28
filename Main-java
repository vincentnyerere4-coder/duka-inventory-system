import java.util.ArrayList;
import java.util.Scanner;

class Product {
    String name;
    double price;
    int quantity;
    Product(String name, double price, int quantity) {
        this.name = name;
        this.price = price;
        this.quantity = quantity;
    }
}

class DukaManager {
    ArrayList<Product> products = new ArrayList<>();
    void addProduct(String name, double price, int qty) {
        products.add(new Product(name, price, qty));
        System.out.println("Bidhaa '" + name + "' imeongezwa!");
    }
    void sellProduct(String name, int qty) {
        for (Product p : products) {
            if (p.name.equalsIgnoreCase(name)) {
                if (p.quantity >= qty) {
                    p.quantity -= qty;
                    double total = p.price * qty;
                    System.out.println("Umeuza " + qty + " " + name + " Jumla: " + total);
                    return;
                } else {
                    System.out.println("Stock haitoshi. Zimebaki: " + p.quantity);
                    return;
                }
            }
        }
        System.out.println("Bidhaa haijapatikana");
    }
    void viewStock() {
        System.out.println("\n--- STOCK YA DUKA ---");
        for (Product p : products) {
            System.out.println(p.name + " | Bei: " + p.price + " | Zipo: " + p.quantity);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        DukaManager duka = new DukaManager();
        Scanner sc = new Scanner(System.in);
        while (true) {
            System.out.println("\n1.Ongeza 2.Uza 3.Stock 4.Toka");
            System.out.print("Chagua: ");
            int ch = sc.nextInt();
            if (ch == 1) {
                System.out.print("Jina: "); String n = sc.next();
                System.out.print("Bei: "); double pr = sc.nextDouble();
                System.out.print("Idadi: "); int qt = sc.nextInt();
                duka.addProduct(n, pr, qt);
            } else if (ch == 2) {
                System.out.print("Jina: "); String n = sc.next();
                System.out.print("Idadi: "); int qt = sc.nextInt();
                duka.sellProduct(n, qt);
            } else if (ch == 3) {
                duka.viewStock();
            } else { break; }
        }
    }
}
