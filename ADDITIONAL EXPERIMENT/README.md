# ADDITIONAL EXPERIMENT 2
## TITLE 2)Display the fibinacci series
```
import java.util.Scanner;

class Fibonacci {
    void displayAndSum(int n) {
        int a = 0, b = 1, c;
        int sum;
        if (n == 1) {
            System.out.println("Fibonacci numbers: 0");
            System.out.println("sum = 0");
            return;
        }
        if (n == 2) {
            System.out.println("Fibonacci numbers: 0 1");
            System.out.println("sum = 1");
            return;
        }
        sum = a + b;
        System.out.println("Fibonacci numbers: " + a + " " + b);
        for (int i = 3; i <= n; i++) {
            c = a + b;
            System.out.print(c + " ");
            sum = sum + c;
            a = b;
            b = c;
        }
        System.out.println();
        System.out.println("sum = " + sum);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter n: ");
        int n = sc.nextInt();
        Fibonacci fib = new Fibonacci();
        fib.displayAndSum(n);
    }
}
```
# output
![additional exp](https://github.com/user-attachments/assets/b4e7bbf3-1b5f-4949-a762-7ac99fab7b16)
