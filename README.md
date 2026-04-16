[Program-1 WAP to add two numbers.](#assi-1)

[Program-2 Write a class for addition of two distances where each distance is given in km, cm, mm.](#assi-2)

[Program-3 Write a class for addition, subtraction, multiplication, division using object and classes Test the result by creation of objects in main class.](#assi-3)

[Program-4 Write a class for addition of two distances where each distance is given in meter and centimeters.  Test the result by creation of objects in main class.](#assi-4)

[Program-5 Write a class for addition of two times where each time is given in hour, minute and seconds. Test the result by creation of objects in main class.](#assi-5)

[Program-6 Collect the code from internet for any 5 programs of C language. Eg: factorial, palindrone, fibonacci, armstrong, pyramind of stars. create functions in single class](#assi-6)

[Program-7 Write a class that is having 4 methods for 1 dimensional array input, output original, output reverse, reverse.](#assi-7)

[Program-8 Write a class with multiple methods to perform matrix operations(Transpose, addition, sum of rows, sum of columns, sum of diagonals) on 3*3 matrix.](#assi-8)

[Program-9 Write a program using 3 classes to print 1 to 10, 1 to 10, 1 to 10, with and without thread and analze the output and repeat the same program using Runnable interface.](#assi-9)

[Program-10 Write a program using the concept of multithreading the output of all 3 threads must be synchronized(use join method for that).](#assi-10)


## assi-1
~~~

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


## assi-2
~~~

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

## assi-3
~~~

class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    int sub(int a, int b) {
        return a - b;
    }

    int mul(int a, int b) {
        return a * b;
    }

    int div(int a, int b) {
        return a / b;
    }
}

public class Assi_3 {
    public static void main(String args[]) {
        Calculator c = new Calculator();

        int a = 20, b = 10;

        System.out.println("Addition: " + c.add(a, b));
        System.out.println("Subtraction: " + c.sub(a, b));
        System.out.println("Multiplication: " + c.mul(a, b));
        System.out.println("Division: " + c.div(a, b));
    }
}
~~~
<img width="1668" height="240" alt="image" src="https://github.com/user-attachments/assets/69914111-b12f-485f-bd98-8820422e9e55" />

## assi-4
~~~
class Distance {
    int meter, cm;

    void input(int m, int c) {
        meter = m;
        cm = c;
    }

    Distance add(Distance d2) {
        Distance result = new Distance();

        result.cm = this.cm + d2.cm;
        result.meter = this.meter + d2.meter;

        if (result.cm >= 100) {
            result.meter++;
            result.cm -= 100;
        }

        return result;
    }

    void display() {
        System.out.println(meter + " meter " + cm + " cm");
    }
}

public class Assi_4 {
    public static void main(String args[]) {

        Distance d1 = new Distance();
        Distance d2 = new Distance();
        Distance d3;

        d1.input(5, 80);
        d2.input(4, 50);

        d3 = d1.add(d2);

        System.out.print("Total Distance: ");
        d3.display();
    }
}
~~~
<img width="1668" height="130" alt="image" src="https://github.com/user-attachments/assets/991247aa-b55e-41d0-b736-0e1f5be61467" />

## assi-5
~~~
import java.util.Scanner;

class Time {
    int hour, minute, second;

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter hour: ");
        hour = sc.nextInt();

        System.out.print("Enter minute: ");
        minute = sc.nextInt();

        System.out.print("Enter second: ");
        second = sc.nextInt();
    }

    Time add(Time t2) {
        Time result = new Time();

        result.second = this.second + t2.second;
        result.minute = this.minute + t2.minute;
        result.hour = this.hour + t2.hour;

        if (result.second >= 60) {
            result.second -= 60;
            result.minute++;
        }

        if (result.minute >= 60) {
            result.minute -= 60;
            result.hour++;
        }

        return result;
    }

    void display() {
        System.out.println(hour + " : " + minute + " : " + second);
    }
}

public class Program5 {
    public static void main(String args[]) {

        Time t1 = new Time();
        Time t2 = new Time();
        Time t3;

        System.out.println("Enter first time:");
        t1.input();

        System.out.println("Enter second time:");
        t2.input();

        t3 = t1.add(t2);

        System.out.print("Total Time = ");
        t3.display();
    }
}
~~~
<img width="1668" height="400" alt="image" src="https://github.com/user-attachments/assets/a9e871cf-5da2-440c-8d40-82ee93bef70a" />

## assi-6
~~~
import java.util.Scanner;

class CPrograms {

    void factorial(int n) {
        int fact = 1;
        for(int i = 1; i <= n; i++)
            fact = fact * i;

        System.out.println("Factorial = " + fact);
    }

    void fibonacci(int n) {
        int a = 0, b = 1, c;

        System.out.print("Fibonacci Series: ");
        for(int i = 1; i <= n; i++) {
            System.out.print(a + " ");
            c = a + b;
            a = b;
            b = c;
        }
        System.out.println();
    }

    void palindrome(int n) {
        int r, rev = 0, temp = n;

        while(n > 0) {
            r = n % 10;
            rev = rev * 10 + r;
            n = n / 10;
        }

        if(temp == rev)
            System.out.println("Number is Palindrome");
        else
            System.out.println("Number is Not Palindrome");
    }

    void armstrong(int n) {
        int r, sum = 0, temp = n;

        while(n > 0) {
            r = n % 10;
            sum = sum + (r * r * r);
            n = n / 10;
        }

        if(temp == sum)
            System.out.println("Number is Armstrong");
        else
            System.out.println("Number is Not Armstrong");
    }

    void pyramid(int rows) {
        System.out.println("Star Pyramid:");

        for(int i = 1; i <= rows; i++) {
            for(int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}

public class Program6 {

    public static void main(String args[]) {

        Scanner sc = new Scanner(System.in);
        CPrograms obj = new CPrograms();

        System.out.print("Enter number for factorial: ");
        int n1 = sc.nextInt();
        obj.factorial(n1);

        System.out.print("Enter number of terms for fibonacci: ");
        int n2 = sc.nextInt();
        obj.fibonacci(n2);

        System.out.print("Enter number to check palindrome: ");
        int n3 = sc.nextInt();
        obj.palindrome(n3);

        System.out.print("Enter number to check armstrong: ");
        int n4 = sc.nextInt();
        obj.armstrong(n4);

        System.out.print("Enter rows for pyramid: ");
        int rows = sc.nextInt();
        obj.pyramid(rows);
    }
}
~~~
<img width="834" height="332" alt="Screenshot 2026-03-09 at 10 41 08 AM" src="https://github.com/user-attachments/assets/9b60758a-688a-430d-a34a-4038e6b665eb" />

## assi-7
~~~
import java.util.Scanner;

class ArrayOperation {

    int arr[] = new int[5];

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter 5 elements of array:");
        for(int i = 0; i < 5; i++) {
            arr[i] = sc.nextInt();
        }
    }

    void displayOriginal() {
        System.out.println("Original Array:");
        for(int i = 0; i < 5; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    void displayReverse() {
        System.out.println("Array in Reverse Order:");
        for(int i = 4; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }

    void reverseArray() {
        for(int i = 0; i < 5/2; i++) {
            int temp = arr[i];
            arr[i] = arr[4 - i];
            arr[4 - i] = temp;
        }

        System.out.println("Array after reversing:");
        for(int i = 0; i < 5; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}

public class Program7 {

    public static void main(String args[]) {

        ArrayOperation obj = new ArrayOperation();

        obj.input();
        obj.displayOriginal();
        obj.displayReverse();
        obj.reverseArray();
    }
}
~~~
<img width="1668" height="664" alt="image" src="https://github.com/user-attachments/assets/fc72b567-f19d-46a5-a0a9-5b52e9ea56ea" />

## assi-8
~~~
import java.util.Scanner;

class Matrix {

    int a[][] = new int[3][3];

    void input() {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter elements of 3x3 matrix:");

        for(int i=0;i<3;i++) {
            for(int j=0;j<3;j++) {
                a[i][j] = sc.nextInt();
            }
        }
    }

    void display() {
        System.out.println("Original Matrix:");

        for(int i=0;i<3;i++) {
            for(int j=0;j<3;j++) {
                System.out.print(a[i][j] + " ");
            }
            System.out.println();
        }
    }

    void transpose() {
        System.out.println("Transpose of Matrix:");

        for(int i=0;i<3;i++) {
            for(int j=0;j<3;j++) {
                System.out.print(a[j][i] + " ");
            }
            System.out.println();
        }
    }

    void sumRows() {
        System.out.println("Sum of each row:");

        for(int i=0;i<3;i++) {
            int sum = 0;
            for(int j=0;j<3;j++) {
                sum = sum + a[i][j];
            }
            System.out.println("Row " + (i+1) + " Sum = " + sum);
        }
    }

    void sumColumns() {
        System.out.println("Sum of each column:");

        for(int j=0;j<3;j++) {
            int sum = 0;
            for(int i=0;i<3;i++) {
                sum = sum + a[i][j];
            }
            System.out.println("Column " + (j+1) + " Sum = " + sum);
        }
    }

    void sumDiagonal() {
        int sum = 0;

        for(int i=0;i<3;i++) {
            sum = sum + a[i][i];
        }

        System.out.println("Sum of main diagonal = " + sum);
    }
}

public class Program8 {

    public static void main(String args[]) {

        Matrix m = new Matrix();

        m.input();
        m.display();
        m.transpose();
        m.sumRows();
        m.sumColumns();
        m.sumDiagonal();
    }
}
~~~
<img width="1668" height="880" alt="image" src="https://github.com/user-attachments/assets/969beb32-13a4-48db-91b1-ab5984d50de3" />

## assi-9
~~~
class ClassA {
    public void printName() {
        for (int i = 0; i < 100; i++) {
            System.out.println("ClassA "+i);
        }
    }
}
class ClassB {
    public void printName() {
        for (int i = 0; i < 100; i++) {
            System.out.println("ClassB "+i);
        }
    }
}
class ClassC {
    public void printName() {
        for (int i = 0; i < 100; i++) {
            System.out.println("ClassC "+i);
        }
    }
}
public class Tanvi_B1 {

    public static void main(String[] args) {
        ClassA a = new ClassA();
        ClassB b = new ClassB();
        ClassC c = new ClassC();

        a.printName();
        b.printName();
        c.printName();
    }
}
~~~
<img width="770" height="593" alt="image" src="https://github.com/user-attachments/assets/32cb4648-302b-4ade-bac4-95f681332405" />

~~~
class ClassA_th extends Thread{
    @Override
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println("ClassA "+i);
        }
    }
}
class ClassB_th extends Thread{
    @Override
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println("ClassB "+i);
        }
    }
}
class ClassC_th extends Thread{
    @Override
    public void run() {
        for (int i = 0; i < 10; i++) {
            System.out.println("ClassC "+i);
        }
    }
}
public class Tanvi_B1_Thread {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        ClassA_th a = new ClassA_th();
        ClassB_th b = new ClassB_th();
        ClassC_th  c = new ClassC_th();

        a.start();
        b.start();
        c.start();
    }
    
}
~~~
<img width="864" height="554" alt="image" src="https://github.com/user-attachments/assets/91624d7b-7a26-4d51-a734-97fdc6dfbcd0" />

~~~
class ClassA_thi implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i < 100; i++) {
            System.out.println("ClassA "+i);
        }
    }
}
class ClassB_thi implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i < 100; i++) {
            System.out.println("ClassB "+i);
        }
    }
}
class ClassC_thi implements Runnable{
    @Override
    public void run() {
        for (int i = 0; i < 100; i++) {
            System.out.println("ClassC "+i);
        }
    }
}
public class Tanvi_B1_Runable {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        ClassA_thi a = new ClassA_thi();
        Thread th1= new Thread(a);
        ClassB_thi b = new ClassB_thi();
        Thread th2= new Thread(b);
        ClassC_thi c = new ClassC_thi();
        Thread th3= new Thread(c);
        th1.start();
        th2.start();
        th3.start();
    }
    
}
~~~
<img width="1033" height="560" alt="image" src="https://github.com/user-attachments/assets/6ff0731f-4166-49eb-b73b-114c3f297c3c" />






