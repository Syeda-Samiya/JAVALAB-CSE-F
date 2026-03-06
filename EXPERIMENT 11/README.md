## EXPERIMENT 11
## TITLE:11)Train Reservation

## Reservation.java
```
class Reservation {

    int availableBerths;

    // Constructor
    Reservation(int berths) {
        availableBerths = berths;
    }

    // Synchronized method for booking berths
    synchronized void reserve(String personName, int requestedBerths) {

        System.out.println(personName + " is trying to reserve " + requestedBerths + " berth(s)");

        // Check if enough berths are available
        if (availableBerths >= requestedBerths) {

            System.out.println("Berths available for " + personName);

            // Deduct berths
            availableBerths = availableBerths - requestedBerths;

            System.out.println("Reservation confirmed for " + personName);
            System.out.println("Remaining berths: " + availableBerths);

        } else {

            System.out.println("Reservation failed for " + personName);
            System.out.println("Not enough berths available");

        }
```
## Person.java
```
class Person extends Thread {

    Reservation reservation;
    String personName;
    int berthsNeeded;

    // Constructor
    Person(Reservation r, String name, int berths) {
        reservation = r;
        personName = name;
        berthsNeeded = berths;
    }

    // Thread execution
    public void run() {

        reservation.reserve(personName, berthsNeeded);

    }
}
```
## Main.java
```
public class Main {

    public static void main(String[] args) {

        // Total berths available
        Reservation reservation = new Reservation(5);

        // Creating multiple persons (threads)
        Person p1 = new Person(reservation, "Ram", 2);
        Person p2 = new Person(reservation, "Sita", 2);
        Person p3 = new Person(reservation, "Ravi", 2);

        // Start threads
        p1.start();
        p2.start();
        p3.start();
    }
}
        System.out.println("-----------------------------------");
    }
}
```
## Output
<img width="1920" height="1080" alt="11" src="https://github.com/user-attachments/assets/81ebb495-b52c-4b7a-aafe-bf4c71389440" />
