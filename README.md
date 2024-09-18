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












