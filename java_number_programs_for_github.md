# Java Number Programs for GitHub

## 1. Reverse a Number
```java
import java.util.Scanner;

public class ReverseNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int rev = 0;

        while (num != 0) {
            int digit = num % 10;
            rev = rev * 10 + digit;
            num /= 10;
        }

        System.out.println("Reversed Number: " + rev);
    }
}
```

---

## 2. Palindrome Number
```java
import java.util.Scanner;

public class PalindromeNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int original = num;
        int rev = 0;

        while (num != 0) {
            rev = rev * 10 + num % 10;
            num /= 10;
        }

        if (original == rev)
            System.out.println("Palindrome Number");
        else
            System.out.println("Not a Palindrome Number");
    }
}
```

---

## 3. Armstrong Number
```java
import java.util.Scanner;

public class ArmstrongNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int original = num;
        int sum = 0;

        while (num != 0) {
            int digit = num % 10;
            sum += digit * digit * digit;
            num /= 10;
        }

        if (sum == original)
            System.out.println("Armstrong Number");
        else
            System.out.println("Not an Armstrong Number");
    }
}
```

---

## 4. Prime Number Check
```java
import java.util.Scanner;

public class PrimeNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        boolean isPrime = true;

        if (num <= 1)
            isPrime = false;

        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }

        if (isPrime)
            System.out.println("Prime Number");
        else
            System.out.println("Not a Prime Number");
    }
}
```

---

## 5. Factorial of a Number
```java
import java.util.Scanner;

public class Factorial {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        long fact = 1;

        for (int i = 1; i <= num; i++) {
            fact *= i;
        }

        System.out.println("Factorial: " + fact);
    }
}
```

---

## 6. Fibonacci Series
```java
import java.util.Scanner;

public class FibonacciSeries {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        int a = 0, b = 1;

        for (int i = 1; i <= n; i++) {
            System.out.print(a + " ");
            int temp = a + b;
            a = b;
            b = temp;
        }
    }
}
```

---

## 7. Strong Number
```java
import java.util.Scanner;

public class StrongNumber {
    static int factorial(int n) {
        int fact = 1;
        for (int i = 1; i <= n; i++) {
            fact *= i;
        }
        return fact;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int original = num;
        int sum = 0;

        while (num != 0) {
            int digit = num % 10;
            sum += factorial(digit);
            num /= 10;
        }

        if (sum == original)
            System.out.println("Strong Number");
        else
            System.out.println("Not a Strong Number");
    }
}
```

---

## 8. Perfect Number
```java
import java.util.Scanner;

public class PerfectNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int sum = 0;

        for (int i = 1; i < num; i++) {
            if (num % i == 0)
                sum += i;
        }

        if (sum == num)
            System.out.println("Perfect Number");
        else
            System.out.println("Not a Perfect Number");
    }
}
```

---

## 9. Neon Number
```java
import java.util.Scanner;

public class NeonNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int square = num * num;
        int sum = 0;

        while (square != 0) {
            sum += square % 10;
            square /= 10;
        }

        if (sum == num)
            System.out.println("Neon Number");
        else
            System.out.println("Not a Neon Number");
    }
}
```

---

## 10. Automorphic Number
```java
import java.util.Scanner;

public class AutomorphicNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int square = num * num;

        if (String.valueOf(square).endsWith(String.valueOf(num)))
            System.out.println("Automorphic Number");
        else
            System.out.println("Not an Automorphic Number");
    }
}
```

---

## 11. Harshad Number
```java
import java.util.Scanner;

public class HarshadNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int original = num;
        int sum = 0;

        while (num != 0) {
            sum += num % 10;
            num /= 10;
        }

        if (original % sum == 0)
            System.out.println("Harshad Number");
        else
            System.out.println("Not a Harshad Number");
    }
}
```

---

## 12. Sum of Digits
```java
import java.util.Scanner;

public class SumOfDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int sum = 0;

        while (num != 0) {
            sum += num % 10;
            num /= 10;
        }

        System.out.println("Sum of Digits: " + sum);
    }
}
```

---

## 13. Product of Digits
```java
import java.util.Scanner;

public class ProductOfDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int product = 1;

        while (num != 0) {
            product *= num % 10;
            num /= 10;
        }

        System.out.println("Product of Digits: " + product);
    }
}
```

---

## 14. Count Digits in a Number
```java
import java.util.Scanner;

public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int count = 0;

        while (num != 0) {
            count++;
            num /= 10;
        }

        System.out.println("Number of Digits: " + count);
    }
}
```

---

## 15. Power of a Number
```java
import java.util.Scanner;

public class PowerNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int base = sc.nextInt();
        int exponent = sc.nextInt();
        int result = 1;

        for (int i = 1; i <= exponent; i++) {
            result *= base;
        }

        System.out.println("Power: " + result);
    }
}
```

---

## 16. GCD / HCF
```java
import java.util.Scanner;

public class GCD {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }

        System.out.println("GCD: " + a);
    }
}
```

---

## 17. LCM of Two Numbers
```java
import java.util.Scanner;

public class LCM {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        int max = Math.max(a, b);

        while (true) {
            if (max % a == 0 && max % b == 0) {
                System.out.println("LCM: " + max);
                break;
            }
            max++;
        }
    }
}
```

---

## 18. Swap Two Numbers
```java
import java.util.Scanner;

public class SwapNumbers {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        int temp = a;
        a = b;
        b = temp;

        System.out.println("After Swapping: " + a + " " + b);
    }
}
```

---

## 19. Decimal to Binary
```java
import java.util.Scanner;

public class DecimalToBinary {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        System.out.println("Binary: " + Integer.toBinaryString(num));
    }
}
```

---

## 20. Binary to Decimal
```java
import java.util.Scanner;

public class BinaryToDecimal {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String binary = sc.nextLine();

        int decimal = Integer.parseInt(binary, 2);

        System.out.println("Decimal: " + decimal);
    }
}
```

---

## 21. Find ASCII Value
```java
import java.util.Scanner;

public class ASCIIValue {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        char ch = sc.next().charAt(0);

        int ascii = (int) ch;

        System.out.println("ASCII Value: " + ascii);
    }
}
```

---

## 22. Check Even or Odd
```java
import java.util.Scanner;

public class EvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        if (num % 2 == 0)
            System.out.println("Even Number");
        else
            System.out.println("Odd Number");
    }
}
```

---

## 23. Leap Year Check
```java
import java.util.Scanner;

public class LeapYear {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int year = sc.nextInt();

        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0))
            System.out.println("Leap Year");
        else
            System.out.println("Not a Leap Year");
    }
}
```

---

## 24. Nth Fibonacci Number
```java
import java.util.Scanner;

public class NthFibonacci {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        int a = 0, b = 1;

        for (int i = 2; i <= n; i++) {
            int temp = a + b;
            a = b;
            b = temp;
        }

        System.out.println("Nth Fibonacci Number: " + b);
    }
}
```

---

## 25. Trailing Zeros in Factorial
```java
import java.util.Scanner;

public class TrailingZeros {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int count = 0;

        for (int i = 5; num / i >= 1; i *= 5) {
            count += num / i;
        }

        System.out.println("Trailing Zeros: " + count);
    }
}
```

