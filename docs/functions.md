# Functions and Lambdas

A function is a named block of code that performs a particular task. In Kotlin, a function always returns a value

## Declaring functions

Functions in Kotlin are declared as follows

```java
  fun function_name(param1:type1,param2:type2,.... ,paramn:typen):return type

```

A quick example of a function that prints the classical , "Hello World!", will be like this;
```java
fun sayHello(){
  println("Hello World!")
}
```

The above function takes no parameters and returns type Unit.Unit is corresponds to void in Java.

Now a function that takes two parameters and returns a value demonstrated thus;

```java
fun welomeStudent(name:String,id:String):String{

    return "Welcome $name. Your student id is $id"

}

```

## Calling functions
Functions in Kotlin are called the same way like most languages.
```kotlin
<function name>(arg1,arg2,..argn)
```
Calling the above functions can be done as follows

```
    sayHello()
    welcomeStudent("John Doe","HF1234")
```

Now the beauty of Kotlin in functions come in when we can call functions using named parameters as follows,
```
    welcomeStudent(id="HF123",name="Mary Doe")

```
Imagine a functions with 20+ parameters; with Java and other languages, you must know the order in which the parameters are passed before calling the function.This is really not easy to retain. With named parameters, you don't have to know the order in which those parameters are passed.

## Functions with Single Expressions
We can write a function that does addition of two integers and return the value as follows;

```
fun add(a:Int,b:Int):Int
{
    return a+ b

}
```

The above function is a single expression function. The single expression function can be simplified further as follows.

```
fun add(a:Int,b:Int) = a + b
```
As you might have noticed, we ommitted the return type because Kotlin will automatically infer the return type to be `Int`.

## Functions with default values

Another awesome part of Kotlin is that it gives you the ability to give default values to your parameters. Let us take a real example. Say you are developing an app with two types of users, when user provides name, he/she is a regular user, but if not, they are anonymous.

```
 fun greetUser(name:String = "Anonymous user",userId:Int = 0)
    {
        println("Welcome $name. Your user id is $userId")
    }

```

The function can be called in the following ways.

```
 greetUser() // prints Welcome Anonymous user. Your userid is 0
    greetUser("Ngenge Senior")// Prints , Welcome Ngenge Senior. Your user id is 0
    greetUser(name="Romeo", userId=3) //Works as expected
    greetUser(userId=2,name="Julliet")
```

