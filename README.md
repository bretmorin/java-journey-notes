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
    - Variable naming
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
        - Variables cannot have spaces or ! in name, but can have numbers as long as the name doesn't begin with a number
            - camelCase should be used in naming when possible
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
    - Order of variable assignment
        ```
        int test = 5;
        test = 2; //test is now 2, not 5
        ```
        - We can shorthand change a variable later on, and the most recent value is the most relevant
        - If we have a variable assigned to a variable, it will only find the most recent iteration value of that variable
            ```
            int second = 32;
            int first = 25;
            second = 17; // second now is 17
            first = second; // this just means that first = 17
            System.out.println(second); //prints 17
            ```

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
    - Converting string to integer
        ```
        String valueAsString = "42"; //42 being text
        int value = Integer.valueOf(valueAsString);
        System.out.println(value); //42 is the output as a number
        //Integer.valueOf command 
        ```
        ```
        System.out.println("Give a number:");
        int result = Integer.valueOf(scanner.nextLine()); //reads input from first prompt and converts
        System.out.println("You gave the number " + result);
        ```
    - Converting string to a double 
        ```
        String valueAsString = "42.42"; //string (text)
        double value = Double.valueOf(valueAsString); //Double.valueOf takes string and converts as parameter
        System.out.println(value); //42.42 output
        ```
        - We can also convert an integer(whole number) into a double (floating-point)
    - Reading booleans
        ```
        System.out.println("Write a boolean");
        boolean value = Boolean.valueOf(scanner.nextLine()); //Boolean.valueOf converts string to boolean
        System.out.println("You wrote " + value); 
        //Write a boolean
        //(if you write 'True', it will say true in next line. If you write anything but T/F, it will say 'false')
        //You wrote false
        ```

4. #### ***Calculating with Numbers***
    - Math basic order of operations takes place, with multiplication and division executing before addition and subtraction, and performed left to right
        - We can affect the order of operations by adding parentheses
            ```
            int calcu = (1 + 1) + 3 * (2 + 5); //prints 23
            int calcu = 1 + 1 + 3 * 2 + 5; //prints 13
            ```
        - We can add parentheses to the println command instead of just the variable
            ```
            System.out.println("Four: " + (2 + 2));
            ```
    - Division between two integers will always produce an integer, rounded
        - However, if one or more of the numbers is a floating-point, then the result will be floating-point
            ```
            double whenDividendIsFloat = 3.0 / 2;
            System.out.printIn(whenDividendIsFloat); // prints 1.5
            ```
            - This does not apply if assigned to an int variable, like so
                ```
                int integer = 3.0 /2;
                System.out.println(integer); // 1
                ```
        - An integer can be converted to floating-point by assigning a variable that specifies a type operation before it
            ```
            int first = 3;
            int second = 2;

            double result1 = (double) first / second; // double must be in parentheses
            System.out.println(result1); // prints 1.5
            // if result1 = (double) (first / second), then the result would not be converted as the division would be executed first
            ```
5. #### ***Conditional Statements and Operations***
    - Math basic o
