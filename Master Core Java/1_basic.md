# 1. Basic Syntax

## Structure of a Java program:
1. Class → everything in Java is inside a class.
2. main() method → entry point.
3. Statements end with ;.
4. Curly braces { } define blocks.

```
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello Java");
    }
}
```

## Interview Qs:
#### What is the entry point of a Java program?
→ public static void main(String[] args)

#### Why is main() method static?
→ So it can run without creating an object.

#### Difference between JDK, JRE, and JVM?
JVM → runs bytecode
JRE → JVM + libraries
JDK → JRE + compiler + tools

# Variables
Definition: A variable is a named memory location.

## Types of variables:
1. Local Variable → declared inside method, not stored in heap.
2. Instance Variable → declared in class, each object has its own copy.
3. Static Variable → declared with static, shared among all objects.

Example : 
```
class Test {
    int instanceVar = 20; //Instance variable
    static int staticVar = 30; //Static variable

    void display() {
        int localVar = 30; // local variable
        System.out.println(localVar);
    }
}
```
### Can a local variable have default value?
→ No, must be initialized before use.

# Data Types
## Primitive Data Types (8):

byte (1 byte), short (2), int (4), long (8)
float (4), double (8)
char (2, Unicode)
boolean (1 bit but JVM uses 1 byte)
Non-primitive Data Types: String, Arrays, Classes, Objects.

## Interview Qs:

#### Difference between primitive and non-primitive data types?
#### Why is char 2 bytes in Java?
→ Supports Unicode (not just ASCII).
#### Default values of primitive data types?
int → 0, double → 0.0, boolean → false, object → null

# Operators
Arithmetic: + - * / %
Relational: == != > < >= <=
Logical: && || !
Assignment: = += -= *= /= %=
Unary: ++ --
Ternary: condition ? value1 : value2

### Difference between == and .equals()?

Ans : == and .equals() both are used to compare the two values.

1.1. == is used to compare the primitives.
e.g : 

int a = 10;
int b = 10;
System.out.println(a==b); //true

1.2. For object type it's used to compare the references.

String str1 = new String("Kundan");
String str2 = new String("Kundan");
System.out.println(str1==str2); //false becase in this case the it's created two object which have different memory

String str3 = "Kundan";
String str4 = "Kundan";
System.out.println(str3==str4); // true (string literal pool optimization)

2. .equals() Method:
Object Types:
The .equals() method is a method inherited from the Object class and is primarily used to compare the content or value of objects.

eg. 
    String s1 = new String("hello");
    String s2 = new String("hello");
    System.out.println(s1.equals(s2)); // true (String class overrides equals() to compare content)

### Summary of Key Differences:
    == is an operator; .equals() is a method.
    == compares primitive values directly and object references (memory locations).
    .equals() compares the content or value of objects and can be overridden for custom content-based equality.

# Control Flow
### (a) If-Else

Used for decision-making.
if(num % 2 == 0)
    System.out.println("Even");
else
    System.out.println("Odd");

### (b) Switch

Provides multiple options.
```
int day = 2;
switch(day) {
    case 1: System.out.println("Mon"); break;
    case 2: System.out.println("Tue"); break;
    default: System.out.println("Other");
}
```

### (c) Loops
For Loop → when range is known.
```
for(int i=1; i<=5; i++) System.out.println(i);
```

While Loop → condition checked first.
```
int i=1;
while(i<=5) { System.out.println(i); i++; }
```

Do-While Loop → executes at least once.
```
int j=1;
do { System.out.println(j); j++; } while(j<=5);
```
