# JAVA
This sheet convers all the basics of JAVA
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
    











