# Java Array and String Programs

## 26. Find Largest Element in an Array

```java
/*
Program: Find Largest Element in an Array

Explanation:
1. The user enters the size of the array.
2. The user enters all array elements.
3. Assume the first element is the largest.
4. Compare each element with the largest value.
5. If a bigger element is found, update the largest value.
6. Finally, print the largest element.
*/

import java.util.Scanner;

public class LargestElement {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int largest = arr[0];

        for(int i = 1; i < n; i++) {
            if(arr[i] > largest) {
                largest = arr[i];
            }
        }

        System.out.println("Largest element is: " + largest);
    }
}
```

---

## 27. Find Smallest Element in an Array

```java
/*
Program: Find Smallest Element in an Array

Explanation:
1. Read array size and elements from the user.
2. Assume the first element is the smallest.
3. Compare all elements with the smallest value.
4. If a smaller element is found, update it.
5. Print the smallest element.
*/

import java.util.Scanner;

public class SmallestElement {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int smallest = arr[0];

        for(int i = 1; i < n; i++) {
            if(arr[i] < smallest) {
                smallest = arr[i];
            }
        }

        System.out.println("Smallest element is: " + smallest);
    }
}
```

---

## 28. Second Largest Element in an Array

```java
/*
Program: Find Second Largest Element

Explanation:
1. Take array input from the user.
2. Store two variables:
   - largest
   - secondLargest
3. Compare elements one by one.
4. Update largest and secondLargest values.
5. Print the second largest element.
*/

import java.util.Scanner;

public class SecondLargest {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int largest = Integer.MIN_VALUE;
        int secondLargest = Integer.MIN_VALUE;

        for(int i = 0; i < n; i++) {

            if(arr[i] > largest) {
                secondLargest = largest;
                largest = arr[i];
            }
            else if(arr[i] > secondLargest && arr[i] != largest) {
                secondLargest = arr[i];
            }
        }

        System.out.println("Second largest element is: " + secondLargest);
    }
}
```

---

## 29. Second Smallest Element in an Array

```java
/*
Program: Find Second Smallest Element

Explanation:
1. Read array elements from the user.
2. Store smallest and secondSmallest values.
3. Compare elements carefully.
4. Update smallest and secondSmallest.
5. Print second smallest element.
*/
import java.util.Scanner;

public class SecondSmallest {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        int smallest = Integer.MAX_VALUE;
        int secondSmallest = Integer.MAX_VALUE;

        for(int i = 0; i < n; i++) {

            if(arr[i] < smallest) {
                secondSmallest = smallest;
                smallest = arr[i];
            }
            else if(arr[i] < secondSmallest && arr[i] != smallest) {
                secondSmallest = arr[i];
            }
        }

        System.out.println("Second smallest element is: " + secondSmallest);
    }
}
```

---

## 30. Reverse an Array

```java
/*
Program: Reverse an Array

Explanation:
1. Read array elements from the user.
2. Traverse the array from last index to first.
3. Print elements in reverse order.
*/
import java.util.Scanner;

public class ReverseArray {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.println("Reversed array:");

        for(int i = n - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
    }
}
```

---

## 31. Sort Array in Ascending Order

```java
/*
Program: Sort Array in Ascending Order

Explanation:
1. Read array elements from the user.
2. Compare elements using nested loops.
3. Swap elements when needed.
4. Print the array in ascending order.
*/
import java.util.Scanner;

public class AscendingSort {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        for(int i = 0; i < n; i++) {
            for(int j = i + 1; j < n; j++) {

                if(arr[i] > arr[j]) {

                    int temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }

        System.out.println("Ascending order:");

        for(int num : arr) {
            System.out.print(num + " ");
        }
    }
}
```

---

## 32. Sort Array in Descending Order

```java
/*
Program: Sort Array in Descending Order

Explanation:
1. Read array elements.
2. Compare elements using nested loops.
3. Swap elements when needed.
4. Print the array in descending order.
*/
import java.util.Scanner;

public class DescendingSort {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        for(int i = 0; i < n; i++) {
            for(int j = i + 1; j < n; j++) {

                if(arr[i] < arr[j]) {

                    int temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }

        System.out.println("Descending order:");

        for(int num : arr) {
            System.out.print(num + " ");
        }
    }
}
```

---

## 33. Sum of Array Elements

```java
/*
Program: Find Sum of Array Elements

Explanation:
1. Read array elements from the user.
2. Initialize sum as 0.
3. Add all elements to sum.
4. Print the total sum.
*/
import java.util.Scanner;

public class SumArray {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        int sum = 0;

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            sum += arr[i];
        }

        System.out.println("Sum of elements is: " + sum);
    }
}
```

---

## 34. Average of Array Elements

```java
/*
Program: Find Average of Array Elements

Explanation:
1. Read array elements.
2. Find the total sum.
3. Divide sum by number of elements.
4. Print the average.
*/
import java.util.Scanner;

public class AverageArray {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        int sum = 0;

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            sum += arr[i];
        }

        double average = (double) sum / n;

        System.out.println("Average is: " + average);
    }
}
```

---

## 35. Find Duplicate Elements in an Array

```java
/*
Program: Find Duplicate Elements

Explanation:
1. Read array elements from the user.
2. Compare each element with remaining elements.
3. If duplicate is found, print it.
*/
import java.util.Scanner;

public class DuplicateElements {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.println("Duplicate elements are:");

        for(int i = 0; i < n; i++) {

            for(int j = i + 1; j < n; j++) {

                if(arr[i] == arr[j]) {
                    System.out.print(arr[i] + " ");
                    break;
                }
            }
        }
    }
}
```

---

## 36. Remove Duplicates from Array

```java
/*
Program: Remove Duplicate Elements

Explanation:
1. Read array elements.
2. Compare elements using nested loops.
3. Store only unique elements.
4. Print array without duplicates.
*/
import java.util.Scanner;

public class RemoveDuplicates {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        System.out.println("Array after removing duplicates:");

        for(int i = 0; i < n; i++) {

            boolean isDuplicate = false;

            for(int j = 0; j < i; j++) {

                if(arr[i] == arr[j]) {
                    isDuplicate = true;
                    break;
                }
            }

            if(!isDuplicate) {
                System.out.print(arr[i] + " ");
            }
        }
    }
}
```

---

## 37. Frequency of Elements in an Array

```java
/*
Program: Find Frequency of Elements

Explanation:
1. Read array elements.
2. Count how many times each element appears.
3. Print frequency of every element.
*/
import java.util.Scanner;

public class FrequencyElements {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter array size: ");
        int n = sc.nextInt();

        int[] arr = new int[n];
        boolean[] visited = new boolean[n];

        System.out.println("Enter array elements:");

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        for(int i = 0; i < n; i++) {

            if(visited[i]) {
                continue;
            }

            int count = 1;

            for(int j = i + 1; j < n; j++) {

                if(arr[i] == arr[j]) {
                    count++;
                    visited[j] = true;
                }
            }

            System.out.println(arr[i] + " occurs " + count + " times");
        }
    }
}
```

---

## 38. Missing Number in Array

```java
/*
Program: Find Missing Number in Array

Explanation:
1. Array contains numbers from 1 to n with one missing number.
2. Find expected sum using formula.
3. Find actual sum of array elements.
4. Difference gives missing number.
*/
import java.util.Scanner;

public class MissingNumber {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();

        int[] arr = new int[n];

        System.out.println("Enter array elements:");

        int actualSum = 0;

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
            actualSum += arr[i];
        }

        int expectedSum = (n + 1) * (n + 2) / 2;

        int missing = expectedSum - actualSum;

        System.out.println("Missing number is: " + missing);
    }
}
```

---

## 39. Merge Two Arrays

```java
/*
Program: Merge Two Arrays

Explanation:
1. Read first array elements.
2. Read second array elements.
3. Create a new array with combined size.
4. Store elements of both arrays.
5. Print merged array.
*/
import java.util.Scanner;

public class MergeArrays {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter size of first array: ");
        int n1 = sc.nextInt();

        int[] arr1 = new int[n1];

        System.out.println("Enter first array elements:");

        for(int i = 0; i < n1; i++) {
            arr1[i] = sc.nextInt();
        }

        System.out.print("Enter size of second array: ");
        int n2 = sc.nextInt();

        int[] arr2 = new int[n2];

        System.out.println("Enter second array elements:");

        for(int i = 0; i < n2; i++) {
            arr2[i] = sc.nextInt();
        }

        int[] merged = new int[n1 + n2];

        for(int i = 0; i < n1; i++) {
            merged[i] = arr1[i];
        }

        for(int i = 0; i < n2; i++) {
            merged[n1 + i] = arr2[i];
        }

        System.out.println("Merged array:");

        for(int num : merged) {
            System.out.print(num + " ");
        }
    }
}
```

---

## 51. Reverse a String

```java
/*
Program: Reverse a String

Explanation:
1. Read string input from the user.
2. Traverse the string from last character to first.
3. Store characters in reverse order.
4. Print reversed string.
*/
import java.util.Scanner;

public class ReverseString {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        String reverse = "";

        for(int i = str.length() - 1; i >= 0; i--) {
            reverse += str.charAt(i);
        }

        System.out.println("Reversed string is: " + reverse);
    }
}
```

---

## 52. Palindrome String

```java
/*
Program: Check Palindrome String

Explanation:
1. Read string from the user.
2. Reverse the string.
3. Compare original and reversed string.
4. If both are same, it is palindrome.
*/
import java.util.Scanner;

public class PalindromeString {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        String reverse = "";

        for(int i = str.length() - 1; i >= 0; i--) {
            reverse += str.charAt(i);
        }

        if(str.equals(reverse)) {
            System.out.println("Palindrome String");
        }
        else {
            System.out.println("Not a Palindrome String");
        }
    }
}
```

---

## 53. Count Vowels and Consonants

```java
/*
Program: Count Vowels and Consonants

Explanation:
1. Read string input from the user.
2. Check every character.
3. Count vowels and consonants separately.
4. Print both counts.
*/
import java.util.Scanner;

public class VowelsConsonants {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = sc.nextLine().toLowerCase();

        int vowels = 0;
        int consonants = 0;

        for(int i = 0; i < str.length(); i++) {

            char ch = str.charAt(i);

            if(ch >= 'a' && ch <= 'z') {

                if(ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
                    vowels++;
                }
                else {
                    consonants++;
                }
            }
        }

        System.out.println("Vowels = " + vowels);
        System.out.println("Consonants = " + consonants);
    }
}
```

---

## 54. Remove Spaces from String

```java
/*
Program: Remove Spaces from String

Explanation:
1. Read string input from the user.
2. Use replace() method to remove spaces.
3. Print updated string.
*/
import java.util.Scanner;

public class RemoveSpaces {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        String result = str.replace(" ", "");

        System.out.println("String after removing spaces:");
        System.out.println(result);
    }
}
 ```
## left rotate array
```java
import java.util.*;
class Main {
    public static void main(String[] args) {
        Scanner s=new Scanner(System.in);
        int n=s.nextInt();
        int[] a=new int[n];
        for(int i=0;i<n;i++){
            a[i]=s.nextInt();
        }
        
        int temp=a[0];
        for(int i=1;i<n;i++){
            a[i-1]=a[i];
        }
        a[n-1]=temp;
        for(int i=0;i<n;i++){
            System.out.println(a[i]);
        }
    }
}
```
### moves zeroes to the end
```java
import java.util.*;
class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int[] a = new int[n];

        for (int i = 0; i < n; i++) {
            a[i] = s.nextInt();
        }
        int left = 0;
        for (int right = 0; right < n; right++) {
            if (a[right] != 0) {
                int temp = a[left];
                a[left] = a[right];
                a[right] = temp;
                left++;
            }
        }
        for (int i = 0; i < n; i++) {
            System.out.print(a[i] + " ");
        }
    }
}
```
## right rotate array

```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        int n = s.nextInt();
        int[] a = new int[n];

        for (int i = 0; i < n; i++) {
            a[i] = s.nextInt();
        }

        int temp = a[n - 1];

        for (int i = n - 1; i > 0; i--) {
            a[i] = a[i - 1];
        }

        a[0] = temp;

        for (int i = 0; i < n; i++) {
            System.out.print(a[i] + " ");
        }
    }
}
```


##linear search
```java
import java.util.*;

class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int p=s.nextInt();
        int[] a = new int[n];
        for (int i = 0; i < n; i++) {
            a[i] = s.nextInt();
        }
        boolean flag=false;
        for (int i = 0; i < n; i++) {
            if(a[i]==p){
               flag=true; 
            }
        }
        if(flag){
            System.out.println("found");
        }
        else{
            System.out.println("not found");
        }
    }
}
```
