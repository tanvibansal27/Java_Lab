[Program-1 WAP to add two numbers]((#assi-1)

[Program-2 WAP to add two objects](#assi-2)
~~~
## assi-1
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Class.java to edit this template
 */
package tanvi_b1;

import java.util.Scanner;

/**
 *
 * @author IBM24
 */
public class add_Num {
     public static void main(String[] args){
         AddNumbers obj = new AddNumbers();

        obj.input();
        obj.add();
        obj.display();
     }
}
class AddNumbers {
    int num1;
    int num2;
    int sum;

    // Input function
    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first number: ");
        num1 = sc.nextInt();
        System.out.print("Enter second number: ");
        num2 = sc.nextInt();
    }

    // Add function
    void add() {
        sum = num1 + num2;
    }

    // Output function
    void display() {
        System.out.println("Sum = " + sum);
    }
}
~~~
<img width="601" height="236" alt="image" src="https://github.com/user-attachments/assets/9f3e6650-2fab-43f2-ba45-147b8d43016c" />
## assi-1

~~~
## assi-2
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package tanvi_b1;

import java.util.Scanner;

/**
 *
 * @author IBM24
 */
public class Tanvi_B1 {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Distance d1 = new Distance();
        Distance d2 = new Distance();

        System.out.println("Enter First Distance:");
        d1.input();

        System.out.println("Enter Second Distance:");
        d2.input();

        Distance sum = d1.add(d2);

        System.out.println("Sum of Distances:");
        sum.display();
    }
    
}
class Distance {
    int km;
    int cm;
    int mm;

    // Input function
    void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter kilometers: ");
        km = sc.nextInt();
        System.out.print("Enter centimeters: ");
        cm = sc.nextInt();
        System.out.print("Enter millimeters: ");
        mm = sc.nextInt();
    }

    // Add function
    Distance add(Distance d2) {
        Distance result = new Distance();

        result.km = this.km + d2.km;
        result.cm = this.cm + d2.cm;
        result.mm = this.mm + d2.mm;

        // Convert mm to cm
        if (result.mm >= 10) {
            result.cm += result.mm / 10;
            result.mm = result.mm % 10;
        }

        // Convert cm to km
        if (result.cm >= 100000) {  // 1 km = 100000 cm
            result.km += result.cm / 100000;
            result.cm = result.cm % 100000;
        }

        return result;
    }

    // Output function
    void display() {
        System.out.println("Distance = " + km + " km " + cm + " cm " + mm + " mm");
    }
}
~~~
<img width="1256" height="395" alt="image" src="https://github.com/user-attachments/assets/81b738ad-3ca7-4645-a480-b6c190687a31" />
## assi-2
