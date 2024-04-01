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



#### Method

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
`greet` is a method of the `Person` class. It is called within an instance of `Person` using dot notation. Methods are associated with objects of a class and can access the properties of that object. So the main difference between functions and methods is how they are defined and accessed.

### List Indexing

When working with collections, it is important to know the concept of indexing. This refers to the position of elements within a collection. An index is a number value that indicates the position of an element. Indexing allows one to access, modify, and remove elements in lists and arrays.

Indexing starts from 0, and the last index of a collection is the size of the collection minus 1.

#### Accessing Elements

You can access an element in a list by referring to its index.

```kotlin
val element = shoppingList[index]
```

For example:

```kotlin
val shoppingList = listOf("apple", "strawberries", "banana")
println(myList[1]) // This gives an output of strawberries
```

### Adding/Removing/Replacing Items to a List

Standard lists are immutable and cannot be changed, so you need to use a mutable list (`MutableList`) in order to modify content.

#### Adding an Item

```kotlin
val mutableList = mutableListOf("CPU", "GPU", "RAM")
mutableList.add("date")
```

#### Removing an Item

```kotlin
mutableList.remove("RAM")
mutableList.removeAt(0) // This would remove the "CPU"
```

#### Replacing an Item

```kotlin
mutableList[1] = "Power supply" // This replaces the GPU with a power supply.
```

### The `set` Method

The `set` method is used with mutable lists to replace an item at a specific position or index. The syntax requires you to use two parameters: the index in which the item needs to be replaced and the new value.

```kotlin
mutableList.set(index, element)
```

Imagine you have a mutable list of computer parts and you would like to replace one of the parts.

```kotlin
val mutableList = mutableListOf("AMD 5800x", "RTX 4080", "Seasonic PSU")
mutableList.set(2, "Corsair PSU") // The Seasonic PSU is replaced
```

### For Loops

Work in progress
