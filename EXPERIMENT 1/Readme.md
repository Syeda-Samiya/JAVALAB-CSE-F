# EXPERIMENT 1
## TITLE 1A) java program to display default value of all primitive datatypes of java 
```
class exp_1a {
    static byte b;
    static short s;
    static int i;
    static double d;
    static float f;
    static char c;
    static boolean bool;

    public static void main(String arg[]) {
        System.out.println("default primitive datatypes:");
        System.out.println("byte: " + b);
        System.out.println("short: " + s);
        System.out.println("int: " + i);
        System.out.println("double: " + d);
        System.out.println("float: " + f);
        System.out.println("char: " + c);
        System.out.println("bool: " + bool);
    }
}
```

# output
![EXPERIMENT 1 OUTPUT](exp1.png)


# EXPERIMENT 1B
## TITLE 1B) Display the quadratic roots
```
import java.util.Scanner;
class QuadraticRoots {
public static void main(String[] args) {
double a,b,c,D;
Scanner sc = new Scanner(System.in);
System.out.print("Enter value of a: ");
a=sc.nextDouble();
System.out.print("Enter value of b: ");
b=sc.nextDouble();
System.out.print("Enter value of c: ");
c=sc.nextDouble();
D=b*b-4*a*c;
System.out.println("Discriminant(D)="+D);
if (D>0) {
double x1 = (-b+Math.sqrt(D))/(2*a);
double x2 = (-b-Math.sqrt(D))/(2*a);
System.out.println("Roots are real and distinct.");
System.out.println("Rootl="+x1);
System.out.println("Root2="+x2);
} else if (D==0) {
double x=-b/(2*a);
System.out.println("Roots are real and equal.");
System.out.println("Root="+x);
} else {
double real=-b/(2*a);
double imaginary = Math.sqrt(-D)/(2*a);
System.out.println("Roots are imaginary (complex).");
System.out.println("Rootl="+real+"+1"+imaginary);
System.out.println("Root2="+real+"-1"+imaginary);
}
sc.close();
}
}
```

# output
![EXPERIMENT 1 OUTPUT](exp1B.png)



