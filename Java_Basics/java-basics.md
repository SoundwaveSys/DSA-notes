# Java Basics
*(Write Once, Run Anywhere)*

Java is a high-level, class-based, object-oriented programming language that is designed to have as few implementation dependencies as possible. It is a general-purpose programming language intended to let application developers write once, run anywhere (WORA), meaning that compiled Java code can run on all platforms that support Java without the need for recompilation.

---

# 1. Sample Code

Let's look at the most basic Java program: Hello World.

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

## Understanding the Parts

### `class Main`
Everything in Java happens inside a class. We define a class named "Main". Ideally, the file name should also be `Main.java`.

### `public static void main(String[] args)`
This is the entry point.

- `public`: Access modifier, means it can be accessed from anywhere.
- `static`: It can be run without creating an object of the class.
- `void`: It does not return any value.
- `main`: The name of the method.
- `String[] args`: Command line arguments. We can pass inputs to the program when running it from the command line.

### `System.out.println`
The command to print output to the screen. `println` means "print line", so it moves to a new line after printing.

---

# 2. Comments

Comments are ignored by the computer. They are for humans to read.

```java
// This is a single line comment

/* 
   This is a 
   multi-line comment 
*/
```

---

# 3. Data Types

Java has 8 primitive data types to store different values.

| Data Type | Description |
|---|---|
| `byte` | 1 byte, small integers (-128 to 127) |
| `short` | 2 bytes, integers |
| `int` | 4 bytes, integers (Most common) |
| `long` | 8 bytes, large integers |
| `float` | 4 bytes, decimals (needs `f` suffix, e.g., `3.14f`) |
| `double` | 8 bytes, decimals (Most common for fractions) |
| `char` | 2 bytes, single character (e.g., `'A'`) |
| `boolean` | true or false |

---

# 4. Operators

## Arithmetic Operators

| Operator | Meaning |
|---|---|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `%` | Modulo |

## Unary Operators

Operators that require only one operand.

| Operator | Meaning |
|---|---|
| `++` | Increment |
| `--` | Decrement |
| `!` | Logical NOT |

## Relational Operators

Used to compare two values. They return a boolean result (`true` or `false`).

| Operator | Meaning |
|---|---|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

## Logical Operators

Used to determine the logic between variables or values.

| Operator | Meaning |
|---|---|
| `&&` | Logical AND |
| `||` | Logical OR |

## Assignment Operators

Used to assign values to variables.

| Operator | Meaning |
|---|---|
| `=` | Assignment |
| `+=` | Add and Assign |
| `-=` | Subtract and Assign |
| `*=` | Multiply and Assign |
| `/=` | Divide and Assign |
| `%=` | Modulo and Assign |

---

# 5. Strings

Strings are objects in Java, not primitives. They store text.

## Immutable
Once created, a `String` object cannot be changed. Modifying it creates a new object.

```java
String s1 = "Hello";

char[] arr = {'W', 'o', 'r', 'l', 'd'};

String s2 = new String(arr);

System.out.println(s1 + " " + s2);

System.out.println(s1.charAt(1));

System.out.println(s1.length());

System.out.println(s1.substring(0, 2));

System.out.println(s1.equals("Hello"));
```

---

# 6. Input Output

For input, we use the `Scanner` class.

```java
import java.util.Scanner;

public class InputExample {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int age = sc.nextInt();

        String name = sc.next();

        System.out.println(name + " is " + age);

        sc.close();
    }
}
```

## What about BufferedReader?

`BufferedReader` is another way to read input. It is faster but harder to use (requires parsing strings to numbers manually). `Scanner` is easier and preferred for beginners.

---

# 7. Type Casting

Converting one data type to another.

## Implicit (Widening)

Small type to large type (e.g., `int` to `double`). This happens automatically by the compiler.

## Explicit (Narrowing)

Large type to small type (e.g., `double` to `int`). This must be done manually by the programmer.

```java
int myInt = 9;

double myDouble = myInt;

int heavyInt = (int) 9.78;
```

---

# 8. Constants

Use the `final` keyword to create constants. These values cannot be changed.

```java
final float PI = 3.14f;

// PI = 3.15f;
```

---

# 9. Arrays

Storing multiple values of the same type.

```java
int[] scores = {90, 80, 70};

System.out.println(scores.length);

System.out.println(scores[0]);

for (int i : scores) {
    System.out.println(i);
}

int[][] matrix = { {1, 2}, {3, 4} };
```

---

# 10. Conditional Statements

## If, Else If, Else

```java
int marks = 85;

if (marks > 90) {
    System.out.println("A");
}
else if (marks > 80) {
    System.out.println("B");
}
else {
    System.out.println("C");
}
```

### Explanation

The program checks the condition `marks > 90`. Since `85` is not greater than `90`, it moves to the next condition `marks > 80`. This is true, so it prints `"B"`.

---

## Switch Statement

```java
int day = 2;

switch (day) {

    case 1:
        System.out.println("Monday");
        break;

    case 2:
        System.out.println("Tuesday");
        break;

    default:
        System.out.println("Invalid");
}
```

### Explanation

The computer checks the value of `day`. It matches with `case 2` and executes the code inside it.

- `break`: Stops the code from running into the next case automatically.
- `default`: Runs if no case matches the value.

---

# 11. Loops

## For Loop

```java
for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

## While Loop

```java
int i = 0;

while (i < 5) {
    System.out.println(i);
    i++;
}
```

## Do While Loop

```java
int i = 0;

do {
    System.out.println(i);
    i++;
}
while (i < 5);
```

---

# 12. Exception Handling

Handling errors so the program doesn’t crash.

```java
try {

    int[] myNumbers = {1, 2, 3};

    System.out.println(myNumbers[10]);

}
catch (Exception e) {

    System.out.println("Something went wrong.");

}
finally {

    System.out.println("The 'try catch' is finished.");
}
```

---

# Summary

We covered the fundamental building blocks of Java:

- Structure: Class based, main method
- Data: Types, Variables, Arrays, Strings
- Logic: Operators, If-Else, Switch
- Control: Loops (for, while)
- Safety: Exception Handling

Practice writing these snippets to get comfortable with the syntax!