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
    - [Section 1: HTML Basics](#section-1-html-basics)
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
    -  Assigning and executing variable name via a string
        ```
        String message = "Hello World";
        //message would be the variable name
        ```
        - Now we can reference the variable using another command
            ```
            String message = "Hello World";
            System.out.println(message);
            ```
        - We can use a '+' sign to join (concatenate) a variable and a string
            ```
            System.out.println(message + "hello world");
            ```
    - 

2. #### ***HTML Foundations***
    - 