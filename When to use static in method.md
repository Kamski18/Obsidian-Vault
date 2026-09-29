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

In this example, I wonder why this method doesn't have `static` in it?

`myMethod()` is intentionally written as **instance method** (non-static) to match `instanceVar`.
### The Fundamental Rule
- **Non-static methods** can access both instance variables (`instanceVar`)  and static variables (`staticVar`)
- **Static methods** can **ONLY** access static variables (`staticVar`). They cannot touch instance variables directly.

## If I DID NOT use static

Because `myMethod()` is non-static, it can access `instanceVar, staticVar`, and its own local variables without any issues:

```java
public class Example {
	int instanceVar = 15;
	static staticVar = 10;
	
	// NON-STATIC METHOD
	public void myMethod() {
	int localvar = 30;
	
	System.out.println(instanceVar); // Allowed
	System.out.println(staticVar);  // Allowed
	System.out.println(localVar);  // Allowed
	}
}
```

However, to call this method, you need to create an object first:

```java
Example obj = new Example();
obj.myMethod();
```


## If I DID use static

If you add `static` to the method signature:

```java
public class Example() {
	int instanceVar = 15;
	static int staticVar = 10;
	
	public static void myMethod() {
		int localVar = 30;
		
		System.out.println(instanceVar) // COMPILED ERROR
		System.out.println(staticVar)  // ALLOWED
		System.out.println(localVar)  // ALLOWED
	}
}
```

The Java compiler will return an error:

```bash
Non-static variable instanceVar cannot be referenced from a static context
```

## Why?

`instanceVar` only exist when an object is built with `new Example()`. However `static` methods exist independently of any object. `static` methods belongs to the class rather than to a specific object instance created (`new Example()`). so the Java compiler will ask the what is the object of this variable?

That is why `static int staticVar = 15;` exists. so that you can use static in the method and don't have to make an object in order for the methods to work.