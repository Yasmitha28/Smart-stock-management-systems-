import java.util.Scanner;

public class SmartStockManagement {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.println("===== SMART STOCK MANAGEMENT SYSTEM =====");

        System.out.print("Enter Product Name: ");
        String productName = sc.nextLine();

        System.out.print("Enter Product Price: ");
        double price = sc.nextDouble();

        System.out.print("Enter Available Stock: ");
        int stock = sc.nextInt();

        System.out.println("\n===== PRODUCT DETAILS =====");
        System.out.println("Product Name : " + productName);
        System.out.println("Price        : ₹" + price);
        System.out.println("Stock        : " + stock);

        if (stock <= 10) {
            System.out.println("\n***** ALERT *****");
            System.out.println("LOW STOCK ALERT!");
            System.out.println("Reorder Required");
            System.out.println("Suggested Quantity: " + (100 - stock));
        } else {
            System.out.println("\nStock Level Normal");
        }

        double totalValue = stock * price;
        System.out.println("Total Stock Value: ₹" + totalValue);

        sc.close();
    }
}
