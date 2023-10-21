# Task1_week1
import java.util.Scanner;

 class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the temperature value: ");
        double temperature = scanner.nextDouble();

        System.out.print("Enter the unit (C for Celsius, F for Fahrenheit): ");
        String unit = scanner.next();

        double convertedTemperature;

        if (unit.equalsIgnoreCase("C")) {
            convertedTemperature = (temperature * 9/5) + 32;
            System.out.println("Converted temperature in Fahrenheit: " + convertedTemperature + "°F");
        } else if (unit.equalsIgnoreCase("F")) {
            convertedTemperature = (temperature - 32) * 5/9;
            System.out.println("Converted temperature in Celsius: " + convertedTemperature + "°C");
        } else {
            System.out.println("Invalid unit specified. Please try again.");
        }

        scanner.close();
    }
}
