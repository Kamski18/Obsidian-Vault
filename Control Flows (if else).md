Just like python (if you already learn it), Java also has if else operators.

```java
public class Main {
	public static void main(String[] args) {
	
	int score = 75;
	
	if (score >= 90) {
		System.out.println('A');
	} else if (score >= 70) {
		System.out.println('B');
	} else if (score >= 50) {
		System.out.println('C');
	} else {
		System.out.println("Fail");
	
	}
	
	}
}
```

Java use `()` for the condition in if else, followed by `{}` for you to put actions when the condition are satisfied.

## Ternary Operator (`?:`)

The ternary operator is a shorthand way to write a simple `if-else` statement that returns a value.

```java
// Syntax: booleanCondition = condition ? valueIfTrue : valueIfFalse

int age = 25;
String status = (age >= 18) ? "Adult" : "Kiddo";

System.out.println(status)
```

