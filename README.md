* # Table of content 
1. Data structure
     *  types of data structure in java
2.  Data types 
    * primitive data types
    * Non-primitive data types
 3.  Conclusion
 4.  Reference



# 1. Data Structure in java
* The data structure is a way of storing and organizing data efficiently such that the required operations on them can be performed efficiently concerning time as well as memory. Simply, Data Structure is used to reduce the complexity (mostly the time complexity) of the code.

* Data Structure is a way to store and organize data so that it can be used efficiently.

* Data Structures (DS) tutorial provides basic and advanced concepts of Data Structure. Our Data Structure tutorial is designed for beginners and professionals.


* Our Data Structure tutorial includes all topics of Data Structure such as Array, Pointer, Structure, Linked List, Stack, Queue, Graph, Searching, Sorting, Programs, etc.

## Types of Data Structures in java

* Array
* Linked List
* Stack 
* Queue
* Binary Tree
* Binary Search Tree
* Heap
* Hashing 


![wety](https://d1m75rqqgidzqn.cloudfront.net/wp-data/2022/07/22114048/image-6.png)
*  ##  Example Java Program using Array

import java.utiil.*

class JavaDemo {

	public static void main (String[] args) {
	    int[] priceOfPen= new int[5];
	    Scanner in=new Scanner(System.in);
	    for(int i=0;i<priceOfPen.length;i++)
	        priceOfPen[i]=in.nextInt();

	    for(int i=0;i<priceOfPen.length;i++)
		    System.out.print(priceOfPen[i]+" ");
	}
}


Input:
23 13 56 78 10

Output:
23 13 56 78 10 
* ## Example of Binary Tree
class TLNode
{
 int data;
 TLNode left,right;
 
 TLNode(int d)
 {
   data=d;
  }
 }
 
 * ## Example of Binary Tree
class TLNode
{
 int data;
 TLNode left,right;
 
 TLNode(int d)
 {
   data=d;
  }
 }
 
 
public class BinaryTree
{
   static void preorder(TLNode r)
   {
		if(r==null)
		    return;
		
		System.out.print(r.data+" ");
		
		preorder(r.left);
		preorder(r.right);
		
   }
   static void in order(TLNode r)
   {
		if(r==null)
		    return;
		
		
		inorder(r.left);
		System.out.print(r.data+" ");
		inorder(r.right);
		
   }
   static void postorder(TLNode r)
   {
		if(r==null)
		    return;
		
		
		postorder(r.left);
		postorder(r.right);
		System.out.print(r.data+" ");

   }
     
    public static void main(String[] args)
	{
		TLNode root=new TLNode(1);
		
		root.left=new TLNode(2);
		root.right=new TLNode(3);
		
		root.left.left=new TLNode(4);
		root.left.right=new TLNode(5);
		
		root.right.left=new TLNode(6);
		root.right.right=new TLNode(7);
		preorder(root);
		System.out.println();
		
		inorder(root);
		System.out.println();
		
		postorder(root);
		System.out.println();
		
		
	}
}



	 
####  Output
	
1 2 4 5 3 6 7 

4 2 5 1 6 3 7 

4 5 2 6 7 3 1 

 





#   2. Data Types in Java
* Data types specify the different sizes and values that can be stored in the variable. There are two types of data types in Java :

* Primitive data types: The primitive data types include boolean, char, byte, short, int, long, float, and double.
* Non-primitive data types: The non-primitive data types include Classes
, Interfaces, and Arrays
.
 *  ### Java Primitive Data Types
In Java language, primitive data types are the building blocks of data manipulation. These are the most basic data types available in Java language.
 *  There are 8 types of primitive data types:



* boolean data type
* byte data type
* char data type
* short data type
* int data type
* long data type
* float data type
* double data type
![image](https://static.javatpoint.com/images/java-data-types.png)



* Whenever a non-primitive data type is defined, it refers to a memory location where the data is stored in heap memory i.e., it refers to the memory location where an object is placed. Therefore, a non-primitive data type variable is also called referenced data type or simply an object reference variable.

* An object reference variable lives on the stack memory and the object to which it points always lives on the heap memory. The stack holds a pointer to the object on the heap.

* In Java programming, all non-primitive data types are simply called objects that are created by instantiating a class.

#### Key points:
* The default value of any reference variable is null.
* Whenever we are passing a non-primitive data type to a method, we are passing the address of that object where the data is stored.

* ## Types of Non-primitive data types
* There are five types of non-primitive data types in Java. They are as follows:

* Class
* Object
* String
* Array
* Interface

1. ## Class and objects:
A class
in Java is a user-defined data type i.e. it is created by the user. It acts as a template for the data which consists of member variables and methods.

An object
is the variable of the class, which can access the elements of the class i.e. methods and variables.

Example:


In the following example, we are creating a class containing the variables and methods ( add() and sub() ). Here, we are accessing the methods using the object of the Class obj.

ClassExample.java

public class ClassExample {  
      
        // defining the variables of class  
        int a = 20;  
        int b = 10;  
        int c;  
  
        // defining the methods of class  
        public void add () {  
            int c = a + b;  
            System. out.println("Addition of numbers is: " + c);  
        }  
  
        public void sub () {  
            int c = a - b;  
            System.out.println("Subtraction of numbers is: " + c);  
        }  
      
    // main method  
    public static void main (String[] args) {  
        // creating the object of class  
        ClassExample obj = new ClassExample();  
  
        // calling the methods  
        obj.add();  
        obj.sub();  
    }  
}  
Output:

The addition of numbers is: 30

Subtraction of numbers is: 10

## 2.Interface:
* An interface
is similar to a class however the only difference is that its methods are abstract by default i.e. they do not have the body. An interface has only the final variables and method declarations. It is also called a fully abstract class.

* Note: If the class implements an interface, it must implement all the methods of that interface. If not, we must declare the class as abstract.
### Example:


* In the following example, we are creating the interface CalcInterface with two abstract methods ( multiply() and divide() ). Here, the class InterfaceExample implements the interface and further defines the methods of that interface. Then, the object of a class is used to access those methods.

InterfaceExample.java

interface CalcInterface {  
    void multiply();  
    void divide();  
}  
public class InterfaceExample implements CalcInterface {  
      
        // defining the variables of class  
        int a = 10;  
        int b = 20;  
        int c;  
  
        // implementing the interface methods  
        public void multiply() {  
            int c = a * b;  
            System. out.println("Multiplication of numbers is: " + c);  
        }  
        public void divide() {  
            int c = a / b;  
            System.out.println("Division of numbers is: " + c);  
        }  
    // main method  
    public static void main (String[] args) throws IOException {  
        InterfaceExample obj = new InterfaceExample();  
        // calling the methods  
        obj.multiply();  
        obj.divide();  
    }  
}  
## 3. String:
* A string represents a sequence of characters for example "Javatpoint", "Hello world", etc. The string is the class of Java.


* One of the ways to create a string and store a value in it is shown below:

* String str = "You're the best";  
Here, the String type variable str has the value "You're the best". Click here to understand more about String in Java.


### Example:

In the following example, we are creating a string with a value. Here, we are using one of the String class methods, substring()
which prints the specified indexed part of the string.

StringExample.java

public class StringExample {  
    public static void main(String[] args) {  
          
        // creating a string and initializing it  
        String str = "Hello! This is an example of String type";  
          
        // applying substring() on above string  
        String subStr = str.substring(0,14);  
  
        // printing the string  
        System.out.println(substrate);  
    }  
}  
Output:

Hello! This is

## 4. Array:
* An array
is a data type that can store multiple homogenous variables i.e., variables of the same type in a sequence. They are stored in an indexed manner starting with index 0. The variables can be either primitive or non-primitive data types.

* The Following example shows how to declare an array of primitive data types int:

int [ ] marks;  
Following example shows how to declare an array of non-primitive data types:


Student [ ] students;   
where Student is the class name and [ ] creates an array of object students.

### Example:

In the following example, we are creating two basic arrays, in which one is initialized and the other is declared (input is read from the user). Further, we are printing those arrays using them for a loop.

ArrayExample.java

// importing required packages  
import java.io. * ;  
import java.util. * ;  
  
public class ArrayExample {  
  public static void main(String[] args) throws IOException {  
    int I;  
    Scanner sc = new Scanner(System. in );  
    // declaring and initializing an array  
    int arr[] = {1, 2, 3, 6, 9};  
    // defining another array arr1  
    int arr1[] = new int[5];  
    // reading values from the user  
    System. out.println("Enter the numbers (size = 5) :");  
    for (i = 0; i < 5; i++) {  
      arr1[i] = sc.next();  
    }  
    System.out.println("Previous array with initialized size is: ");  
    for (i = 0; i < 5; i++) {  
      System.out.print(arr[i] + " ");  
    }  
    System.out.println("\nThe new array we have entered is:");  
    for (i = 0; i < 5; i++) {  
      System.out.print(arr1[i] + " ");  
    }  
  }  
}  
### Output:

Enter the numbers (size = 5) :

56

43

22

1

7

The previous array with the initialized size is:

1 2 3 6 9

The new array we have entered is:

56 43 22 1 7

# 3. Conclusion
* Good choice of algorithm and data structure can make big differences to the efficiency of a program, and we looked at how one problem can have several alternative algorithms that can solve it, or one abstract data type to have several alternative data structures that can represent it.

* When writing code to solve some problem or represent some structure, it is best to write it in a way so that code can be reused in different circumstances. We saw how inheritance helps us write more general code, and generic typing is another Java feature that can be used to write code useable with a variety of different actual types. We also saw how to make use of code from the Java library: the object-oriented programming style and the various generalization mechanisms encourage the re-use of code that already exists rather than writing your own from the beginning.
# 4. Reference
* https://www.javatpoint.com/non-primitive-data-types-in-java

* https://www.geeksforgeeks.org/data-types-in-java/

* https://www.mygreatlearning.com/blog/data-structures-using-java/
