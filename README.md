Q1
Code:

import java.util.*;
public class Reverse {
    public static void reverse(double[] arr) {
        List<Double> list = new ArrayList<>();
        for (double num : arr) {
            list.add(num);
        }
        Collections.reverse(list);
        for (int i = 0; i < arr.length; i++) {
            arr[i] = list.get(i);
        }
    }

    public static void main(String[] args) {
        double[] arr = {5.8, 2.6, 9.0, 3.4, 7.1};
        System.out.println("Initial Array:");
        for (double num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
        reverse(arr);
        System.out.println("Reversed Array:");
        for (double num : arr) {
            System.out.print(num + " ");
        }
    }
}

Output:
Initial Array:
5.8 2.6 9.0 3.4 7.1 
Reversed Array:
7.1 3.4 9.0 2.6 5.8 

Q2
Code:

import java.util.Scanner;
public class Divisors {

    public static void printDivisors(int num) {
        for (int i = num; i >= 1; i--) {
            if (num % i == 0) {
                System.out.println(i);
            }
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String choice = "Y";
        while (choice.equalsIgnoreCase("Y")) {
            System.out.print("Please enter a positive integer: ");
            int num = scanner.nextInt();
            if (num <= 0) {
                if (num == 0) {
                    System.out.println("0 is not a positive integer.");
                } else {
                    System.out.println(num + " is not a positive integer.");
                }
                continue;
            }
            printDivisors(num);
            System.out.print("Would you like to see the divisors of another integer (Y/N)? ");
            choice = scanner.next();
            System.out.println();
        }
        scanner.close();
    }
}


Output:
Please enter a positive integer: 36
36
18
12
9
6
4
3
2
1
Would you like to see the divisors of another integer (Y/N)? y

Please enter a positive integer: -44
-44 is not a positive integer.
Please enter a positive integer: 0
0 is not a positive integer.
Please enter a positive integer: 109
109
1
Would you like to see the divisors of another integer (Y/N)? n
