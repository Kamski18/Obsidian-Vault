Java is a very **strongly typed** language. Every variables must be declared with specific data type. The format for making a variables is:

```
dataType variableName = value;
```

Example:
```java
int age = 25;
```

## Primitive Data Types

Java has 8 primitive data types, but only 4 are often used:

| Type    | Used For                                  | Example                      |
| ------- | ----------------------------------------- | ---------------------------- |
| int     | whole numbers                             | `int age = 25;`              |
| double  | for decimal number                        | `double price = 1.95;`       |
| char    | single character (use single quotes `''`) | `char letter = 'A';`         |
| boolean | logical true or false                     | `boolean isLoggedIn = true;` |

## References Data Types (Objects)

Unlike primitive data types that store simple values directly in memory, **references data types** store references (addresses) to complex objects.

The most common references data type is `String`, which holds text wrapped in double quotes (`""`)

```java
String name = "addin";
```

> [!IMPORTANT]
> `String` must be typed with capital `S` for Java!

## Modifying Variables

Once a variables is declared, you can change the variable without stating the data types (as long as the new value is the same as its data type)

```java
int score = 50;
score = 100; // You don't need to declare the data types anymore.
```

if you want to prevent a variable's value from changing, you can add `final` keyword to make it constant (the value is fixed and will never change)

```java
final double PI = 3.14159; // This will be a constant variable
```


## Types of variables in Java (scopes)

Where you declare the variable inside a Java program determines where it can be used:

```java
public class Example {
	// 1. INSTANCE VARIABLE (belongs to an object created from this class)
	int instanceVar = 15;
	
	// 2. STATIC VARIABLE (belongs to the class itself, shared by all instances)
	static int staticVar = 10;
	
	public void myMethod() {
	// 3. LOCAL VARIABLE (declared inside a method, exists ONLY inside this method)
	int localVar = 30;
	System.out.println(localVar);
	}

}
```

Ever wonder why I didn't put `static` in the method above? Refer to [[When to use static in method]]