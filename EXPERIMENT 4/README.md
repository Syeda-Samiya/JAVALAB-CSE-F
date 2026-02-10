## EXPERIMENT 4
## EXPERIMENT 4a
# TITLE 4a)To write a JAVA program to implement Single Inheritance.
## Person.java
```
public class Person {
    String name;
    int age;

    // Constructor
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method to display person details
    void displayPersonDetails() {
        System.out.println("Name : " + name);
        System.out.println("Age  : " + age);
    }
}
```
## Employee.java
public class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String nationalInsuranceNumber;

    // Constructor
    Employee(String name, int age, double annualSalary, int yearOfJoining, String nationalInsuranceNumber) {
        super(name, age); // calling Person class constructor
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.nationalInsuranceNumber = nationalInsuranceNumber;
    }

    // Method to display employee details
    void displayEmployeeDetails() {
        displayPersonDetails(); // inherited method
        System.out.println("Annual Salary : " + annualSalary);
        System.out.println("Year of Joining : " + yearOfJoining);
        System.out.println("National Insurance Number : " + nationalInsuranceNumber);
    }
}

##  TestEmployee.java
```
public class TestEmployee {
    public static void main(String[] args) {

        Employee emp1 = new Employee(
                "syeda Samiya",
                22,
                450000.00,
                2024,
                "NIN12345"
        );

        emp1.displayEmployeeDetails();
    }
}
```
# Output
![4a](https://github.com/user-attachments/assets/45be18dc-3d73-42c2-be95-9031269a0245)


## EXPERIMENT 4b
# TITLE 4b)To write a JAVA program to implement Multiple Inheritance.
## Bicycle.java
```
public class Bicycle {
    String pedalType;

    void showBicycleInfo() {
        System.out.println("This is a bicycle with pedals.");
        System.out.println("Pedal Type : " + pedalType);
    }
}

```
## Motorbike.java

public class Motorbike extends Bicycle {
    int engineCapacity;

    void showMotorbikeInfo() {
        System.out.println("This motorbike has an engine.");
        System.out.println("Engine Capacity : " + engineCapacity + " cc");
    }
}

## ElectricBike.java
public class ElectricBike extends Motorbike {
    int batteryCapacity;

    void showElectricBikeInfo() {
        System.out.println("This electric bike has an electric motor and battery.");
        System.out.println("Battery Capacity : " + batteryCapacity + " Wh");
    }
}

## TestVehicle.java
```
public class TestVehicle {
    public static void main(String[] args) {

        ElectricBike eBike = new ElectricBike();

        eBike.pedalType = "Standard Pedals";
        eBike.engineCapacity = 150;
        eBike.batteryCapacity = 500;

        eBike.showBicycleInfo();      // from Bicycle
        eBike.showMotorbikeInfo();    // from Motorbike
        eBike.showElectricBikeInfo(); // from ElectricBike
    }
}
```

# Output
![4b](https://github.com/user-attachments/assets/124b828a-cece-4133-ab34-d4d7bcd2d0ee)

## EXPERIMENT 4c
# TITLE 4c) To Find The Areas Of Different Shapes
## Figure.java
```
abstract class Figure {
    double dim1;
    double dim2;

    // Constructor
    Figure(double dim1, double dim2) {
        this.dim1 = dim1;
        this.dim2 = dim2;
    }

    // Abstract method
    abstract double area();
}
```
## Rectangle.java

class Rectangle extends Figure {

    // Constructor
    Rectangle(double length, double breadth) {
        super(length, breadth);
    }

    // Implementing abstract method
    double area() {
        return dim1 * dim2;
    }
}

## Triangle.java
class Triangle extends Figure {

    // Constructor
    Triangle(double base, double height) {
        super(base, height);
    }

    // Implementing abstract method
    double area() {
        return 0.5 * dim1 * dim2;
    }
}
## TestFigure.java
```
public class TestFigure {
    public static void main(String[] args) {

        Figure f1 = new Rectangle(10, 5);
        System.out.println("Area of Rectangle = " + f1.area());

        Figure f2 = new Triangle(8, 6);
        System.out.println("Area of Triangle = " + f2.area());
    }
}
```

# Output
![4c](https://github.com/user-attachments/assets/cec94c87-5efb-4494-93cc-02f34f64dc61)




