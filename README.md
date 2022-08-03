# java-journey-notes
The goal of this section is to record a Java cheat-sheet for a future reference guide.

I'll keep things barebones for my own understanding while providing some reference links if I want to explore other niche areas further. 

# Reference Links
- Java Cheat Sheet
    - 

## Table of Contents
- [Java Journey Notes](#java-journey-notes)
- [Reference Links](#reference-links)
    - [Table of Contents](#table-of-contents)
    - [Section 1: HTML Basics](#section-1-java-basics)
    - [Section 2: CSS Basics](#section-2-css-basics)
    - [Section 3: Adaptive Sizing](#section-3-adaptive-sizing)
    - [Section 4: Box Model and Page Structure](#section-4-box-model-and-page-structure)
    - [Section 5: Web Components and Layout Patterns](#section-5-web-components-and-layout-patterns)
    - [Section 6: Responsiveness](#section-6-responsiveness)
    - [Section 7: Frameworks](#section-7-frameworks)

### Section 1: Java Basics
- Java Structure

1. #### ***Java Formatting***
    - Basic syntax
        - // for commenting
        - /* */ for multi-line commenting
        - ; to end/separate arguments
    - Source starts with boilerplate code
        - In this example, the 'public class' is our source name, and execution of the program comes after '...args) {'
            ```
            public class Example {
                public static void main(String[] args) {
                System.out.println("Text to be printed");
                    }
                }
            ```
        - Classes like 'System' and 'String' must be capitalized
        - shortcut for 'System.out' is 'sout'+tab
    - Import tools before beginning of program frame
        ```
        import java.util.Scanner;
        public class Program {
            ...
        ```
        - the scanner tool comes with Java and reads user input

2. #### ***Variables***
    - Think of a variable as a container in which information can be stored
        - Examples include:
            - Text (string)
            - whole numbers (int)
                - i.e. 123
            - floating-point numbers (double)
                - i.e. 1.352454
            - true/false (boolean)
    - Variables are assigned using = sign
        ```
        int months = 12;
        ```
        - The variable name is 'months' and the value is 12
    - No two variables can have the same name
        ```
        int months = 12;
        System.out.println("the value is " + months);
        months = 24;
        System.out.println("the value is " + months);
        ```
        - The system would print 12 first, and then 24.
            - The computer first creates a container called 'months' that is defined as a 'int' type, and 12 is input into the container
            - For the 2nd value, the computer checks to see if a container already exists. If it does, the new value overwrites the old value. If the container name isn't found, there will be an error message
    - Variables cannnot have two different type's
        ```
        boolean integerTest = false;
        integerTest = 123; //does not work

        int value = 10;
        integerTest = values; //neither does this
        ```
        - Exception for this rule is that an integer can be assigned to a floating-point variable, since Java knows how to convert an integer to a floating-point during assignment
            ```
            double floatingPoint = 0.42;
            floatingPoint = 1; //works

            int value = 10;
            floatingPoint = value; //also works
            ``` 
        - 









3. #### ***Strings***
    - Assigning and executing variable name via a string
        ```
        String message = "Hello World";
        //message would be the variable name
        ```
        - Now we can reference the variable using another command
            ```
            String message = "Hello World";
            System.out.println(message);
            ```
    - Add scanner to string variable - i.e. reading user input
        ```
        String message = scanner.nextLine();
        ```
        - The variable (message) output won't get printed until it's called. This means we
        can add a delay of printing the variable until we get multiple inputs
        - Difference between 'scanner.nextLine' and 'reader.nextLine':
            - scanner saves the input to memory and doesn't return it
            - reader will return the input when the variable is called
    - We can use a '+' sign to join (concatenate) a variable and a string
        ```
        System.out.println(message + "hello world");
        ```
        - If writing text that is long and want to add new lines, do '/n' within the quotes for a new line
    - Multi-step process combining with text
        ```
        System.out.println("What's your name?");
        String message = scanner.nextLine();
        System.out.println("Hi " + message);
        ```
    - Math with variables
        ```
        double pi = 3.14;
        double radius = 22.0;
        double surfaceArea = pi * radius * radius;

        System.out.println(surfaceArea); //1519.76 output
        ```
   