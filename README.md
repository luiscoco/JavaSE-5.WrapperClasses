# JavaSE-5.WrapperClasses

In Java, a wrapper class is a class that encapsulates types, converting them into objects.

The eight primitive data types in Java—int, char, float, double, boolean, byte, short, and long—all have corresponding wrapper classes. Here are the wrapper classes:

Integer: for int
Character: for char
Float: for float
Double: for double
Boolean: for boolean
Byte: for byte
Short: for short
Long: for long

Here's a quick example of using Integer as a wrapper class for the primitive type int:

```java
public class WrapperExample {
    public static void main(String[] args) {
        // Primitive data type
        int primitiveInt = 42;

        // Using Integer wrapper class
        Integer wrappedInt = Integer.valueOf(primitiveInt);

        // Auto-boxing (converting int to Integer implicitly)
        Integer autoBoxedInt = primitiveInt;

        // Unboxing (converting Integer to int explicitly)
        int unboxedInt = wrappedInt.intValue();

        System.out.println("Primitive int: " + primitiveInt);
        System.out.println("Wrapped Integer: " + wrappedInt);
        System.out.println("Auto-boxed Integer: " + autoBoxedInt);
        System.out.println("Unboxed int: " + unboxedInt);
    }
}
```

In this example:

Integer.valueOf(primitiveInt) is explicitly creating an Integer object from a primitive int.

Integer is a wrapper class for the primitive type int.

Auto-boxing is the process of converting a primitive type to its corresponding wrapper class implicitly.

Unboxing is the process of converting a wrapper class object to its primitive type explicitly.

Wrapper classes are useful when you need to treat primitive types as objects. They also provide utility methods for converting between primitive types and strings, among other things.

### Autoboxing

Definition: Autoboxing is the automatic conversion of a primitive type to its corresponding wrapper class object.

Example:

```java
int primitiveInt = 42;
Integer wrappedInt = primitiveInt; // Autoboxing
```

### Unboxing

Definition: Unboxing is the reverse process, where the value of a wrapper class object is automatically converted to its corresponding primitive type.

Example:

```java
Integer wrappedInt = 42;
int primitiveInt = wrappedInt; // Unboxing
```

### Object Immutability:

Immutability refers to the state of an object that cannot be modified after it is created.

### Wrapper Classes and Immutability

Wrapper classes, such as Integer, Double, etc., are immutable in Java.

Once an Integer object is created, its value cannot be changed.

Methods like intValue() in Integer class do not modify the existing object but return a new primitive value.

Example:

```java
Integer immutableInt = 42;
// Attempting to modify the value will result in a compilation error
// immutableInt = 43; // Compilation error
```

### Why Immutability?

Immutability ensures that the state of an object remains constant, which can simplify code and make it more predictable.

Immutable objects are thread-safe since their state cannot be changed by multiple threads.

### Operations on Immutable Objects

Operations on immutable objects often return a new object with the modified value, leaving the original object unchanged.

Example with Immutability:

```java
Integer originalInt = 42;
Integer modifiedInt = originalInt + 10; // Creates a new Integer object with the result
System.out.println(originalInt); // Still prints 42
```

Understanding autoboxing, unboxing, and object immutability is crucial, especially when working with wrapper classes and designing code that involves both primitive types and their corresponding objects.
