# Speed running this section xd

## First program

```kotlin
fun main() {
    println("Hello, Android!")
}
```

Kotlin needs a main function as the entry point of the program.

They immediately introduce style guides available here: <https://developer.android.com/kotlin/style-guide>

They include:

- The name of a function should follow camel case convention and start with a lowercase letter.
- Spaces in the function name declaration
- 4 space indent
- vertical alignment of curly brackets

## Variables

### Types and declaration

Types in Kotlin:

- String
- Int
- Double
- Float
- Boolean (true, false, in lowercase)

For specifics in numerical data types see <https://kotlinlang.org/docs/numbers.html>. 

For declaring a variable you need a name and a data type, a name and an initial value (using type inference), or the three (a name, a data type and an initial value).

```kotlin
fun main() {
    val count: Int = 2
    println(count)
}
```

Variables names also use camel case.

### String templates

To print variables, we can use a string template:

```kotlin
fun main() {
    val count: Int = 10
    println("You have $count unread messages.")
}
```

String templates can also be used to do operation:

```kotlin
fun main() {
    val unreadCount = 5
    val readCount = 100
    println("You have ${unreadCount + readCount} total messages in your inbox.")
}
```

### Constants

`val` is immutable (constant), to mute a variable value we use `var`:

```kotlin
fun main() {
    var cartTotal = 0
    println("Total: $cartTotal")

    cartTotal = 20
    println("Total: $cartTotal")
}
```

For more info an Constants, see <https://developer.android.com/kotlin/style-guide#constant_names>.

### Increment and decrement operators

We use these operators (`++` and `--`) as suffix operators:

```kotlin
fun main() {
    var count = 10
    println("You have $count unread messages.")
    count++
    println("You have $count unread messages.")
}
```

In this case `count++` is equivalent to `count = count + 1`.

### Other data types

Usual stuff. Adding floats and doubles, concatenating strings, escape sequence character, using bools.

```kotlin
fun main() {
    val trip1: Double = 3.20
    val trip2: Double = 4.10
    val trip3: Double = 1.72
    val totalTripLength: Double = trip1 + trip2 + trip3
    println("$totalTripLength miles left to destination")
}
```


```kotlin
fun main() {
    val nextMeeting = "Next meeting: "
    val date = "January 1"
    val reminder = nextMeeting + date + " at \"work\""
    println(reminder)
}
```

```kotlin
fun main() {
    val notificationsEnabled: Boolean = false
    println("Are notifications enabled? " + notificationsEnabled)
}
```


### Comments

```kotlin
// This is a comment

/*
 * This is a long comment
 * Not that long but longer
 */
```


## Functions

We have used two functions `main()` and `println()`. `main` is the entry point so we dont call it any where, it is used to include other code we want to execute.

A simple example:

```kotlin
fun main() {
    birthdayGreeting()
}

fun birthdayGreeting(): Unit {
    println("Happy Birthday, Rover!")
    println("You are now 5 years old!")
}
```

### Return values

Functions can return values. The default return type is `Unit` which is equivalent to `void` or `None`.

To return other type, we need to use that type and a return statement:

```kotlin
fun main() {
    val greeting = birthdayGreeting()
    println(greeting)
	 // or println(birthdayGreeting())
}

fun birthdayGreeting(): String {
    val nameGreeting = "Happy Birthday, Rover!"
    val ageGreeting = "You are now 5 years old!"
    return "$nameGreeting\n$ageGreeting"
}
```

### Parameters

When using `println()` we give an argument to the function, we pass a value.

A parameter specifies a name and a data type that can be passed to the function and accessed inside.

```kotlin
fun main() {
    println(birthdayGreeting("Rover"))
	 println(birthdayGreeting("Rex"))
}

fun birthdayGreeting(name: String): String {
    val nameGreeting = "Happy Birthday, $name!"
    val ageGreeting = "You are now 5 years old!"
    return "$nameGreeting\n$ageGreeting"
}
```

Parameters in kotlin are immutable.

```kotlin
fun main() {
    println(birthdayGreeting("Rover", 5))
    println(birthdayGreeting("Rex", 2))
}

fun birthdayGreeting(name: String, age: Int): String {
    val nameGreeting = "Happy Birthday, $name!"
    val ageGreeting = "You are now $age years old!"
    return "$nameGreeting\n$ageGreeting"
}
```

The function name with its inputs (parameters) are collectively known as the function signature.

When calling a function, we can also use named parameters: `println(birthdayGreeting(name = "Rex", age = 2))` or `println(birthdayGreeting(age = 2, name = "Rex"))`.

Also, parameters can have default arguments (values).

```kotlin
fun birthdayGreeting(name: String = "Rover", age: Int): String {
    return "Happy Birthday, $name! You are now $age years old!"
}
```

If a default argument is given, the parameter can be omitted when calling the function.

