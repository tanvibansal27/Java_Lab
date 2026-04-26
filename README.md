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

[Program-11 Write a program to demonstrate Java collection Framewrok List).](#assi-11)

[Program-12 Write a program to demonstrate Java collection Framewrok Linked List).](#assi-12)

[Program-13 Write a program to demonstrate Java collection Framewrok Stack).](#assi-13)

[Program-14 Write a program to demonstrate Java collection Framewrok Hashmap).](#assi-14)

[Program-15 Write a program to demonstrate Java collection Framewrok Queue).](#assi-15)

[Program-16 Addition of 2 numbers using swing.](#assi-16)

[Program-17 Make a registration form with 10 elements and send the data into database (use jdbc connectivity)](#assi-17)

[Program-18 Make one calculator in swing.](#assi-18)

[Program-19 Matrix Addition using swing class.](#assi-19)

[Program-20 Create one jframe apply 10 buttons on that after clicking on each button a new
structure is created.(Circle, oval rectangle, etc ....) ](#assi-20)

[Program-21 Just using mouse Event create a frame like paint brush with selection of colour and width.](#assi-21)

[Program-22 Create a package of any 5 classes of your choice and import it.](#assi-22)

[Program-23 Create one package and sub package  import and test it .](#assi-23)

[Program-24 Create one small array of size 5 apply array out of bounds exception using try catch give a proper message in catch and demonstrate the exception exactly in the same fashion demonstrate arithmetic exception .](#assi-24)

[Program-25 To test the range of age of one student.write a program using user defined exception.
](#assi-25)

[Program-26 File Handling Programs (given in the PPT)](#assi-26)

[Program-27 Inheritance Programs, using interface and abstract classes.](#assi-27)


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

## assi-10
~~~
class MyThread extends Thread {
    private String threadName;

    MyThread(String name) {
        threadName = name;
    }

    public void run() {
        for (int i = 1; i <= 3; i++) {
            System.out.println(threadName + " is running: " + i);
            try {
                Thread.sleep(500); // just to slow down output
            } catch (InterruptedException e) {
                System.out.println(e);
            }
        }
        System.out.println(threadName + " finished.");
    }
}

public class MultiThreadJoinExample {
    public static void main(String[] args) {

        MyThread t1 = new MyThread("Thread 1");
        MyThread t2 = new MyThread("Thread 2");
        MyThread t3 = new MyThread("Thread 3");

        try {
            t1.start();
            t1.join(); // wait for t1 to finish

            t2.start();
            t2.join(); // wait for t2 to finish

            t3.start();
            t3.join(); // wait for t3 to finish

        } catch (InterruptedException e) {
            System.out.println(e);
        }

        System.out.println("All threads have finished execution.");
    }
}
~~~
<img width="1592" height="812" alt="image" src="https://github.com/user-attachments/assets/768f2104-c832-448c-9240-2b5b404d4548" />


## assi-11
~~~
import java.util.*;
public class List_Interface {
    public static void main(String[] args) {
        // TODO code application logic here
        List<String> list = new ArrayList<>();
        list.add("Apple");
        list.add("Banana");
        list.add("Mango");
        
        for(String fruit : list){
            System.out.println(fruit);
        }  
        
        list.add(1,"orange");
        System.out.println("Element at index 1 after modifying : " + list.get(1));
        
        list.set(0,"grapes");
        
        list.remove("Banana");
        
        System.out.println("sise: " + list.size());
        
    }
}
~~~
<img width="678" height="352" alt="image" src="https://github.com/user-attachments/assets/d0d0ea16-36b9-4571-8925-68e21c62a679" />

## assi-12
~~~
import java.util.LinkedList;

public class LinkedListDemo {
    public static void main(String[] args) {

        // Create a LinkedList
        LinkedList<String> list = new LinkedList<>();

        
        list.add("Apple");
        list.add("Banana");
        list.add("Cherry");

        
        list.addFirst("Mango");
        list.addLast("Orange");

        System.out.println("List: " + list);

        
        System.out.println("First element: " + list.getFirst());
        System.out.println("Last element: " + list.getLast());
        System.out.println("Element at index 2: " + list.get(2));

        
        list.set(1, "Pineapple");
        System.out.println("After update: " + list);

        
        list.remove("Cherry");
        list.removeFirst();
        list.removeLast();

        System.out.println("After removals: " + list);

        
        System.out.println("Contains Banana? " + list.contains("Banana"));

       
        System.out.println("Size: " + list.size());

       
        System.out.println("Iterating:");
        for (String item : list) {
            System.out.println(item);
        }
    }
}
~~~
<img width="622" height="263" alt="image" src="https://github.com/user-attachments/assets/f15a7ecd-a56d-42a3-8ce4-6bfe5b812ec5" />

## assi-13
~~~
import java.util.Stack;

public class StackDemo {
    public static void main(String[] args) {

        // Create a Stack
        Stack<Integer> stack = new Stack<>();

        // Push elements
        stack.push(10);
        stack.push(20);
        stack.push(30);

        System.out.println("Stack: " + stack);

        // Peek (top element)
        System.out.println("Top element: " + stack.peek());

        // Pop (remove top)
        System.out.println("Popped: " + stack.pop());

        System.out.println("Stack after pop: " + stack);

        // Check if empty
        System.out.println("Is empty? " + stack.isEmpty());

        // Search element
        System.out.println("Position of 10: " + stack.search(10));
    }
}
~~~
<img width="617" height="230" alt="image" src="https://github.com/user-attachments/assets/570fcaa5-647a-4a00-8a54-c5062d67f614" />

## assi-14
~~~
import java.util.HashMap;

public class HashMapDemo {
    public static void main(String[] args) {

        // Create a HashMap
        HashMap<Integer, String> map = new HashMap<>();

        // Put elements (key, value)
        map.put(1, "Apple");
        map.put(2, "Banana");
        map.put(3, "Cherry");

        System.out.println("Map: " + map);

        // Access value
        System.out.println("Key 2 value: " + map.get(2));

        // Update value
        map.put(2, "Mango");
        System.out.println("After update: " + map);

        // Remove element
        map.remove(3);
        System.out.println("After removal: " + map);

        // Check key/value
        System.out.println("Contains key 1? " + map.containsKey(1));
        System.out.println("Contains value Apple? " + map.containsValue("Apple"));

        // Size
        System.out.println("Size: " + map.size());

        // Iterate
        System.out.println("Iterating:");
        for (Integer key : map.keySet()) {
            System.out.println(key + " -> " + map.get(key));
        }
    }
}
~~~
<img width="586" height="355" alt="image" src="https://github.com/user-attachments/assets/77b5cee3-7fdc-4123-bdb0-33aea71a858d" />

## assi-15
~~~
import java.util.LinkedList;
import java.util.Queue;

public class QueueDemo {
    public static void main(String[] args) {

        // Create Queue
        Queue<Integer> queue = new LinkedList<>();

        // Add elements
        queue.add(10);
        queue.add(20);
        queue.add(30);

        System.out.println("Queue: " + queue);

        // Access head
        System.out.println("Head (peek): " + queue.peek());

        // Remove element
        System.out.println("Removed: " + queue.poll());

        System.out.println("Queue after removal: " + queue);

        // Check empty
        System.out.println("Is empty? " + queue.isEmpty());

        // Size
        System.out.println("Size: " + queue.size());
    }
}
~~~
<img width="604" height="158" alt="image" src="https://github.com/user-attachments/assets/4ff7881c-75c9-4c6e-b194-f34ae4beb5ab" />

## assi-16
~~~
import javax.swing.*;
import java.awt.event.*;

public class AdditionSwing {
    public static void main(String[] args) {

        // Create frame
        JFrame frame = new JFrame("Addition Calculator");
        frame.setSize(300, 200);
        frame.setLayout(null);

        // Labels
        JLabel l1 = new JLabel("Enter Number 1:");
        l1.setBounds(20, 20, 120, 25);
        frame.add(l1);

        JLabel l2 = new JLabel("Enter Number 2:");
        l2.setBounds(20, 60, 120, 25);
        frame.add(l2);

        JLabel resultLabel = new JLabel("Result:");
        resultLabel.setBounds(20, 140, 200, 25);
        frame.add(resultLabel);

        // Text fields
        JTextField t1 = new JTextField();
        t1.setBounds(150, 20, 100, 25);
        frame.add(t1);

        JTextField t2 = new JTextField();
        t2.setBounds(150, 60, 100, 25);
        frame.add(t2);

        // Button
        JButton btn = new JButton("Add");
        btn.setBounds(90, 100, 100, 30);
        frame.add(btn);

        // Action Listener
        btn.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                try {
                    int num1 = Integer.parseInt(t1.getText());
                    int num2 = Integer.parseInt(t2.getText());
                    int sum = num1 + num2;

                    resultLabel.setText("Result: " + sum);
                } catch (NumberFormatException ex) {
                    JOptionPane.showMessageDialog(frame, "Please enter valid numbers!");
                }
            }
        });

        // Frame settings
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }
}
~~~
<img width="881" height="577" alt="image" src="https://github.com/user-attachments/assets/b9fcc653-004b-4b58-9481-b554a021a64e" />

## assi-17
~~~
import javax.swing.*;
import java.awt.event.*;
import java.sql.*;

public class RegistrationForm {
    public static void main(String[] args) {
        JFrame f = new JFrame("Registration");

        JTextField name = new JTextField();
        JTextField email = new JTextField();
        JPasswordField pass = new JPasswordField();
        JButton submit = new JButton("Submit");

        name.setBounds(100, 30, 150, 25);
        email.setBounds(100, 70, 150, 25);
        pass.setBounds(100, 110, 150, 25);
        submit.setBounds(100, 150, 100, 30);

        f.add(new JLabel("Name")).setBounds(20, 30, 80, 25);
        f.add(new JLabel("Email")).setBounds(20, 70, 80, 25);
        f.add(new JLabel("Password")).setBounds(20, 110, 80, 25);

        f.add(name); f.add(email); f.add(pass); f.add(submit);

        submit.addActionListener(e -> {
            try {
                Connection con = DriverManager.getConnection(
                    "jdbc:mysql://localhost:3306/test", "root", "password");

                PreparedStatement ps = con.prepareStatement(
                    "INSERT INTO users VALUES (?, ?, ?)");

                ps.setString(1, name.getText());
                ps.setString(2, email.getText());
                ps.setString(3, new String(pass.getPassword()));

                ps.executeUpdate();
                JOptionPane.showMessageDialog(f, "Data Inserted!");

            } catch (Exception ex) {
                System.out.println(ex);
            }
        });

        f.setSize(300, 250);
        f.setLayout(null);
        f.setVisible(true);
    }
}
~~~
<img width="379" height="314" alt="image" src="https://github.com/user-attachments/assets/ae929320-5685-4f00-a9b6-2a4652809964" />

## assi-18
~~~
import javax.swing.*;
import java.awt.event.*;

public class Calculator {
    public static void main(String[] args) {
        JFrame f = new JFrame("Calculator");

        JTextField t1 = new JTextField();
        JTextField t2 = new JTextField();
        JLabel result = new JLabel("Result:");

        JButton add = new JButton("+");
        JButton sub = new JButton("-");

        t1.setBounds(50, 30, 100, 30);
        t2.setBounds(50, 70, 100, 30);
        add.setBounds(30, 110, 50, 30);
        sub.setBounds(100, 110, 50, 30);
        result.setBounds(50, 150, 150, 30);

        add.addActionListener(e -> {
            int a = Integer.parseInt(t1.getText());
            int b = Integer.parseInt(t2.getText());
            result.setText("Result: " + (a + b));
        });

        sub.addActionListener(e -> {
            int a = Integer.parseInt(t1.getText());
            int b = Integer.parseInt(t2.getText());
            result.setText("Result: " + (a - b));
        });

        f.add(t1); f.add(t2); f.add(add); f.add(sub); f.add(result);
        f.setSize(250, 250);
        f.setLayout(null);
        f.setVisible(true);
    }
}
~~~
<img width="379" height="314" alt="image" src="https://github.com/user-attachments/assets/e20fe662-2ad0-4dcc-9e88-a3969b6013e0" />
<img width="379" height="314" alt="image" src="https://github.com/user-attachments/assets/9de77d37-b62c-4506-8c98-f946b69ef137" />

## assi-19
~~~
import javax.swing.*;
import java.awt.event.*;

// Class for Matrix Logic
class Matrix {
    int[][] A = new int[2][2];
    int[][] B = new int[2][2];
    int[][] C = new int[2][2];

    // Method to add matrices
    public void add() {
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                C[i][j] = A[i][j] + B[i][j];
            }
        }
    }
}

// GUI Class
class MatrixGUI extends JFrame implements ActionListener {

    JTextField[][] aField = new JTextField[2][2];
    JTextField[][] bField = new JTextField[2][2];
    JTextField[][] resultField = new JTextField[2][2];

    JButton addBtn;
    Matrix m = new Matrix();

    MatrixGUI() {
        setTitle("Matrix Addition");
        setSize(400, 400);
        setLayout(null);

        int x = 30, y = 30;

        // Matrix A input
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                aField[i][j] = new JTextField();
                aField[i][j].setBounds(x + j * 40, y + i * 40, 35, 35);
                add(aField[i][j]);
            }
        }

        // Matrix B input
        x = 150;
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                bField[i][j] = new JTextField();
                bField[i][j].setBounds(x + j * 40, y + i * 40, 35, 35);
                add(bField[i][j]);
            }
        }

        // Result Matrix
        x = 270;
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 2; j++) {
                resultField[i][j] = new JTextField();
                resultField[i][j].setBounds(x + j * 40, y + i * 40, 35, 35);
                resultField[i][j].setEditable(false);
                add(resultField[i][j]);
            }
        }

        // Button
        addBtn = new JButton("Add");
        addBtn.setBounds(150, 150, 80, 30);
        add(addBtn);

        addBtn.addActionListener(this);

        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        try {
            // Take input
            for (int i = 0; i < 2; i++) {
                for (int j = 0; j < 2; j++) {
                    m.A[i][j] = Integer.parseInt(aField[i][j].getText());
                    m.B[i][j] = Integer.parseInt(bField[i][j].getText());
                }
            }

            // Perform addition
            m.add();

            // Show result
            for (int i = 0; i < 2; i++) {
                for (int j = 0; j < 2; j++) {
                    resultField[i][j].setText(String.valueOf(m.C[i][j]));
                }
            }

        } catch (Exception ex) {
            JOptionPane.showMessageDialog(this, "Enter valid numbers!");
        }
    }
}

// Main Class
public class MatrixAdditionApp {
    public static void main(String[] args) {
        new MatrixGUI();
    }
}
~~~
<img width="403" height="404" alt="image" src="https://github.com/user-attachments/assets/a9e6c6e6-84c8-493f-85fc-24f480a00ee6" />

## assi-20
~~~
import javax.swing.*;
import java.awt.*;

public class Shapes extends JPanel {
    String shape = "";

    public void paint(Graphics g) {
        super.paint(g);
        if(shape.equals("circle")) g.drawOval(100,100,50,50);
        if(shape.equals("rect")) g.drawRect(100,100,80,50);
    }

    public static void main(String[] args) {
        JFrame f = new JFrame();
        Shapes s = new Shapes();

        JButton b1 = new JButton("Circle");
        JButton b2 = new JButton("Rectangle");

        b1.addActionListener(e -> { s.shape="circle"; s.repaint(); });
        b2.addActionListener(e -> { s.shape="rect"; s.repaint(); });

        f.add(b1, BorderLayout.NORTH);
        f.add(b2, BorderLayout.SOUTH);
        f.add(s);

        f.setSize(400,400);
        f.setVisible(true);
    }
}
~~~
<img width="403" height="404" alt="image" src="https://github.com/user-attachments/assets/34567b4c-c3e2-45a6-bbf6-015413fca50a" />

<img width="403" height="404" alt="image" src="https://github.com/user-attachments/assets/88a6ad4d-acef-4d6e-b846-0b983be79dbf" />

## assi-21
~~~
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class PaintApp extends JFrame {
    int x,y;

    public PaintApp() {
        addMouseMotionListener(new MouseMotionAdapter() {
            public void mouseDragged(MouseEvent e) {
                x = e.getX();
                y = e.getY();
                repaint();
            }
        });

        setSize(400,400);
        setVisible(true);
    }

    public void paint(Graphics g) {
        g.fillOval(x, y, 5, 5);
    }

    public static void main(String[] args) {
        new PaintApp();
    }
}
~~~
<img width="403" height="404" alt="image" src="https://github.com/user-attachments/assets/39d4cd1f-9caa-42d1-a323-a52998616a60" />

## assi-22
~~~
package mypack;
1.A.java
package mypack;

public class A {
    public void showA() {
        System.out.println("This is Class A");
    }
}
2.B.java
package mypack;

public class B {
    public void showB() {
        System.out.println("This is Class B");
    }
}
3 C.java
package mypack;

public class C {
    public void showC() {
        System.out.println("This is Class C");
    }
}
4 D.java
package mypack;

public class D {
    public void showD() {
        System.out.println("This is Class D");
    }
}
5 E.java
package mypack;

public class E {
    public void showE() {
        System.out.println("This is Class E");
    }
}
6 main file
import mypack.*;

public class TestPackage {
    public static void main(String[] args) {

        A a = new A();
        B b = new B();
        C c = new C();
        D d = new D();
        E e = new E();

        a.showA();
        b.showB();
        c.showC();
        d.showD();
        e.showE();
    }
}
~~~

## assi-23
~~~
package pack.subpack;
public class Test {
    public void show(){ System.out.println("Subpackage"); }
}
~~~

## assi-24
~~~
public class ExceptionDemo {
    public static void main(String[] args) {

        int[] arr = new int[5];

        try {
            arr[10] = 5;
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array index out of bounds!");
        }

        try {
            int a = 10/0;
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero!");
        }
    }
}
~~~
<img width="1232" height="504" alt="image" src="https://github.com/user-attachments/assets/0a06f981-a710-4ee4-a0b7-30b5e7beaec1" />

## assi-25
~~~
class InvalidAgeException extends Exception {
    InvalidAgeException(String msg){
        super(msg);
    }
}

public class AgeTest {
    static void checkAge(int age) throws InvalidAgeException {
        if(age < 18)
            throw new InvalidAgeException("Age must be 18+");
    }

    public static void main(String[] args) {
        try {
            checkAge(15);
        } catch(Exception e){
            System.out.println(e.getMessage());
        }
    }
}
~~~
<img width="1232" height="504" alt="image" src="https://github.com/user-attachments/assets/2128e0ef-d377-43dc-afed-9c39389a88f4" />

## assi-26
~~~
import java.io.*;

public class FileDemo {
    public static void main(String[] args) throws Exception {
        FileWriter fw = new FileWriter("test.txt");
        fw.write("Hello Java");
        fw.close();

        FileReader fr = new FileReader("test.txt");
        int i;
        while((i=fr.read())!=-1)
            System.out.print((char)i);
    }
}
~~~
<img width="1232" height="504" alt="image" src="https://github.com/user-attachments/assets/3ef54ed6-46bc-470f-9f0c-bcd5fa474eba" />

## assi-27
~~~
abstract class Animal {
    abstract void sound();
}

interface Run {
    void run();
}

class Dog extends Animal implements Run {
    void sound() { System.out.println("Bark"); }
    public void run() { System.out.println("Running"); }
}

public class Test {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.sound();
        d.run();
    }
}
~~~
<img width="1232" height="504" alt="image" src="https://github.com/user-attachments/assets/22c55b88-608f-4a13-af0e-5cfa6020ac55" />

