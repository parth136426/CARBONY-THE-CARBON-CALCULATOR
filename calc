import java.util.Scanner;

public class CarbonCalc {
public static void main(String[] args) {
    Scanner console = new Scanner(System.in);

    double trans = determineTransportationEmission(console);
    double elec = determineElecticityEmission(console);
    double food = determineFoodEmission(console);

    giveIntro();

    calculateTotalEmission(trans, elec, food);
}

    
    public static void giveIntro() {
        System.out.println("This program will estimate your carbon footprint");
        System.out.println("(in metric tons per year) by asking you");
        System.out.println("to input relevant household data.");
        System.out.println("");
    }

    
    public static double determineTransportationEmission(Scanner input) {
        Scanner console = new Scanner(System.in);
        System.out.println("We will first begin with your transportation-related carbon expenditures...");
        System.out.print("How many kilometres do you drive per day? ");
        double kmPerDay = console.nextDouble();
        System.out.print("What is your car's fuel efficiency (in km/litre)? ");
        double fuelEfficiency = console.nextDouble();
        System.out.println("We now know that the numeber of litres you use per year is...");
        double litresUsedPerYear = 365.00 * (kmPerDay / fuelEfficiency);
        System.out.println(litresUsedPerYear);
        System.out.println("...and the kg of transportation-related CO2 you emit must be...");

        
        double trans = 2.3 * litresUsedPerYear;
        System.out.println(trans);
        System.out.println("");
        return trans;
    }

    
    public static double determineElecticityEmission(Scanner input) {
        Scanner console = new Scanner(System.in);
        System.out.println("We will now move on to your electricity-related carbon expenditures...");
        System.out.print("What is your monthly kilowatt usage (kWh/mo)? ");
        double kWhPerMonth = console.nextDouble();
        System.out.print("How many people live in your home? ");
        double numPeopleInHome = console.nextDouble();
        System.out.println("The kg of electricity-related CO2 you emit must be...");

        
        double elec = (kWhPerMonth * 12 * 0.257) / numPeopleInHome;
        System.out.println(elec);
        System.out.println("");
        return elec;
    }

    
    public static double determineFoodEmission(Scanner input) {
        Scanner console = new Scanner(System.in);
        System.out.println("We will now move on to your food-related carbon expenditures...");
        System.out.print("In a given year, what percentage of your diet is meat? ");
        double meat = console.nextDouble();
        System.out.print("In a given year, what percentage of your diet is dairy? ");
        double dairy = console.nextDouble();
        System.out.print("In a given year, what percentage of your diet is fruits and veggies? ");
        double fruitVeg = console.nextDouble();
        System.out.print("In a given year, what percentage of your diet is carbohydrates? ");
        double carbs = console.nextDouble();

        
        System.out.println("The kg of food-related CO2 you emit must be...");
        double food = (meat * 53.1 + dairy * 13.8 + fruitVeg * 7.6 + carbs * 3.1);
        System.out.println(food);
        System.out.println("");
        return food;
    }

    
    public static double calculateTotalEmission(double trans, double elec, double food) {
        System.out.println("Your total kg of CO2 emitted across all sources is equal to...");
        double total = trans + elec + food;
        System.out.println((double) total);
        System.out.println("");
        return total;

    }

}
