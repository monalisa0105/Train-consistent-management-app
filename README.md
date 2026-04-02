import java.util.*;

// Bogie class (Custom Object)
class Bogie {
String name;
int capacity;

    public Bogie(String name, int capacity) {
        this.name = name;
        this.capacity = capacity;
    }

    public String toString() {
        return name + " → Capacity: " + capacity;
    }
}

public class Trainconsistentmanagementapp {

    public static void main(String[] args) {

        // Welcome message
        System.out.println("=== Train Consist Management App ===");

        // Create list of bogies
        List<Bogie> bogies = new ArrayList<>();

        // Add bogies
        bogies.add(new Bogie("Sleeper", 72));
        bogies.add(new Bogie("AC Chair", 54));
        bogies.add(new Bogie("First Class", 24));

        // Sort bogies by capacity (ascending)
        bogies.sort(Comparator.comparingInt(b -> b.capacity));

        // Display sorted bogies
        System.out.println("\nBogies Sorted by Capacity:");

        for (Bogie b : bogies) {
            System.out.println(b);
        }
    }
}