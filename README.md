# 7.ACB-CondOp

To format the provided text for GitHub Markdown, here is how it should look:

### The Conditional Expression (Ternary Operator)

The conditional expression is the only ternary operator, i.e., an operator with three operands. It looks like this:

```java
cond ? expr1 : expr2
```

Here, `cond` is an expression of type boolean. If `cond` is true, then the value of `expr1` becomes the value of the whole expression, and `expr2` will not be evaluated. If `cond` is false, then the value of `expr2` becomes the value of the whole expression, and `expr1` is not evaluated.

```java
int mx = a > b ? a : b;
```
This initializes `mx` with the bigger of `a` and `b` values. The ternary operator resembles the `if...else` construct but is not equivalent.

**Note:** The expression `b ? e1 : e2` has a value, while `if...else` does not. For example:

```java
a > b ? System.out.print("a") : System.out.print("b"); // NO!!!
```

This doesn’t make sense because `System.out.print` has no return value.

### Listing 7 ACB-CondOp/Largest.java Page 24

```java
import java.util.Scanner;
import java.util.Locale;

public class Largest {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        scan.useLocale(Locale.US);

        System.out.print("Enter three numbers (with DOT as dec. separator!) -> ");
        var a = scan.nextDouble();
        var b = scan.nextDouble();
        var c = scan.nextDouble();

        var largest = b > a ? b : a;
        largest = c > largest ? c : largest;

        var smallest = b < a ? b : a;
        smallest = c < smallest ? c : smallest;

        System.out.println("Number " + largest + " is the largest and " + smallest + " is the smallest");
    }
}
```

This program calculates and prints the largest and smallest of three numbers entered by the user.
