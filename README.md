# JAVA
This sheet convers all the basics of JAVA
Every class in the java extends Object class that makes the java 99.99% object oriented except the primitive classes ex: int, float this are premitive classes
This improves java performance since primitive types are fixed and no need to store in the heap memory that is is time consuming.
## Introduction
    IDE – Integrated Development Environment
    Always use LTS version of Java (Long Term Support)
    Java – To run the application
    Javac – To compile the application
    If I want to experiment with the code in the code line I can use jshell
    Java Playground : jshell
    
    Cmd: jshell
    Now I can write System.out.println("Hello world");
![image](https://github.com/user-attachments/assets/eb661732-47ef-4a0c-8162-630a50accb3d)
### How Java Works
    Java is independent because of JVM(Java Virtual machine).
    Independent – It can run on any platform
    We have hardware on top of that we have os on that top we have JVM. 
    JVM doesnot accept the code directly it needs bytecode
    The JVM itself is platform dependent. It doesnot work on ios os.
    To convert java code to byte code we need complier. That is Javac.
    I can have 1000 files for a project. Out of all this files only first file is executed.
    The first file needs to have main method.
    The main has a particular signature that is public static void main(String args[]).
    My code is not going to work without this signature.
    Java is object oriented everything should be in class.
    Java Code – .java
    Java Complie code - .class
    JRE(Java Runtime Environment):
    JVM + Libraries is the part of JRE
    All the running of the application takes in JRE
    JDK – Java Development Kit
    JDK contains JRE, JRE contains JVM
    JDK will have JRE, JRE will have JVM
    If my friend have JRE and JVM he can directly run my program.
    Java follows WORA (Write Once Run Anywhere)
![image](https://github.com/user-attachments/assets/feb7e5ee-31b6-4c82-9110-57e03294cadb)
### Data Types
    Variables:
    Type variablename = value;
    = is called as assignment operator.
    Data Types
    Primitive: Integer, Float, Char, boolean
    Integer – byte, short (2 bytes), int (4 bytes), long(8 bytes)
    Float – double(4 bytes)(default), float(8 bytes)
    float a = 10.0;
    It will throw a error since 10.0 is considered as double by default so we need to add f at the end.
    float a = 10.0f; //works 
    double b = 10.0; //works
![image](https://github.com/user-attachments/assets/ab3fc211-c91e-4c8c-a75b-66e9a17a49b7)
    Playing with strings
![image](https://github.com/user-attachments/assets/f17a593f-8ad3-4848-80d9-9cb5cd72d273)
### Type Conversion and casting:
    class HelloWorld {
        public static void main(String[] args) {
            int a = 256;
            byte b = 127;
            a = b; //Iam assigning byte value to integer it works
                   //This is called implict conversion
            System.out.println(a);
            int c = 10;
            byte d = 20;
            // d = c; //doesnot work because cant assign bigger value to smaller value
            d = (byte) c; //Doing typecasting it works
                          //Explict conversion
            System.out.println("d->"+d);
            float f = 5.6f;
            int g = (int) f; //5 Losing the values after deceimal
            System.out.println(g);
            //use typecast and convert a integer to byte, the max of byte is 256
            //It will use modules operation and gives the remainder now
            int j = 257;
            byte k = (byte) j;
            System.out.println(k);
        }
    }
    Type Promotion:
    byte a = 100;
    byte b = 3;
    Int c = a*b; //The max value of the byte is 256 now the 300 value that is as been assigned to int the product of byte is byte but now it is promoted.
### Difference between pre Increment and post increment
    int num = 7;
    num++;
    System.out.println(num); //8
    ++num;
    System.out.println(num); //9
    // we can see the difference only during assignment
    int result = num++; //9 since we are giving cmd first fetch the value and do post increment
    int result2 = ++num; // 10 since we are incrementing and later fetch value
    System.out.println(result);
    System.out.println(result2);
### If, else, switch, while, for, do while
    class HelloWorld {
        public static void main(String[] args) {
            int a = 10;
            //Covering if else if else statement
            if(a<5)
                System.out.println("Falls in <5");
            else if(a>5 && a<10)
                System.out.println("Falls in >5 and <10");
            else
                System.out.println("Greater than 10 or equal");
            //Terinary Operator
            String result = a%2 == 0 ? "Even" : "Odd";
            System.out.println(result);
            //Covering switch statement
            switch(a){
                case 1:
                    System.out.println("This is 1");
                    break;
                case 2:
                    System.out.println("This is 2");
                    break;
                default:
                    System.out.println("Default triggered");
            }
            //While Loop
            while(a<12){
                System.out.println("Hello");
                a++;
            }
            int b = 4;
            //Do while loop
            do{
                System.out.println("Do loop");
                b++;
            }
            while(b<10);
            //For loop
            for(int i=0; i<5; i++){
                System.out.println("For loop");
            }
        }
    }
### Unsolved Questions
    class HelloWorld {
        public static void main(String[] args) {
        int a = 3;
     
        int b = 6;
     
        int result = (~a & b) | (a & ~b);
     
        System.out.println(result);
        }
    }
    Op: 5
    Question 2:
    class HelloWorld {
        public static void main(String[] args) {
        int x = 5;
     
    int y = 10;
     
    int z = (x++ > 5 && y-- < 10) ? x-- : y;
    System.out.println(x);
    System.out.println(y);
        }
    }
    Op: 6, 10
    Question3:
    class HelloWorld {
        public static void main(String[] args) {
        int i, j;
     
    i = 100;
     
    j = 300;
     
    while(++i < --j);
     
    System.out.println(i);
        }
    }
### Class and Object
    Object - is something that have properties and has certain behaviour.
    How to create obj 
    classname reference_variable = new classname();
    
    class Calculator {
        public int add(int num1, int num2) {
            return num1 + num2;
        }
    }

    class Hello {
        public static void main(String args[]) {
            Calculator obj = new Calculator(); //Creating the Object here
            int result = obj.add(4, 5);
            System.out.println(result);
        }
    }
    To create components we use classes

### Methods
    class Computer {
        public void playmusic() {
            System.out.println("Playing Music...");
        }
        public String getComputerCount() {
            return "Computer count is 5";
        }
    }
    
    class Main {
        public static void main(String args[]){
            System.out.println("hello");
            Computer obj = new Computer();
            String computerstatement = obj.getComputerCount();
            System.out.println(computerstatement);
        }
    }
#### Method Overloading
    We have same method name and different parameters that is called method overloading, if we have same method name and same paramters but the different return type it doesnot work. Since it is only concentrated on different parameters not the return type
    different parameter meaning = the parameter length can be different or parameter type can be different
    class Computer {
        public int add(int a, int b){
            return a+b;
        }
        public int add(int a, int b, int c){
            return a+b+c;
        }
        public double add(double a, double b){
            return a+b;
        }
    }
    
    class Main {
        public static void main(String args[]){
            Computer obj = new Computer();
            int addition = obj.add(2,3,4);
            double doubleaddition = obj.add(2.5, 4.5);
            System.out.println(addition); //9
            System.out.println(doubleaddition); //7.0
        }
    }
    Example for same paramters but different return type
    class Computer {
        public int add(int a, int b){
            return a+b;
        }
        public double add(int a, int b){
            return (double)a+b;
        }
    }
    
    class Main {
        public static void main(String args[]){
            Computer obj = new Computer();
            int addition = obj.add(2,3);
            System.out.println(addition);
        }
    }
    This code is failed since add(int,int) function already exists

### Stack and Heap for the method
    Every method will have their own seperate stack and all the global variables or instance variables are stored in the heap memory, the local variables are part of the stack.
    Since we are creating object then we get the address. this object has been stored in the heap memory.
    When ever we call this obj we are refering the same obj and using.
    We can create multiple objects then in the heap we can have multiple objects.
    Creating Multiple objects below and if we change the value of one object does it change the in the other place
    class Computer {
        int num = 5;
        public void getNum(){
            System.out.println(num);
        }
    }
    
    class Main {
        public static void main(String args[]){
            int data = 10;
            Computer obj = new Computer();
            Computer obj1 = new Computer();
            obj.num = 10;
            obj.getNum(); //10
            obj1.getNum(); //5
        }
    }
    refer 28 classes for the image
## Array
### Creation of array
    import java.util.Arrays;
    
    class Main {
        public static void main(String args[]){
           //Creation of an array
           //Static array
           int staticArray[] = {1,2,3,4,5};
           //Print entire array
           System.out.println(Arrays.toString(staticArray)); //[1,2,3,4,5]
           //Change the value
           staticArray[0] = 6;
           //Best way to pring array
           for(int i=0; i<staticArray.length; i++){
               System.out.print(staticArray[i]+" ");
           }
           System.out.println();
           //Dynamic Array if i dont set the value the default will be zero
           int arr[] = new int[5];
           System.out.println(Arrays.toString(arr));
           //Dynamic 2d Arrays
           //Assign random values and printing the 2d array
           int num[][] = new int[4][5];
           for(int i=0; i<num.length; i++){
               for(int j=0; j<num[0].length;j++){
                   num[i][j] = (int)(Math.random()*100);
                   System.out.print(num[i][j]+" ");
               }
               System.out.println();
           }
           System.out.println();
           //Enhanced for Loop 
           for(int n[]: num){ //Grabs Entire array of each step
               for(int m: n){ //Grabs each element of the array
                   System.out.print(m+" ");
               }
               System.out.println();
           }
           //Lets create a jagged array meaning an array can contain different length of columns in each row 
           int jaggedArray[][] = new int[3][];
           jaggedArray[0] = new int[3];
           jaggedArray[1] = new int[4];
           jaggedArray[2] = new int[2];
           //Print the jagged array
           for(int i=0; i<jaggedArray.length; i++){
               for(int j=0; j<jaggedArray[i].length; j++){
                   System.out.print(jaggedArray[i][j]+" ");
               }
               System.out.println();
           }
           //Enhanced For loop 
           for(int a[]: jaggedArray){
               for(int n: a){
                   System.out.print(n+" ");
               }
               System.out.println();
           }
        }
    }
    An array is an object since it is created using new keyword. that is stored in the heap memory.
    Size is fixed.
    It is storing only one type of values not storing multiple type values.
    Searching is difficult.
#### Array of Objects
    import java.util.Arrays;

    class Student {
        String name;
        int marks;
        int age;
    }
    
    class Main {
        public static void main(String args[]){
            Student s1 = new Student();
            s1.name = "Koushik";
            s1.marks = 98;
            s1.age = 25;
            Student s2 = new Student();
            s2.name = "K";
            s2.marks = 95;
            s2.age = 12;
            Student s3 = new Student();
            s3.name = "G";
            s3.marks = 92;
            s3.age = 15;
            //Array of objects
            Student students[] = new Student[3];
            students[0] = s1;
            students[1] = s2;
            students[2] = s3;
            for(int i=0; i<students.length; i++){
                System.out.println(students[i].name);
            }
        }
    }
### Strings
    String is a class in the java, since it is a class i need to create a obj so that i can use.
    String name = new String("Koushik");
    String name = "koushik"; //Even this works the java automatically creates a object for you.
    since it is a class we can have multiple methods.
    name.concat(" gampa");
    System.out.println(name); //Koushik Gampa
    String is immutable every time we update a string it creates new string, the older is not removed it stays in the special area of the heap memory that is called as String Constant pool.
    Since we reuses the strings multiple times.
    Example
    String name="koushik";
    String name2="koushik";
    System.out.println(name==name1); //True here comparing the address of the strings it is true
    
    first in the string constant pool it will create koushik, if koushik is there it dont create a new string instead it will give the address;
    String s1 = "raja";
    s1 = s1 + "run";
    in the string constant pool it will create the raja, it will creat one more variable raja run. since raja is no longer required it removed by java garbage collector to save some space.
    For photo refer 37 lecture

### Mutable String(String Buffer and String Builder)
    class Main {
        public static void main(String args[]){
            StringBuffer s1 = new StringBuffer("Koushik");
            s1.append(" Gampa");
            s1.insert(0, "Java ");
            System.out.println(s1);
        }
    }
    StringBuffer and StringBuilder have almost same methods but the only difference is StringBuffer is thread safe where as StringBuilder is not thread safe.
### Static
#### Static Variable
    Static variable is shared by different objects. Consider it has a common variable if we change in one place it effects all the areas.
    static variables are shared between different objects.
    static makes the varable class member not object member.
    class Mobile {
        String brand;
        int price;
        static String name;
        
        public void printDetails(){
            System.out.println(brand + " " + price+ " "+ name);
        }
    }

    class Main {
        public static void main(String args[]){
            Mobile obj = new Mobile();
            obj.brand = "Nokia";
            obj.price = 20000;
            obj.name = "Smart Phone";
            
            Mobile obj2 = new Mobile();
            obj2.brand = "iphone";
            obj2.price = 50000;
            obj2.name = "Iphone";
            System.out.println(obj2.name); //Iphone
            System.out.println(obj.name); //Iphone 
            //since the variable is static it acts as a common class even if the value of the name is modified using obj2 it effects obj1
            //we can modify static variable using objects and class as well. The recommended way is class modification
            Mobile.name = "Smart Phone";
            System.out.println(obj.name); //Smart Phone
            System.out.println(obj2.name); //Smart Phone
        }
    }
#### Static Method
    class Mobile {
        String brand;
        int price;
        static String name;
        
        public void printDetails(){
            System.out.println(brand + " " + price+ " "+ name);
        }
        public static void show(){
            //System.out.println(brand + " " + price + " " + name); //we can directly use the name here but we cannot use brand and price
            //we can use static varibale inside the static method directly but we cant use non static variable
            // Reason since static variable is common varible for the all the objects we can use.
            //But brand, price differs for individual objects but we can indirectly use it as below see show1 method.
        }
        public static void show1(Mobile obj){
            System.out.println(obj.brand + " " + obj.price+ " "+ name); //we are using it indirectly
        }
    }

    class Main {
        public static void main(String args[]){
            Mobile obj = new Mobile();
            obj.brand = "Nokia";
            obj.price = 20000;
            obj.name = "Smart Phone";
            
            Mobile obj2 = new Mobile();
            obj2.brand = "iphone";
            obj2.price = 50000;
            obj2.name = "Iphone";
            
            Mobile.show();
            Mobile.show1(obj);
            Mobile.show1(obj2);
        }
    }
    Q) why do we use static in public static void main()?
    If the excution is not started how can we create a object.
    if i remove static in the pulic static void main()
    if i want to call the main i need to use Main obj = new Main(); obj.main();
    if excution is not started we cant create obj. if excution is started only then we can create obj.This is deadlock event if we want to solve this issue we use static if we use this then there is no need of creating object.
    we can directly call the method directly using Main.main();
### Static block
    Static block is used to initialize static variables
    class Mobile {
        String brand;
        int price;
        static String name;
        static {
            name = "Smart Phone"; //initialize the static varible it wont get called every time the object has been created.
            System.out.println("Static Method called!");
        }
        Mobile() {
            brand = ""; //Giving default value in the constructor
            price = 0;
            System.out.println("Constructor called!");
        }
    }
    
    class Main {
        public static void main(String args[]) throws ClassNotFoundException{
            Mobile obj = new Mobile();
            obj.brand = "samsung";
            obj.price = 20000;
            Mobile obj2 = new Mobile();
            obj2.brand = "Realme";
            obj2.price = 10000;
            
            //Op: Static Method called!, Constructor called! , Constructor called!
            //every time a obj gets created it follows two steps 1. Class loads and 2.objects get intialized. the class loads only once.
            //every time class loads it has been stored in a special area of jvm called as ClassLoader
            // If no object then class is not loaded
            //To load the class without creating object we can use 
            Class.forName("Mobile");
        }
    }

### Encapsulation
    wrapping of data and code together
    other words Encapsulating code and methods together
    class Human {
        String name = "koushik";
        private String location = "Sai Nagar, Jammikunta";
        
        public String getLocation() {
            return location;
        }
        
    }
    
    class Main {
        public static void main(String args[]) {
            Human obj = new Human();
            System.out.println(obj.name); //koushik
            // System.out.println(obj.location); //Error Location has private access in the Human class
            String location = obj.getLocation(); //Sai Nage, jammikunta the private varibles are only accessable using the class own methods
            System.out.println(location);
        }
    }

    Q) what if the varible is not intialized ?
    we have to create methods to set and get the values to data.
    class Human {
        String name;
        private String location;
        
        public String getLocation() {
            return location;
        }
        
        public void setLocation(String m) {
            location = m;
        }
    }
    
    class Main {
        public static void main(String args[]) {
            Human obj = new Human();
            obj.setLocation("Sai Nagar");
            String location = obj.getLocation();
            System.out.println(location);
        }
    }

## This keyword in Java
    This is keyword that represents the current object
    class Human {
        private int age;
        
        public int getAge(){
            return age;
        }
        // public void setAge(int a){
        //     age = a;
        // }
        //What if i want to use the parameter name as age
        // public void setAge(int age){
        //     age = age; //0 if two variables have same name the priority is given to local variable but we need to instance variable so that in the get method we get value
        // }
        //To solve this issue we have to pass obj to differentiate
        
        // public void setAge(int age, Human obj){
        //     obj.age = age; //30 but here we are passing obj again that is not good instead java gives this keyword that has current object in it.
        // }
        
        public void setAge(int age){
            this.age = age; //Now we can see the difference this.age is instance varibale and age is local variable
        }
    }
    
    class Main {
        public static void main(String args[]) {
            Human obj = new Human();
            obj.setAge(10, obj);
            System.out.println(obj.getAge());
        }
    }

## Casing
    //Camel Casing
    class and interface - capital, Calc
    variables and methods - small letters
    Constants - full caps PIE

    showMyMarks() - method
    CalcManager - class
    CalcManager() - constructor

### Anonomous object
    Creating Object without the reference variable is called anonomous object.
    Student students = new Student();
    students is a reference to the object where as new Student() is the actual object.
    Code:
    class Student {
        int age;
        public Student(int age) {
            this.age = age;
            System.out.println("Object created!");
        }
        public void show(){
            System.out.println(this.age);
        }
    }
    
    public class Main
    {
    	public static void main(String[] args) {
    	    new Student(10).show(); //Here object is created without reference variable we cannot reuse this obj since we doesnot have reference variable. We can only once this kind of objects.
    	    new Student(20).show();
    	}
    }
    
### Inheritance
    parent - child
    base - dervied
    super - subclass
    Multi level inheritance works
    Multiple inheritance doesnot work, since ambigous problem
    class Calc {
        public int add(int a, int b){
            return a+b;
        }
        public int sub(int a, int b){
            return a-b;
        }
    }
    
    class AdvCalc extends Calc {
        public int multiple(int a, int b){
            return a*b;
        }
        public int division(int a, int b){
            return a/b;
        }
    }
    
    class VeryAdvanceCalc extends AdvCalc {
        public int module(int a, int b){
            return a%b;
        }
    }
    
    public class Main
    {
    	public static void main(String[] args) {
    	    VeryAdvanceCalc obj = new VeryAdvanceCalc();
    	    int r1 = obj.add(4,5);
    	    int r2 = obj.sub(9,3);
    	    int r3 = obj.multiple(4,5);
    	    int r4 = obj.module(4,5);
    	    System.out.println(r1+ " " + r2+" "+ r3+" "+r4);
    	}
    }
#### Super and this in inheritance
    super() - is used to call the constructor of the parent class constructor even if we dont metion it will be there by default
    this() - is used to call the constructors of the same class
    class A {
        public A() {
            System.out.println("This is A");
        }
        public A(int a){
            System.out.println("This is parameterized constructor A");
        }
    }
    class B extends A {
        public B() {
            super(4);
            System.out.println("This is B");
        }
        public B(int a){
            super(5); //call super to pass the consturctor value
            System.out.println("This is parameterized constructor B");
        }
        public B(int a, int b){
            this(); //this is as same as super() but we can call constructors of the same class
            System.out.println("This is 2 parameterized constructor");
        }
    }
    
    public class Main
    {
    	public static void main(String[] args) {
    	    B obj = new B();
    	    B obj2 = new B(5); // My requirement is to have parameterized constructor for both class A and class B
    	    B obj3 = new B(5,6); //My requirement call the unparameterized constructor and parameterized constructor of A
    	}
    }
    
    // output we get as 
    // This is A 
    // This is B 
    // since in the constructor B there is a hidden default method super(); that calls the A constructor automatically
### Overriding 
    Code:
    class A {
       public void show() {
           System.out.println("This is A shows");
       }
    }
    class B extends A {
        public void show() {
            System.out.println("This is B show");
        }
        
    }
    
    public class Main
    {
    	public static void main(String[] args) {
    	    A obj = new A();
    	    obj.show();
    	    B obj2 = new B();
    	    obj2.show();
    	}
    }
    Best Example for Method overloading and 
    Code:
    class A {
       public void show() {
           System.out.println("This is A shows");
       }
       public void show(double time) { //Method overloading
           System.out.println("Today:"+time);
       }
    }
    class B extends A {
        public void show() { //Method overriding
            System.out.println("This is B show");
        }
        
    }
    
    public class Main
    {
    	public static void main(String[] args) {
    	    A obj = new A();
    	    obj.show();
    	    B obj2 = new B();
    	    obj2.show();
    	    obj2.show(6.30);
    	}
    }
### Packages
    Pending
### Access Modifiers

### Dynamic Method Dispatch
    Creating object of child and assign the value to the parent class type is called the dynamic method dispatch.
    class A {
      public void show(){
          System.out.println("This is A show");
      }
    }
    class B extends A {
        public void show(){
            System.out.println("This is B show");
        }
    }
    class C extends A {
        public void show(){
            System.out.println("This is C show");
        }
    }
    class D {
        
    }
    
    public class Main
    {
    	public static void main(String[] args) {
    	    A obj = new A();
    	    obj.show();
    	    obj = new B(); //Since B is inheriting A object we can create obj B object that can be assigned to A type reference variable
    	    obj.show();
    	    obj = new C();
    	    obj.show();
    	    //obj = new D(); //It will be incompactable type since D is not inheriting the A 
    	    
    	    A obj1 = new B(); //The reference variable type A but the object that we have created is B object
    	    obj1.show();
    	}
    }
### Final
    Method:
        int a = 10;
	    a = 20;
	    System.out.println(a); //Normally we can directly update the value of a if i want to make it non changeable i need to use final
	    final int b = 10;
	    b = 20; //Will get error b cant be changed since it is a constant
     Class:
         final class Calc {
            public void show(){
                System.out.println("In the Calc application");
            }
            public int add(int a, int b) {
                return a+b;
            }
        }
        
        // class AdvanceCalc extends Calc {
            
        // } // will get the error since final class cannot be extended stops inheritance
        
        public class Main
        {
        	public static void main(String[] args) {
        	    Calc obj = new Calc();
        	    System.out.println(obj.add(2,3));
        	    obj.show();
        	}
        }
    Method:
        //Suppose i have a class and i have methods such as author name and add feature. i dont want any one to replace the author name but they can use my add feature.
        class Calc {
            public final void showAuthor(){
                System.out.println("The Author is koushik");
            }
            public int add(int a, int b) {
                return a+b;
            }
        }
        
        class AdvanceCalc extends Calc{
            // public void showAuthor(){
            //     System.out.println("The Author is KRK");
            // } //i will get error since i cant override the final method
        }
        
        public class Main
        {
        	public static void main(String[] args) {
        	    AdvanceCalc obj = new AdvanceCalc();
        	    obj.showAuthor();
        	    System.out.println(obj.add(2,3));
        	}
        }
### Wrapper Class
	Primitive type have Object classes of there own int is primitive where Integer is a Object that extends Object Class.
	AutoBoxing - When we store a primitive type in the object automatically
 	Autounboxing - when we take out the primitive value from the object
  	int num = 8;
   	Integer num1 = num; //Auto Boxing
	int num2 = num1; //Auto Unboxing
	String str = "12";
	int num = Integer.parseInt(str);
	System.out.println(num);
## Simple Quiz game application 
	Main.java 	
		public class Main {
		    public static void main(String args[]) {
		        QuestionService service = new QuestionService();
		        service.displayService();
		        int score = service.getScore();
		        System.out.println(score);
		    }
		}
  QuestionService.java
		import java.util.Scanner;
		public class QuestionService {
		    Question[] question = new Question[5];
		    Scanner sc = new Scanner(System.in);
		    String[] answers = new String[5];
		
		    QuestionService() {
		        question[0] = new Question(1, "Tyres of Car", "4", "2", "1", "0", "4");
		        question[1] = new Question(2, "Tyres of bike", "4", "2", "1", "0", "2");
		        question[2] = new Question(3, "Tyres of lorry", "14", "16", "2", "0", "16");
		        question[3] = new Question(4, "Tyres of boat", "4", "2", "1", "0", "0");
		        question[4] = new Question(5, "Tyres of human", "4", "2", "1", "0", "0");
		    }
		
		    public void displayService() {
		        int index = 0;
		        for (Question indQues : question) {
		            System.out.println(indQues.toString());
		            System.out.print("Enter the answer:");
		            answers[index] = sc.nextLine();
		            index++;
		        }
		        System.out.println(answers);
		    }
		
		    public int getScore() {
		        int score = 0;
		        for (int i = 0; i < question.length; i++) {
		            String actualAnswer = question[i].getAnswer();
		            String enteredAnswer = answers[i];
		            if (actualAnswer.equals(enteredAnswer)) {
		                score++;
		            }
		        }
		        return score;
		    }
		}
	Question.java
	 	public class Question {
	    private int id;
	    private String question;
	    private String option1;
	    private String option2;
	    private String option3;
	    private String option4;
	    private String answer;
	
	    Question(int id, String question, String option1, String option2, String option3, String option4, String answer) {
	        this.id = id;
	        this.question = question;
	        this.option1 = option1;
	        this.option2 = option2;
	        this.option3 = option3;
	        this.option4 = option4;
	        this.answer = answer;
	    }
	
	    public int getId() {
	        return this.id;
	    }
	
	    public void setId(int id) {
	        this.id = id;
	    }
	
	    public String getQuestion() {
	        return this.question;
	    }
	
	    public void setQuestion(String question) {
	        this.question = question;
	    }
	
	    public String getAnswer() {
	        return this.answer;
	    }
	
	    public void setAnswer(String answer) {
	        this.answer = answer;
	    }
	
	    @Override
	    public String toString() {
	        return "Question [id=" + id + ", question=" + question + ", option1=" + option1 + ", option2=" + option2
	                + ", option3=" + option3 + ", option4=" + option4 + "]";
	    }
	
	}
### Abstarct Keyword
	// A Abstract method is a method that is defined in the class but it is not implemented. the class that inherites the abstract class must implement abstract method
	// A Abstract can only be implemented inside a abstract class
	// Cannot create a obj of the abstract car.but we can take the instance of it
 	// It is not mandatory to have abstract methods inside abstarct class. we can even have normal methods as well.
  	// The abstarct method can have both abstract and non abstarct methods.(multiple abstract methods is possible).
   	// The class that implements abstract class is the concrete class.
	
	abstract class Car {
	    public abstract void drive(); //Here we defining a method but we are not implementing
	    public void playMusic() { //Normal Method
	        System.out.println("Playing Music ...");
	    }
	}
	
	class WagonR extends Car { //Concrete Class
	    public void drive(){
	        System.out.println("Iam Driving WagonR");
	    }
	}
	
	public class Main
	{
		public static void main(String[] args) {
	// 		Car obj = new Car(); //Not possible
	        Car obj = new WagonR(); //Possible
	        WagonR obj2 = new WagonR();
	        obj.drive();
	        obj.playMusic();
		}
	}
	//Example of implementing multiple abstract classes
	
	abstract class Car {
	    public abstract void drive();
	    public abstract void fly();
	    public void playMusic() { 
	        System.out.println("Playing Music ...");
	    }
	}
	
	abstract class WagonR extends Car {
	    public void drive(){
	        System.out.println("Iam Driving WagonR");
	    }
	}
	
	class UpdatedWagonR extends WagonR {
	    public void fly() {
	        System.out.println("The car is flying");
	    }
	}
	
	
	public class Main
	{
		public static void main(String[] args) {
	        // Car obj = new WagonR(); // Not Possible since abstract
	        Car obj = new UpdatedWagonR();
	        obj.drive();
	        obj.fly();
	        obj.playMusic();
		}
	}
### Inner Class
	class A {
	    int age;
	    public void show() {
	        System.out.println("This is inside the show");
	        // B obj = new B(); //we can call like this 
	        // obj.config();
	    }
	    class B {
	        public void config() {
	            System.out.println("This is from config");
	        }
	    }
	}
	
	
	public class Main
	{
		public static void main(String[] args) {
	        A obj = new A();
	        obj.show();
	        A.B obj1 = obj.new B();
	        // Object Location need to mention object name = the outer class object instance to create new object of B. jus like we obj.show() we use obj.new
	        obj1.config();
		}
	}

 	// Making Static B
	  class A {
	    int age;
	    public void show() {
	        System.out.println("This is inside the show");
	    }
	    static class B { // Now this is static class
	        public void config() {
	            System.out.println("This is from config");
	        }
	    }
	}
	
	
	public class Main
	{
		public static void main(String[] args) {
	        A obj = new A();
	        obj.show();
	        A.B obj1 = new A.B(); // This will only work when i make B class has static
	        obj1.config();
		}
	}
### Anonyomous Inner class
	Anonyomous Means class that doesnot have name.
	// class A {
	//     public void show() {
	//         System.out.println("This is A show");
	//     }
	// }
	
	// public class Main
	// {
	// 	public static void main(String[] args) {
	//         A obj = new A();
	//         obj.show();
	// 	}
	// }
	
	//I have this code how to give new behaviour to the show method
	// Option1: create a new class B use method overriding and add new behaviour but the only purpose of the B class is the to override A method
	// The best way is to use anonymous fucntion
	
	class A {
	    public void show() {
	        System.out.println("This is A show");
	    }
	}
	
	
	public class Main
	{
		public static void main(String[] args) {
	        A obj = new A() 
	        { //We have created a class without any name
	            public void show() {
	                System.out.println("This is new Show");
	            }
	        };
	        obj.show();
		}
	}
#### Abstract for anonyomous class
	abstract class A {
	    public void show() {
	        System.out.println("This is A show");
	    }
	}
	
	
	public class Main
	{
		public static void main(String[] args) {
	        A obj = new A() //Here this code will work since we are not creating object of the abstract class. but we are creating object of anonmyous class
	        {
	            public void show() {
	                System.out.println("This is new Show");
	            }
	        };
	        obj.show();
		}
	}
## Interface
	What is the need of interface?
 		To make the code loosly coupled.
	// Interface is type of class where all the methods inside the class are public abstract methods by default even if we dont define
	// Instead of extends we are using implements
	// By default in interface variables are static and final by default
 	// Since we cannot create objects based on interface then we cannot be able to modify the variables
  	// Interface doesnot occupy the heap memory.
   	// The concrete class can implement multiple interfaces where in abstract we can extend only one class.
	// Inheritance is possible in the interface
 	// class - class extends
  	// class - interface implements
   	// interface - interface extends
	
	interface A {
	    int age = 23;
	    String area = "Mumbai";
	    
	    void show();
	    void config();
	}
	interface X {
	   void fly(); 
	}
	interface Y extends X {
	    
	}
	class B implements A,Y { // Y doenot hace fly but got it because inheritance
	    public void show() {
	        System.out.println("Show implemented");
	    }
	    public void config() {
	        System.out.println("Configuration Implemented");
	    }
	    public void fly() {
	        System.out.println("Flying is happening");
	    }
	}
	
	
	public class Main
	{
		public static void main(String[] args) {
	        A obj = new B();
	        obj.show();
	        obj.config();
	        System.out.println(A.area);
	        // A.area = "Hyderabad"; // Not possible since the area is final we cannot change
	        // A.fly(); // A has no idea about the fly method so change the instance to get full data
	        B obj1 = new B();
	        obj1.fly();
		}
	}

  Actual Example of Interface:
  	// We use interfaces to make code loosly coupled
		interface Computer {
		    void show();
		}
		
		class Laptop implements Computer {
		    public void show() {
		        System.out.println("This is laptop, codes that are faster");
		    }
		}
		
		class Desktop implements Computer {
		    public void show() {
		        System.out.println("This is computer, codes better than laptop");
		    }
		}
		
		class Employee {
		    public void showSystem(Computer obj) { // Here we are using Computer class instance that makes more generic we can use laptop or computer classes instances
		        obj.show();
		    }
		}
		
		public class Main
		{
			public static void main(String[] args) {
			    Employee emp = new Employee();
			    Computer desk = new Desktop();
			    Computer lap = new Laptop();
			    emp.showSystem(desk);
			}
		}
### Enum Statements 
  	Enum is a class, can create constructor, it extends object class
  	enum Status {
	    Success, Pending, Failure, Processing;
	}
	
	public class Main
	{
		public static void main(String[] args) {
			Status status = Status.Success;
			System.out.println(status);
			Status[] arr = Status.values();
			System.out.println(arr[0]);
			// If else for enum
			if(status == Status.Success) {
			    System.out.println("In the success stage");
			}
			else if(status == Status.Failure) {
			    System.out.println("In the failure stage");
			}
			else {
			    System.out.println("In the processing or pending");
			}
			// Switch statements for enum 
			switch(status) {
			    case Success:
			        System.out.println("In the success phase");
			        break;
			    case Failure:
			        System.out.println("In the failure phase");
			        break;
			    default:
			        System.out.println("In the processing or pending phase");
			}
		}
	}

#### Enum Class
	enum Laptop {
	    Mackbook(4000), Msi(50000), Dell(1000), Hp(500); //need to pass the price so we need a constructor
	    
	    private int price;
	    
	    Laptop(int price){
	        this.price = price;
	    }
	    
	    public void getPrice(){
	        System.out.println(this.price);
	    }
	}
	
	public class Main
	{
		public static void main(String[] args) {
		    Laptop dell = Laptop.Dell;
		    dell.getPrice();
		}
	}
### Annotations
	A supplement to the compiler
 	It is also called as meta data.Some time i want to intract with the compiler. This doesnot change the behaviour of the code but that reduces the bugs.
	Annotations are the inbuilt statements that we can give some context to compiler about the action that we are doing.
 	It reduces the bugs since we can see the error during compile time itself.
  	class A {
	    public void shows() {
	        System.out.println("This is A show");
	    }
	}
	
	class B extends A {
	    public void show() {
	        System.out.println("This is B class");
	    }
	}
	
	public class Main
	{
		public static void main(String[] args) {
		    B obj = new B();
		    obj.shows();
		}
	}
### Types of Interfaces
	Normal Interface - 2 or 3 methods inside interface are called normal interface
 	Functional Interface / SAM(single abstract method) - interface with only one method
  	Marker Interface - with no methods
   	we can implement lambda functions using functional interface only
### Lambda Functions
	//Normal Invitation
	interface A {
	    void show();
	}
	
	public class Main
	{
		public static void main(String[] args) {
		    A obj = new A(){
		        public void show() {
		            System.out.println("This is the implemented system");
		        }
		    };
		    obj.show();
		    
		}
	}
 	Code after lambda functions
  		interface A {
		    void show(int i);
		}
		
		public class Main
		{
			public static void main(String[] args) {
			    A obj = (i) -> {
			        System.out.println("Hello"+i);
			    };
			    obj.show(5);
			    
			}
		}
	Return Value for lambda functions
 		interface A {
		    int add(int i, int j);
		}
		
		public class Main
		{
			public static void main(String[] args) {
			    A obj = (i,j) -> {
			        return i+j;
			    };
			    System.out.println(obj.add(5,6));
			}
		}

### Exception
	// Multiple try catch exceptions
 	// Always we need to place the critical statments in the try catch
	public class Main
	{
		public static void main(String[] args) {
		    int a = 0;
		    int b = 0;
		    int[] arr = new int[4];
		    try {
		        int c = a/b;
		        int d = arr[4];
		    }
		    catch(ArithmeticException e){
		        System.out.println("Exception statement : "+e);
		    }
		    catch(ArrayIndexOutOfBoundsException e){
		        System.out.println("Another Exception Statement: "+ e);
		    }
		    catch(Exception e){
		        System.out.println("Exception Statement: "+ e);
		    }
		    
		    System.out.println("End statement");
		}
	}
	// Throw exception and throw a message
 	class Main {
	    public static void main(String[] args) {
	        int a = 10;
	        int b = 0;
	        try {
	           if(b==0) {
	            throw new Exception("Problem with denominator");
	            }
	            int c = a/b;
	            System.out.println(c);
	        }
	        catch(Exception e) {
	            System.out.println(e); //java.lang.Exception: Problem with denominator
	        }
	    }
	}
 	// Custom Exception
	  	class CustomException extends Exception{
	    public CustomException(String msg){
	        // System.out.println("Zero Denominator Error:" + msg);
	        super(msg);
	    }
	}
	
	class Main {
	    public static void main(String[] args) {
	        int a = 10;
	        int b = 0;
	        try {
	           if(b==0) {
	            throw new CustomException("Problem with denominator");
	            }
	            int c = a/b;
	            System.out.println(c);
	        }
	        catch(Exception e) {
	            System.out.println(e); //
	        }
		 	Sytem.out.println("Running");
	    }
	}
 
 	// Duking the Exception
  	Normal way of handling Exception
   	class Calculator {
	    public void divide(int a, int b) {
	        try{
	            int c = a/b;
	            System.out.println(c); 
	        }
	        catch(ArithmeticException e){
	            System.out.println(e);
	        }
	    }
	}
	
	class Main {
	    public static void main(String[] args) {
	       Calculator obj = new Calculator();
	       obj.divide(10,5); //2
	       obj.divide(10,0); //java.lang.ArithmeticException: / by zero
	    }
	}

 	// if i have multiple class or methods that have divide function everything has the same kind of exception instead of handling excetpion inside the subclass we can handle the exception in another class
  	// Throws keyword tells that this particular class will throw a this kind of exception but it is not handled in the present class the class that implements this class will handle the exception
   	// In the below example the exception handling is implemented in the parent class rather than subclass
	    class Calculator {
	        public void divide(int a, int b) throws ArithmeticException {
	            int c = a/b;
	            System.out.println(c);
	        }
	    }
	    
	    class Main {
	        public static void main(String[] args) {
	           Calculator obj = new Calculator();
	           try {
	               obj.divide(10,5); //2
	               obj.divide(10,0);
	           }
	           catch(ArithmeticException e){
	               System.out.println(e);
	           }
	        }
	    }

## Reading Inputs from user
	// How System.out.println works ?
 		println is the method of PrintStream Class. That we need to create a object for PrintStream to use println. Not to worry because the object is already created as static out inside System class.
   	// Since System.out does it have System.in ?
		Yes java has System.in that reads one letter at a time and when we print it gives the ascii value.
  	Code:
	   	import java.io.*;
	
		class Main {
		    public static void main(String[] args) throws IOException{
		        int num = System.in.read();
		        System.out.println(num);
		    }
		}
   
	// BufferedReader
 	import java.io.*;

	class Main {
	    public static void main(String[] args) throws IOException{
	        
	        InputStreamReader in = new InputStreamReader(System.in);
	        BufferedReader bf = new BufferedReader(in);
	        int num = Integer.parseInt(bf.readLine());
	        System.out.println(num);
	        bf.close();
	    }
	}

  	Buffered Reader needs InputStreamReader object has a argument where as InputStreamReader needs InputStream as a Argument here System.in is the InputStream.
    and the readLine throws an Exception that can be handled using try/catch or use throws and make parent to handle it.(here parent is jvm since it is main it dangeours to use)
	Since BufferedReader is a resource after use of resource close the resource.
 	
	// Scanner Class
 	import java.util.Scanner;
	
	class Main {
	    public static void main(String[] args) {
	        Scanner sc = new Scanner(System.in);
	        int a = sc.nextInt();
	        System.out.println(a);
	    }
	}

	We need to mention System.in since we need to specify from we are getting input is it from System or console

## Threading in Java
	class A extends Thread{
	    public void run() {
	        for(int i=0;i<100;i++){
	            System.out.println("Hi");
	            try{
	                Thread.sleep(1000);
	            } catch(InterruptedException e) { System.out.println(e); }
	        }
	    }
	}
	
	class B extends Thread{
	    public void run() {
	        for(int i=0;i<100;i++){
	            System.out.println("Hello");
	            try{
	                Thread.sleep(1000);
	            } catch(InterruptedException e) { System.out.println(e); }
	        }
	    }
	}
	
	class Main {
	    public static void main(String[] args) {
	        A hiObj = new A();
	        B helloObj = new B();
	        hiObj.start();
	        helloObj.start();
	    }
	}
### Threading Using Runnable in Java
	Code:
 		class A implements Runnable {
            public void run(){
                for(int i=0;i<10;i++){
                    System.out.println("Display");
                    try{
                        Thread.sleep(1000);
                    }
                    catch(InterruptedException e){
                        System.out.println(e);
                    }
                }
            }
        }
        class B implements Runnable {
            public void run() {
                for(int i=0;i<10;i++){
                    System.out.println("B Class");
                    try{
                        Thread.sleep(1000);
                    }
                    catch(Exception e){
                        System.out.println(e);
                    }
                }
            }
        }
        class Main {
            public static void main(String[] args) {
                Runnable A = new A();
                Runnable B = new B();
                Thread t1 = new Thread(A);
                Thread t2 = new Thread(B);
                t1.start();
                t2.start();
            }
        }
### Race Condition
	Code:
		 class Counter {
		    int count;
		    public synchronized void increment() { //We have to synchorized that makes one thread to work at a time.
		        count++;
		    }
		}
		
		
		class Main {
		    public static void main(String[] args) throws Exception {
		        Counter c = new Counter();
		        Runnable A = () -> {
		                for(int i=0;i<1000;i++){
		                    c.increment();
		                }
		        };
		        Runnable B = () -> {
		                for(int i=0;i<1000;i++){
		                    c.increment();
		                }
		        };
		        Thread t1 = new Thread(A);
		        Thread t2 = new Thread(B);
		        t1.start();
		        t2.start();
		        t1.join(); // We use this method to get the output from other thread
		        t2.join(); // t1=1 then t2 = t1+1 = 2 and so on
		        System.out.println(c.count); // we are getting random answer but expected is 2000
		    }
		}
# Collection
### ArrayList
	To add values to array dynamic we use arraylist
 	Code:
  		import java.util.ArrayList;
		import java.util.List;
		
		class Main {
		    public static void main(String[] args) {
		        List<Integer> nums = new ArrayList<Integer>();
		        nums.add(10);
		        nums.add(20);
		        System.out.println(nums);
		        System.out.println(nums.get(0));
		        System.out.println(nums.indexOf(20));
		        nums.set(0,5);
		        System.out.println(nums);
		        // Iteration
		        for(int i: nums){
		            System.out.println(i);
		        }
		    }
		}
		Arraylist can be of type collection as well but we use List since List has many methods. Just to insert values Collection can be usefull but if i want to work with indexes i need to List
  		Collection<Integer> nums = new ArrayList<Integer>();
		List extends Collection but the class that implements List is ArrayList
### Set
 	Set extends Collection the class that implements Set is Hashset
  	Set Doesnot gives values in the sorted order and doesnot have indexing operations
  	Code:
		import java.util.HashSet;
		import java.util.Set;
		import java.util.Iterator;
		
		class Main {
		    public static void main(String[] args) {
		        Set<Integer> nums = new HashSet<Integer>();
		        nums.add(10);
		        nums.add(20);
		        nums.add(20);
		        System.out.println(nums);
		        for(int i:nums){
		            System.out.println(i);
		        }
		        System.out.println("Iterator Starts Here");
		        // Instead of This for loop i can use Iterator
		        Iterator<Integer> values= nums.iterator();
		        // .next() method gives one value at once
		        while(values.hasNext())
		            System.out.println(values.next());
		    }
		}
### Map
	Map extends collection and HashMap implements Map
 	Difference between hashmap and hashtable is hashtable is syncronized when we working with threads it is always better to work with hashtable
 	Code:
  	import java.util.Map;
	import java.util.HashMap;
	
	class Main {
	    public static void main(String[] args) {
	        Map<String,Integer> students = new HashMap<String,Integer>();
	        students.put("a", 10);
	        students.put("b", 20);
	        students.put("c", 10);
	        students.put("a", 15);
	        System.out.println(students); // Print everyting
	        System.out.println(students.keySet());
	        
	        for(String key: students.keySet()){
	            System.out.println(key+":"+students.get(key));
	        }
	    }
	}

 	Hashtable syntax:
  		Map<String, Integer> students = new Hashtable<String, Integer>();

### Comparator
	Code:
 		import java.util.Collections;
		import java.util.ArrayList;
		import java.util.List;
		import java.util.Comparator;
		
		class Main {
		    public static void main(String[] args) {
		       List<Integer> nums = new ArrayList<>();
		       nums.add(10);
		       nums.add(5);
		       nums.add(20);
		       
		       Collections.sort(nums); // Default Sort
		       System.out.println("default sort"+nums);
		       
		       // Custom Sort, sort based on last element
		       Comparator<Integer> comp = new Comparator<Integer>(){
		           public int compare(Integer i, Integer j){
		               if(i%10 > j%10){
		                   return 1;
		               }
		               else{
		                   return -1;
		               }
		           }
		       };
		       Collections.sort(nums, comp);
		       System.out.println("sort based on last digit" + nums);
		       
		    }
		}
#### Comparator for the Student type
	Code:
 		import java.util.List;
		import java.util.ArrayList;
		import java.util.Comparator;
		import java.util.Collections;
		
		class Student {
		    String name;
		    int age;
		    public Student(String name, int age) {
		        this.name = name;
		        this.age = age;
		    }
		    public String toString(){
		        return name + ",age:"+age;
		    }
		}
		class Main {
		    public static void main(String[] args) {
		        List<Student> students = new ArrayList<Student>();
		        students.add(new Student("a", 23));
		        students.add(new Student("b", 21));
		        students.add(new Student("c", 24));
		        
		        Comparator<Student> comp = new Comparator<Student>(){
		            public int compare(Student a, Student b){
		                if(a.age > b.age){
		                    return 1;
		                }
		                else{
		                    return -1;
		                }
		            }
		        };
		        Collections.sort(students, comp);
		        System.out.println(students);
		    }
		}
  Code Reduction using functionalComponents and teranary operator
  Code:
  	import java.util.List;
	import java.util.ArrayList;
	import java.util.Comparator;
	import java.util.Collections;
	
	class Student {
	    String name;
	    int age;
	    public Student(String name, int age) {
	        this.name = name;
	        this.age = age;
	    }
	    public String toString(){
	        return name + ",age:"+age;
	    }
	}
	class Main {
	    public static void main(String[] args) {
	        List<Student> students = new ArrayList<Student>();
	        students.add(new Student("a", 23));
	        students.add(new Student("b", 21));
	        students.add(new Student("c", 24));
	        
	        Comparator<Student> comp = (a,b) -> {
	                return a.age > b.age ? 1 : -1;
	        };
	        Collections.sort(students, comp);
	        System.out.println(students);
	    }
	}
### Using Comparable instead of comparator
	Code:
 		import java.util.List;
		import java.util.ArrayList;
		import java.util.Collections;
		
		class Student implements Comparable<Student> {
		    String name;
		    int age;
		    public Student(String name, int age) {
		        this.name = name;
		        this.age = age;
		    }
		    public String toString(){
		        return name + ",age:"+age;
		    }
		    public int compareTo(Student that){
		        return this.age > that.age ? 1 : -1;
		    }
		}
		class Main {
		    public static void main(String[] args) {
		        List<Student> students = new ArrayList<Student>();
		        students.add(new Student("a", 23));
		        students.add(new Student("b", 21));
		        students.add(new Student("c", 24));
		        
		        Collections.sort(students);
		        
		        System.out.println(students);
		    }
		}
  
### ForEach
	Code:
		import java.util.List;
		import java.util.function.Consumer;
		import java.util.Arrays;
		
		public class Main {
		    public static void main(String args[]) {
		        List<Integer> nums = Arrays.asList(4, 5, 6, 7);
		        Consumer<Integer> con = new Consumer<Integer>() {
		            public void accept(Integer n) {
		                System.out.println(n);
		            }
		        };
		        nums.forEach(con); // This is the behind the scene
		        nums.forEach((n) -> System.out.println(n)); // In most of the cases we use this
		    }
		}
### Stream
	Stream is gives methods such as filter, map methods to it.
 	If we use the stream the actual data is not mutated.
  	Stream allows us to perform only one operation on the data.
   	import java.util.List;
	import java.util.function.Consumer;
	import java.util.stream.Stream;
	import java.util.Arrays;
	
	public class Main {
	    public static void main(String args[]) {
	        List<Integer> nums = Arrays.asList(4, 5, 6, 7);
	        Stream<Integer> s1 = nums.stream();
	        s1.forEach((n) -> System.out.println(n));
	        s1.forEach((n) -> System.out.println(n)); // stream has already been operated upon or closed
	    }
	}
	Actual Code:
 		import java.util.List;
		import java.util.stream.Stream;
		import java.util.Arrays;
		
		public class Main {
		    public static void main(String args[]) {
		        List<Integer> nums = Arrays.asList(4, 5, 6, 7);
		        Stream<Integer> s1 = nums.stream();
		        Stream<Integer> s2 = s1.filter(n -> n % 2 == 0); //Filter function
		        Stream<Integer> s3 = s2.map(n -> n * n); //Map function
		        s3.forEach((n) -> System.out.println(n)); //forEach
		        // Instead of doing in this many variables we can write like this
		        int result = nums.stream().filter(n -> n % 2 == 0).map(n -> n * n).reduce(0, (c, e) -> c + e);
		        System.out.println(result);
		    }
		}
### Parallel Strea
	Code:
 		import java.util.List;
		import java.util.ArrayList;
		import java.util.Random;
		import java.util.stream.Stream;
		
		public class Main {
		    public static void main(String args[]) {
		        List<Integer> nums = new ArrayList<>();
		        Random ran = new Random();
		        for (int i = 0; i < 1000; i++) {
		            nums.add(ran.nextInt());
		        }
		        int s1 = nums.stream().map(n -> n * n).reduce(0, (c, e) -> c + e);
		        int s2 = nums.stream().map(n -> n * n).mapToInt(n -> n).sum();
		        int s3 = nums.parallelStream().map(n -> n * n).mapToInt(n -> n).sum();
		        System.out.println(s1 + " " + s2 + " " + s3);
		    }
		}
		
		// Parallel stream works faster since it creates multiple threads
		// Parallel stream doesnot work if want to sort
## Optional Class
	There will be a scenario where i might not get any value in such case i need to make my string Optional so that i can avoid nullpointerexception
 	Code:
	 	import java.util.List;
		import java.util.Arrays;
		import java.util.Optional;
		
		public class Main {
		    public static void main(String args[]) {
		        List<String> names = Arrays.asList("ram", "krishna", "raja", "laxmi");
		        Optional<String> targetName = names.stream().filter(name -> name.contains("x")).findFirst();
		        // System.out.println(targetName.get()); // if laxmi is not present i get this exception NoSuchElementFoundException
		        // Instead we can use this to avoid this exception
		        System.out.println(targetName.orElse("Not Found")); // Gives values or Not Found
		
		        // We can do it another way
		        String newTarget = names.stream().filter(name -> name.contains("x")).findFirst().orElse("Not Found");
		        System.out.println(newTarget);
		    }
		}
### Method Reference
	Code:
 		import java.util.List;
		import java.util.Arrays;
		
		public class Main {
		    public static void main(String args[]) {
		        List<String> names = Arrays.asList("ram", "krishna", "raja", "laxmi");
		        List<String> uNames = names.stream().map(name -> name.toUpperCase()).toList();
		        System.out.println(uNames); // [RAM, KRISHNA, RAJA, LAXMI]
		        // Instead of this i can use simply the code of Map using Method refrence
		        // Method reference works on class/object::method Note: dont call this method just give name Example: String::toUpperCase
		        List<String> upperNames = names.stream().map(String::toUpperCase).toList();
		        System.out.println(upperNames);
		        upperNames.stream().forEach(System.out::println);
		    }
		}
### Constructor Reference
	Convert a names list to Student list
 	Code:
  		import java.util.List;
		import java.util.Arrays;
		
		class Student {
		    String name;
		
		    public Student(String name) {
		        this.name = name;
		    }
		}
		
		public class Main {
		    public static void main(String args[]) {
		        List<String> names = Arrays.asList("ram", "krishna", "laxmi");
		        List<Student> studentsObjs = names.stream().map(name -> new Student(name)).toList();
		        System.out.println(studentsObjs);
		
		        // Easiest way to do it
		        List<Student> students = names.stream().map(Student::new).toList();
		        System.out.println(students);
		    }
		}
### Maven
	Maven is a project management tool. that can help us do this operation such as compiling, running, Test, package, deploy
 	To use external libraries, and to to work with dependencies
  	maintaining jar files versioning.
   	Example:
		spring 5 works with hibernate 4
  		But we cannot say spring 6 can work with hibernate 4
	So downloading the dependence is not good.
 	Maven helps in this management.
### Spring Project Setup and structure
  	Every projects follows groupid, artifact id and version
   	groupid is the unique that cannot be found in the world, artifact id is the project name
    	com.koushik.java reverse of my domin since domain names are unique in the world
     	Java Turorial is the artifact id that is project name
	Pom.xml file stores all the dependencies and plugins many other settings
 	When we run a java applicaiton it doenot look at Pom file it looks at the effective pom, effective pom is responsible for all the dependices
  	Right click on pom file and click on effective pom to see it
   	Archetypes:
		Basic we can create our own templates for the projects or else we can use the existing template strcutures available in the world.
  	When ever i create a project i can choose archetype and select maven central for internet maven repos and select on spring-mvc-jersey archetype to start a project
### How maven works
	Every time when i ask for a dependency it is going to .m2 folder(local folder) located in the documents folder and searchs for the dependency if it is not found then it will go the maven central (internet) and download the dependency.
 	Since most of the dependencies we are getting from internet they can be vulnerable. so we need to update our dependencies time to time.
## JDBC (Java DataBase Connector)
	It follows 7 steps
 		1. Import Package
   		2. Load Driver and register(that is coming from jar file)
   		3. Create a Connection
	 	4. Create the statement
	 	5. Excecute the statement
   		6. Process the request
   		6. Close
	Simple Code to connect to postgres and execute a query to retrive a student name
	 Connect to postgres sql
  		1. postgres dependency from mvm repo to the pom.xml file
		Write this code in this in Main.java
			package org.example;
			import java.sql.*;
			import java.lang.*;
			
			public class Main {
			    public static void main(String[] args) throws ClassNotFoundException, SQLException{
			        String url = "jdbc:postgresql://localhost:5432/java_tutorial";
			        String uname = "postgres";
			        String password = "koushik";
			        String query = "select * from student where sid=3";
			
			        // Class.forName("org.postgresql.Driver"); // Registering the driver(optional)
			        Connection con = DriverManager.getConnection(url, uname, password); // Make connection
			        Statement st = con.createStatement();
			        ResultSet result = st.executeQuery(query);
			        System.out.println(result); // org.postgresql.jdbc.PgResultSet@43bd930a
		   
			        result.next(); // The pointer in the database is pointing at the title of database by using .next() the pointer will shift to next record if found true else false
			        System.out.println(result.getString("sname"));
			
			        con.close(); // close the connection
			        System.out.println("Connection Established");
			    }
			}

#### Retriving multiple values
	query = "select * from student";
 	while(result.next()){
  		System.out.println(result.getString("sname"));
	}
### CRUD operations
	For select we use st.executeQuery() returns queryset; for insert, delete, update we use st.execute(); returns boolean 
		package org.example;
		import java.sql.*;
		import java.lang.*;
		
		public class Main {
		    public static void main(String[] args) throws ClassNotFoundException, SQLException{
		        String url = "jdbc:postgresql://localhost:5432/java_tutorial";
		        String uname = "postgres";
		        String password = "koushik";
		        
		//      String query = "insert into student values(5, 'john'),(6,'ram')";
		//      String updateQuery = "update student set sname='jonny' where sname='john'";
		        String deleteQuery = "delete from student where sid=6";
		
		        Connection con = DriverManager.getConnection(url, uname, password); // Make connection
		        Statement st = con.createStatement();
		        
		//      boolean status = st.execute(query);
		//      boolean status = st.execute(updateQuery);
		        boolean status = st.execute(deleteQuery);
		        System.out.println(status); // insert,update or delete query false
		        
		        con.close(); // close the connection
		        System.out.println("Connection Established");
		    }
		}
#### Prepared Statements
	Instead of writing raw sql queries we can use prepared statements Advantages: does chaching, stops sql injection.
 		package org.example;
		import java.sql.*;
		import java.lang.*;

		public class Main {
		    public static void main(String[] args) throws ClassNotFoundException, SQLException{
		        String url = "jdbc:postgresql://localhost:5432/java_tutorial";
		        String uname = "postgres";
		        String password = "koushik";
		
		        int sid = 7;
		        String sname = "harsha";
		        String query = "insert into student values(?,?)";
		
		        Connection con = DriverManager.getConnection(url, uname, password); // Make connection
		        PreparedStatement ps = con.prepareStatement(query);
		
		        ps.setInt(1, sid); // Instead of using column name we can give numbering also
		        ps.setString(2, sname);
		        ps.execute(); // Important step
		
		        con.close(); // close the connection
		        System.out.println("Connection Established");
		    }
		}

   
     	
	
 
   
      	




	








