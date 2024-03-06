# Chapter 1: Basic Kotlin Syntax and Structure

**Lessons:** 
- Variables and data types
- Understanding user input and control flows
- Working through loops and operators 

### What are Variables?
Variables hold data types such as numbers, characters, strings, lists, objects, and so forth.

### Creating Variables: Basic Kotlin Syntax and Structure
Variables are defined using the `var` or `val` keywords, followed by the variable name, an optional data type, and an assignment. The assignment operator is represented by the equals sign (`=`). The assignment operator is used to assign a value to a variable.

- `var` variableName: DataType = value //Mutable (var is changeable)
- `val` constantName: DataType = value // Immutable (val is not changeable)

```kotlin
var age: Int = 20
var name = "Vahe" 
val isProgrammer = true
```

When a value is assigned to a `var` variable, you can change its value. However, when a value is assigned to a `val` variable, you cannot change it. 

### What are Data types?
Data types are labels that tell the computer what type of data you are dealing with. Once a data type is set, it stays the same.

#### Integers (Int and Long)
Integer types hold whole numbers. The most common type is `Int` and for larger values, you may use `Long`.

```kotlin
var age: Int = 20
var oneBillion: Long = 1_000_000_000L
```

#### Floats and Doubles (Float and Double)
Floats and Doubles are used for decimals. Double is more precise and is the default Kotlin uses for decimal numbers.

```kotlin
var pi: Double = 3.14
var floatNumber: Float = 2.73F // The F must be used to indicate a Float.
```

#### Booleans
Booleans have a true or false value (on/off). They are used to code decisions and allow a portion of the code to run based on whether the condition is true or false.

#### Logical Operators
- || (OR): Is true if at least one condition is true.
- && (AND): Is true if both conditions are true.
- ! (NOT): Turns a true value into a false value and vice versa.

```kotlin
val isWeekend = true
val hasHomework = false

val shouldRelax = isWeekend || hasHomework // shouldRelax will be true because at least one condition (isWeekend) is true.
```

```kotlin
val isMorning = true
val isHungry = true

val shouldEatBreakfast = isMorning && isHungry // shouldEatBreakfast will be true only because both conditions are true.
```

### Char
The char data type is used for single characters such as a letter, a number, or symbols. The char data type is used with single quotes.

```kotlin
var letter: Char = 'A'
var number: Char = '3'
var symbol: Char = '!'
```

You can also use Unicode characters for additional symbols or letters in different languages.

```kotlin
var heart: Char = '\u2764'
println(heart) // This will output a heart emoji
```

### Strings
A string is a sequence of characters that are used with double quotes. You can use strings to create texts such as sentences.

```kotlin
var aGreeting: String = "Hello, Earth!"
```

You can also join strings together using the + operator. This is known as string concatenation.

```kotlin
var firstName = "Samus"
var lastName = "Aran"
var fullName = firstName + " " + lastName
```

### Type Casting
This is a process that allows you to convert a type of variable to a different data type. 

### User Input
User input is necessary to create interactive programs. In order to ask the user for input and to display it, you may use `println()` to show a message and `readLine()` to get a response from the user.

```kotlin
println("Please enter your name:") // Displays to the user
val userName = readLine() // Get a response from the user
println("Hello, $userName!") // Shows the response
```

### 'if', 'if else', and 'else if' statements
if and else if statements are used to make decisions based on conditions. 

```kotlin
var age = 20
if (age >= 18) {
    println("You can vote.")
}
```

```kotlin
var age = 15
if (age >= 18) {
    println("You may vote")
} else {
    println("You may not vote")
}
```

```kotlin
var number = 0
if (number > 0) {
    println("The number is positive.")
} else if (number == 0) {
    println("The number is zero.")
} else {
    println("The number is negative.")
}
```

### 'When' Statements
These are like decision-makers. You give 'when' a value, and it picks a result based on the value.

```kotlin
var number = 2
when (number) {
    1 -> println("It is one")
    2 -> println("It is two")
    3 -> println("It is three")
    else -> println("It is not one, two, or three")
}
```

### 'While' loops
A while loop keeps doing a task for as long as a certain condition is true.

```kotlin
var count = 1
while (count <= 5) {
    println("Clap")
    count++
}
```

```kotlin
var countdown = 5
while (countdown >= 0) {
    println("Countdown: $countdown")
    countdown--
}
println("Timer has ended")
```

### Operators
These are special symbols/keywords used to perform operations including arithmetic, comparisons, assignment, and logic. 

**Arithmetic Operators:**

- Addition (+)
- Subtraction (-)
- Multiplication (*)
- Division (/)
- Modulus (%)

**Comparison Operators:**

- Equals (==)
- Not Equals (!=)
- Greater Than (>)
- Less Than (<)
- Greater Than or Equal To (>=)
- Less Than or Equal To (<=)

**Assignment Operators:**

- Equals (=)
- Plus Equals (+=)
- Minus Equals (-=)
- Multiply Equals (*=)
- Divide Equals (/=)

**Logical Operators:**

- AND (&&)
- OR (||)
- NOT (!)

### Additional Notes
- Kotlin is a multi-paradigm language centered on safety, conciseness, and interoperability.
- Kotlin is considered a multi-paradigm language because it allows programmers to leverage different programming approaches within the same codebase, such as Object-oriented, functional, and procedural.
- Kotlin is concise and expressive language, removing boilerplate and providing building blocks for creating readable Domain-Specific Languages.
- Kotlin is interoperable with Java, allowing both languages to be mixed within the same project.
- Kotlin Coroutines are a lightweight alternative to threads.
```
