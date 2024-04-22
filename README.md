import javax.swing.*;

public class Main
{
    public static void main(String args[]) throws Exception
    {
        // Declare variables.
        final int NUM_ITEMS = 5; // Named constant
        String addIn;  // Add-in ordered by customer.
        boolean foundIt = false; 
        // Initialized array of add-ins.
        String addIns[] = {"Cream", "Cinnamon", "Chocolate", "Amaretto", "Whiskey"}; 
        // Initialized array of add-in prices.
        double addInPrices[] = {.89, .25, .59, 1.50, 1.75};
        double orderTotal = 2.00;  // All orders start with a 2.00 charge
        
        while (true) {

        // Get user input.
        addIn = JOptionPane.showInputDialog("Enter coffee add-in or XXX to quit: ");
        // Write the rest of the program here.
        if (addIn.equalsIgnoreCase( "XXX")) {
            break; 
        }
        
        for (int i = 0; i < NUM_ITEMS; i++) {
            if (addIn.equalsIgnoreCase(addIns[i])){
                System.out.println("Add-in: " + addIns[i]);
                System.out.println("price: $" + addInPrices[i]);
                orderTotal += addInPrices[i];
                foundIt = true;
                break; 
            }
        }
        if (!foundIt) {
            System.out.println("Sorry, we do not carry that.");
        }    
        }
        System.out.println("Order Total : $" + orderTotal);
    }
}

