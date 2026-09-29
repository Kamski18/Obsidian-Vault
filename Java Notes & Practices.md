Java used to build secure, high-performances applications that run on everything from small devices to large cloud servers. In this language, we call method as **method**. Method is a method that is inside a class.

## Quick start

```java
public class Main {
	public static void main(String[] args) {
		System.out.println("Hello Java");
	}
}
```

> [!IMPORTANT]
> For the code block above, the method is named as `Main`. Therefore, it is a MUST to name the file as `Main.java`

you NEED to put semicolon `;` when:
- Variables declaration and assignments
- Method calls and actions
- Control flow keywords like `return` or `break`

```java
// variables declaration and assignments
int age = 25;
String name = "addin";

// Method calls and actions
System.out.println("Hello Java");
counter.increment();

// Control flow keywords
return true;
break;
```

THAT'S IT.
## Explanations

```java
public class Main {}
```

`public` (Access Modifier)

- Makes the class accessible from anywhere in your project. (You can import this class to another file ~~like python.~~)
- when you use this, you need to name the file the same name as the class name.

`class` (Keyword)

- Everything in Java revolve around class.
- Declares a new blueprint (class) so you can put your method or variables in the class.

`Main` (Identifier)

- The name of the class (you can name it however you want it)
- By standard Java naming conventions, class name use **PascalCase** (capitalizing first letter of each word)

`{}` (curly braces)

- Defines the body of the class
- All variables, method, and logic associated with the class go inside the curly braces.

```java
	public static void main(String[] args) {}
```

`static` (Keyword)

Class is just a blueprint, not the object itself. in order for you to use it is to make an instance (or object, both **almost** the same). But `static` allow us to use the class directly without making an instance.

Example given (Focus on the differences of this two code block):

```java
public class Printer {
	// Notice I didn't use static (Non-static method / method)
	public void printMessage() {
		System.out.println("Hello Java");
	}
	
	public static void main(String[] args) {
	// You need to use the class first to create an object
	// format: class instanceName = new class()
	
	// this will create an instance in memory
	Printer myPrinter = new Printer();
	
	// now you NEED to use the instance in order to call the method.
	myPrinter.printMessage();
	}
	
}
```

Now lets look at this one

```java
public class Printer {
	// I USE STATIC IN THIS METHOD
	public static void printMessage() {
		System.out.println("Hello Java");
	}
	
	public static void main(String[] args) {
		// Now, you can just call the method directly. NO NEED TO CREATE AN INSTANCE.
		printMessage();
		
		// OR You can call it using the class name.
		Printer.printMessage();
	}
}
```

Basically `static` make things easier.

`void` (Return Type)

- Indicates that this method won't return any value at all.

`main` (method name)

- The exact name that the JVM looks for.

> [!NOTES]
> JVM (Java Virtual Machine) an abstract computing engine that converts Java bytecode into native machine instructions for your computer.

- You need to have main method in every **starter** class.
- It must named as `main` with the lowercase and the exact word.
- Not every class need main method, only for starter classes.

> [!NOTES]
> `Starter Classes` is classes that your program will run first. This class will have other classes in it for the program to use.


`String[] args` (Parameter)

- An array (`[]`) of sequence of characters (`String`) passed to your program as **command-line arguments**.
- It allows users or terminal commands to pass inputs directly into your application when launching it.

Example Given:

```bash
java Main apple banana durian
```

This words will be passed to the method:

```java
public class Main {
	public static void main(String[] args) {
	// Most language including Java start counting from 0 so:
	// args[0] = "apple"
	// args[1] = "banana"
	// args[2] = "durian"
	
	// you can then use the args passed as you like.
	
	System.out.println("First argument passed: " + args[0])
	
	// output - First argument passed: apple
	}
}
```



```java
System.out.println("hello Java");
```

`System` (Class)

- Yes, System is a built in standard Java class provided by the core Java library (`java.lang` package) that gives you access to system-level features like screen output, keyboard input, and environment variables.

`.out` (Static Field)

- a pre-created `static` variable inside the `System` class that represent **the standard output stream** (by default your IDE, terminal)
- Because it is `static`, you can access it directly via `System.out` without creating a `new System()` object. - refer `static` explanation.

`.println()` (Method)

- Short term for "**print line**". It takes whatever inside the parentheses, outputs it to the console, and automatically moves the cursor to a **new line** below it. (yes looks basic but this is all need to be done manually if using low level language.) 

`"Hello Java"` (Argument)

- the actual text (a `String` in Java) that you want to display. Strings in java **MUST** be wrapped with `"` (double quotes).

> [!NOTES]
> `""` are used for `String` while `''` are used for chars

[[Variables]]
[[Control Flows (if else)]]
