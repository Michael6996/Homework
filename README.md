"Welcome to metric converter! 

Please input your query. For example, 1 km = m. 

Enter 'exit' or '-1' to exit the program"

"Your input is not currently handled by this app, please input another query, for example, 1 kg = lb"

import java.util.Scanner;

public class App{
    
    
   // public static void main(String[] args, Scanner scanner) throws Exception {
        public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Welcome to the metric converter! \n");
        System.out.println("Please input your query (choose 1-4). \n");
        
        System.out.println("Choose a conversion option:");
        System.out.println("1. Kilograms to Pounds");
        System.out.println("2. Meters to Feets");
        System.out.println("3. Celsius to Fahrenheit");
        System.out.println("4. Seconds to days");

        System.out.println("Enter -1 to exit the program. \n");

        String query = scanner.nextLine();
        Conversion(query);

      scanner.close();
        }
    
        public static void Conversion(String choice) {
            double result;
            Scanner scanner = new Scanner(System.in);
    
            switch (choice) {
                case "1" :
                    System.out.println("Enter the weight in kilograms: ");
                    double kilograms = scanner.nextDouble();
                    result = kilograms * 2.20462;
                    System.out.println("Result: " + result + " pounds");
                    break;
                    case "2" :
                    System.out.println("Enter the distance in meters: ");
                    double meters = scanner.nextDouble();
                    result = meters * 3.4808;
                    System.out.println("Result: " + result + " feet");
                    break;
                    case "3" :
                    System.out.println("Enter the tempature in Celsius: ");
                    double celsius = scanner.nextDouble();
                    result = celsius * 1.8 + 32;
                    System.out.println("Result: " + result + " Fahrenheit");
                    break;
                    case "4" :
                    System.out.println("Enter the time in seconds: ");
                    double seconds = scanner.nextDouble();
                    result = seconds * 0.000011574;
                    System.out.println("Result: " + result + " days");
                    break;
                case "-1":
                    break;
                default:
                    System.out.println("Invalid Choice. Please try again.");
                    scanner.close();
                }
            }
            
        }

