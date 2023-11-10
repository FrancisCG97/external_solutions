import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        File file = new File("DATA.lst");
        try {
            Scanner scanner = new Scanner(file);
            String data = scanner.nextLine();
            scanner.close();

            String[] values = data.split(" ");
            String num1 = values[0];
            String num2 = values[1];

            int sum = Integer.parseInt(num1) + Integer.parseInt(num2);
            System.out.println(sum);
        } catch (FileNotFoundException e) {
            e.printStackTrace();
        }
    }
}
