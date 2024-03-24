### For Loops, Lists, Functions, and Methods
**Lessons**: mutable and immutable lists. Difference between functions and methods. List manipulation via indexing, adding, and removing elements. Loops.

#### `ListOf` and `MutableListOf`
- `ListOf` creates an immutable list and `MutableListOf` creates a mutable list. The latter allows for modification such as adding and removing items.
```kotlin
val immutableList = listOf("item1", "item2")
val mutableList = mutableListOf("item1", "item2")
```

#### Functions and Methods
Functions and methods are conceptually similar, however, they are defined depending on whether they are top-level functions or member functions of a class.

Taking a look at a top-level function:
```kotlin
fun greet(name: String) {
    println("Hello, $name!")
}

fun main() {
    greet("Atreus")
}
```
`Greet` is a top-level function because it is defined outside of any class. You can call it directly from anywhere in the same file or elsewhere as long as it is accessible.

Taking a look at a method:
```kotlin
class Person(val name: String) {
    fun greet() {
        println("Hello, $name!")
    }
}

fun main() {
    val person = Person("Atreus")
    person.greet()
}
```
`Greet` is a method of the `Person` class. It is called within an instance of `Person` using dot notation. Methods are associated with objects of a class and can access the properties of that object. So the main difference between functions and methods is how they are defined and accessed.

--- 

Work in progress
