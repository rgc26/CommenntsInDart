author: Dart Tutorial Team
summary: Learn about different types of comments in Dart including single-line, multi-line, and documentation comments
id: comments-in-dart
categories: codelab,markdown,programming,dart
environments: Web
status: Published
feedback link: https://github.com/your-repo
analytics account: Google Analytics ID

# Comments in Dart Tutorial

## Overview
Duration: 0:02:00

Welcome to the Comments in Dart Tutorial! This codelab will teach you everything you need to know about comments in Dart programming language. Comments are essential for writing readable and maintainable code.

**What you'll learn:**
* Understanding what comments are and their purpose
* Different types of comments in Dart
* Single-line comments and their usage
* Multi-line comments for longer explanations
* Documentation comments for generating documentation
* Best practices for writing effective comments

**Prerequisites:**
* Basic understanding of programming concepts
* Familiarity with Dart syntax (from previous tutorials)

Positive
: Comments are crucial for code documentation and collaboration - they help you and others understand your code better!

## Understanding Comments
Duration: 0:03:00

**Comments** are the set of statements that are ignored by the Dart compiler during program execution. They are used to explain the code so that you or other people can understand it easily.

### What are Comments?

Comments are non-executable text in your code that provide explanations, documentation, or notes about what the code does. They are completely ignored by the Dart compiler and don't affect the program's execution.

### Why Use Comments?

Comments serve several important purposes:

* **Code Documentation**: Explain what your code does
* **Code Maintenance**: Help you understand your own code later
* **Team Collaboration**: Help other developers understand your code
* **Debugging**: Add notes about complex logic or workarounds
* **Documentation Generation**: Create API documentation automatically

### Advantages of Comments

* You can describe your code clearly
* Other people will understand your code more easily
* You can explain complex algorithms or business logic
* Comments help with code maintenance and debugging
* Documentation comments can generate API docs automatically

Positive
: Good commenting practices make your code more professional and easier to maintain!

## Types of Comments in Dart
Duration: 0:03:00

Dart supports three different types of comments, each with its own purpose and syntax.

### Comment Types Overview

* **Single-Line Comment**: For commenting on a single line of code
  * Syntax: `// This is a single-line comment`
* **Multi-Line Comment**: For commenting on multiple lines of code
  * Syntax: `/* This is a multi-line comment */`
* **Documentation Comment**: For generating documentation or reference for a project/software package
  * Syntax: `/// This is a documentation comment`

### When to Use Each Type

* **Single-Line Comments**: Quick explanations, variable descriptions, TODO notes
* **Multi-Line Comments**: Longer explanations, algorithm descriptions, section headers
* **Documentation Comments**: API documentation, function descriptions, class documentation

Negative
: Remember that comments should explain "why" not "what" - the code itself should be self-explanatory for the "what" part!

## Single-Line Comments in Dart
Duration: 0:03:00

Single-line comments are the most common type of comment in Dart. They start with `//` and continue to the end of the line.

### Basic Single-Line Comment

```dart
void main() {
// This is single-line comment.
print("Welcome to Technology Channel.");
}
```

**Output:**
```
Welcome to Technology Channel.
```

### Single-Line Comments with Code

```dart
void main() {
  // Declare variables
  String name = "John";  // User's name
  int age = 25;         // User's age
  
  // Calculate years until retirement
  int yearsToRetirement = 65 - age;  // Assuming retirement at 65
  
  // Display information
  print("Name: $name");
  print("Age: $age");
  print("Years until retirement: $yearsToRetirement");
}
```

**Output:**
```
Name: John
Age: 25
Years until retirement: 40
```

### Inline Comments

```dart
void main() {
  int result = 10 + 20;  // Calculate sum
  print(result);          // Display result
  
  // TODO: Add input validation
  // FIXME: Handle edge case when age is negative
  // NOTE: This function will be deprecated in version 2.0
}
```

### Best Practices for Single-Line Comments

* Keep comments concise and clear
* Use comments to explain "why" not "what"
* Add comments for complex logic or business rules
* Use TODO, FIXME, or NOTE for special annotations
* Don't over-comment obvious code

Positive
: Single-line comments are perfect for quick explanations and inline documentation!

## Multi-Line Comments in Dart
Duration: 0:03:00

Multi-line comments are used when you need to write longer explanations that span multiple lines. They start with `/*` and end with `*/`.

### Basic Multi-Line Comment

```dart
void main(){  
/*
This is a multi-line comment.
You can write multiple lines here.
The compiler will ignore all of this text.
*/
    print("Welcome to Technology Channel.");  
}  
```

**Output:**
```
Welcome to Technology Channel.
```

### Multi-Line Comments for Complex Logic

```dart
void main() {
  /*
   * This function calculates the compound interest
   * Formula: A = P(1 + r/n)^(nt)
   * Where:
   * A = Final amount
   * P = Principal amount
   * r = Annual interest rate
   * n = Number of times interest is compounded per year
   * t = Time in years
   */
  
  double principal = 1000;
  double rate = 0.05;  // 5% annual interest
  int time = 5;        // 5 years
  int compoundings = 12; // Monthly compounding
  
  double amount = principal * pow((1 + rate/compoundings), (compoundings * time));
  print("Final amount: \$${amount.toStringAsFixed(2)}");
}
```

### Multi-Line Comments for Section Headers

```dart
void main() {
  /*
   * ============================================
   * STUDENT GRADE CALCULATOR
   * ============================================
   * This program calculates a student's final grade
   * based on their scores in different subjects.
   * ============================================
   */
  
  // Variable declarations
  double mathScore = 85.5;
  double scienceScore = 92.0;
  double englishScore = 78.5;
  
  // Calculate average
  double average = (mathScore + scienceScore + englishScore) / 3;
  
  // Display results
  print("Math: $mathScore");
  print("Science: $scienceScore");
  print("English: $englishScore");
  print("Average: ${average.toStringAsFixed(2)}");
}
```

### Multi-Line Comments for Algorithm Explanations

```dart
void main() {
  List<int> numbers = [5, 2, 8, 1, 9, 3];
  
  /*
   * BUBBLE SORT ALGORITHM
   * 
   * This algorithm sorts the array by repeatedly
   * stepping through the list, comparing adjacent
   * elements and swapping them if they are in
   * the wrong order.
   * 
   * Time Complexity: O(n²)
   * Space Complexity: O(1)
   */
  
  for (int i = 0; i < numbers.length - 1; i++) {
    for (int j = 0; j < numbers.length - i - 1; j++) {
      if (numbers[j] > numbers[j + 1]) {
        // Swap elements
        int temp = numbers[j];
        numbers[j] = numbers[j + 1];
        numbers[j + 1] = temp;
      }
    }
  }
  
  print("Sorted array: $numbers");
}
```

Negative
: Multi-line comments should be used sparingly and only when single-line comments are insufficient!

## Documentation Comments in Dart
Duration: 0:04:00

Documentation comments are special comments that start with `///` and are used to generate documentation for your code. They are particularly useful for creating API documentation.

### Basic Documentation Comment

```dart
void main(){  
/// This is documentation comment
    print("Welcome to Technology Channel.");  
}  
```

**Output:**
```
Welcome to Technology Channel.
```

### Documentation Comments for Functions

```dart
/// Calculates the area of a circle given its radius.
/// 
/// [radius] The radius of the circle in units.
/// Returns the area of the circle in square units.
/// 
/// Example:
/// ```dart
/// double area = calculateCircleArea(5.0);
/// print(area); // Output: 78.54
/// ```
double calculateCircleArea(double radius) {
  const double pi = 3.14159;
  return pi * radius * radius;
}

void main() {
  double area = calculateCircleArea(5.0);
  print("Circle area: ${area.toStringAsFixed(2)}");
}
```

### Documentation Comments for Classes

```dart
/// Represents a student in the school system.
/// 
/// This class contains information about a student including
/// their name, age, and academic performance.
class Student {
  /// The student's full name.
  final String name;
  
  /// The student's age in years.
  final int age;
  
  /// The student's grade point average (0.0 to 4.0).
  double gpa;
  
  /// Creates a new student with the given information.
  /// 
  /// [name] The student's full name.
  /// [age] The student's age in years.
  /// [gpa] The student's grade point average.
  Student(this.name, this.age, this.gpa);
  
  /// Returns whether the student is eligible for honors.
  /// 
  /// A student is eligible for honors if their GPA is 3.5 or higher.
  bool isEligibleForHonors() {
    return gpa >= 3.5;
  }
}

void main() {
  Student student = Student("Alice Johnson", 18, 3.8);
  print("Student: ${student.name}");
  print("Eligible for honors: ${student.isEligibleForHonors()}");
}
```

### Documentation Comments with Parameters and Return Values

```dart
/// Calculates the factorial of a given number.
/// 
/// The factorial of a number n is the product of all positive
/// integers less than or equal to n.
/// 
/// [n] The number to calculate factorial for.
/// Returns the factorial of [n].
/// 
/// Throws [ArgumentError] if [n] is negative.
/// 
/// Example:
/// ```dart
/// int result = factorial(5);
/// print(result); // Output: 120
/// ```
int factorial(int n) {
  if (n < 0) {
    throw ArgumentError('Factorial is not defined for negative numbers');
  }
  
  if (n <= 1) {
    return 1;
  }
  
  return n * factorial(n - 1);
}

void main() {
  try {
    int result = factorial(5);
    print("Factorial of 5: $result");
  } catch (e) {
    print("Error: $e");
  }
}
```

### Generating Documentation

Documentation comments can be used with Dart's documentation generator (`dartdoc`) to create beautiful API documentation:

```bash
# Generate documentation
dart doc

# Or for a specific package
dart doc --output=docs
```

Positive
: Documentation comments are essential for creating professional API documentation and helping other developers use your code!

## Best Practices for Comments
Duration: 0:02:00

Writing good comments is an art. Here are some best practices to follow when commenting your Dart code.

### Do's and Don'ts

**Do's:**
* Write comments that explain "why" not "what"
* Keep comments up-to-date with code changes
* Use clear and concise language
* Comment complex algorithms and business logic
* Use documentation comments for public APIs
* Add TODO, FIXME, or NOTE for special cases

**Don'ts:**
* Don't comment obvious code
* Don't write comments that just repeat the code
* Don't leave outdated comments
* Don't over-comment simple code
* Don't use comments to explain bad code - fix the code instead

### Examples of Good vs Bad Comments

```dart
// ❌ Bad - Comment just repeats the code
int age = 25; // Set age to 25

// ✅ Good - Comment explains the business logic
int age = 25; // Minimum age required for the program

// ❌ Bad - Obvious comment
print("Hello"); // Print hello

// ✅ Good - Explains the purpose
print("Hello"); // Display welcome message to user

// ❌ Bad - Outdated comment
int maxUsers = 100; // Maximum 50 users allowed

// ✅ Good - Accurate comment
int maxUsers = 100; // Maximum users allowed in the system
```

### Comment Style Guidelines

```dart
// Use consistent capitalization
// Start with a capital letter and end with a period
String userName = "john"; // User's display name.

// For multi-line comments, align them properly
/*
 * This is a properly formatted
 * multi-line comment with
 * consistent indentation.
 */

/// Use documentation comments for public APIs
/// 
/// This function calculates the total price including tax.
/// [price] The base price before tax.
/// [taxRate] The tax rate as a decimal (e.g., 0.08 for 8%).
/// Returns the total price including tax.
double calculateTotalPrice(double price, double taxRate) {
  return price * (1 + taxRate);
}
```

### Special Comment Tags

```dart
// TODO: Add input validation for email field
// FIXME: This calculation is off by 1 for edge cases
// NOTE: This function will be deprecated in version 2.0
// HACK: Temporary workaround until the bug is fixed
// XXX: This code needs to be reviewed

void processUserData(String email) {
  // TODO: Validate email format
  // FIXME: Handle empty email strings
  
  if (email.isEmpty) {
    print("Error: Email cannot be empty");
    return;
  }
  
  // Process the email
  print("Processing email: $email");
}
```

Positive
: Following these best practices will make your code more professional and easier to maintain!

## Practice Exercise
Duration: 0:02:00

Now it's time to practice what you've learned about comments in Dart!

### Exercise: Comment Your Code

Take the following Dart code and add appropriate comments to make it more readable and maintainable:

```dart
void main() {
  List<int> scores = [85, 92, 78, 96, 88];
  int total = 0;
  
  for (int score in scores) {
    total += score;
  }
  
  double average = total / scores.length;
  
  if (average >= 90) {
    print("Excellent performance!");
  } else if (average >= 80) {
    print("Good performance!");
  } else if (average >= 70) {
    print("Average performance!");
  } else {
    print("Needs improvement!");
  }
}
```

### Sample Solution with Comments

```dart
/// Student Grade Calculator
/// 
/// This program calculates the average score from a list of test scores
/// and provides feedback based on the performance level.
void main() {
  // List of student test scores
  List<int> scores = [85, 92, 78, 96, 88];
  
  // Calculate total score
  int total = 0;
  for (int score in scores) {
    total += score;
  }
  
  // Calculate average score
  double average = total / scores.length;
  
  // Provide feedback based on average score
  if (average >= 90) {
    print("Excellent performance!");
  } else if (average >= 80) {
    print("Good performance!");
  } else if (average >= 70) {
    print("Average performance!");
  } else {
    print("Needs improvement!");
  }
}
```

### Additional Challenge

Create a function that calculates the factorial of a number and add comprehensive documentation comments:

```dart
/// Calculates the factorial of a given number.
/// 
/// The factorial of a number n (denoted as n!) is the product of all
/// positive integers less than or equal to n.
/// 
/// [n] The number to calculate factorial for.
/// Returns the factorial of [n].
/// 
/// Throws [ArgumentError] if [n] is negative.
/// 
/// Example:
/// ```dart
/// int result = factorial(5);
/// print(result); // Output: 120 (5 * 4 * 3 * 2 * 1)
/// ```
int factorial(int n) {
  // Handle negative numbers
  if (n < 0) {
    throw ArgumentError('Factorial is not defined for negative numbers');
  }
  
  // Base case: factorial of 0 and 1 is 1
  if (n <= 1) {
    return 1;
  }
  
  // Recursive case: n! = n * (n-1)!
  return n * factorial(n - 1);
}

void main() {
  try {
    int result = factorial(5);
    print("Factorial of 5: $result");
  } catch (e) {
    print("Error: $e");
  }
}
```

Negative
: Try to solve this exercise on your own before looking at the solution!

Positive
: Practice is the best way to master commenting techniques!

## Next Steps
Duration: 0:01:00

Congratulations! You've completed the Comments in Dart Tutorial. Here's what you've accomplished:

### What You've Learned

* ✅ Understanding of what comments are and their purpose
* ✅ Knowledge of different types of comments in Dart
* ✅ Single-line comments and their usage
* ✅ Multi-line comments for longer explanations
* ✅ Documentation comments for generating documentation
* ✅ Best practices for writing effective comments

### Continue Your Learning Journey

To expand your Dart knowledge, consider learning about:

* **Operators in Dart** - How to perform operations on data
* **Control Flow** - Using conditions and loops
* **Functions** - Creating reusable code blocks
* **Classes and Objects** - Object-oriented programming
* **Error Handling** - Managing exceptions and errors
* **Testing** - Writing unit tests for your code

### Resources

* [Official Dart Documentation](https://dart.dev/guides)
* [Dart Language Tour](https://dart.dev/guides/language/language-tour)
* [Dart Tutorial Website](https://dart-tutorial.com)
* [DartPad](https://dartpad.dev) - Online Dart editor

### Final Challenge

Create a simple calculator program that:
* Uses all three types of comments appropriately
* Includes documentation comments for public functions
* Demonstrates best practices for commenting
* Has clear explanations for complex logic

Positive
: You now have a solid understanding of comments in Dart and are ready to write well-documented, professional code!

Negative
: Remember to always keep your comments up-to-date and use them to explain "why" not "what"! 