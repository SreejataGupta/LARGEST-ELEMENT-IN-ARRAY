# Find Largest Element in Java

A clean, production-ready Java implementation for finding the maximum value in an integer array. This project demonstrates both traditional iterative loops and modern Java 8+ Stream approaches, complete with edge-case validation and unit tests.

---

## Features

- **Standard Iterative Loop (`O(n)` time, `O(1)` space):** Best performance and memory efficiency.
- **Java 8+ Stream API:** Modern, concise one-liner approach.
- **Robust Error Handling:** Checks for `null` or empty arrays to prevent `NullPointerException` and `ArrayIndexOutOfBoundsException`.

---

## Code Example

```java
public class FindLargestElement {

    public static void main(String[] args) {
        int[] numbers = {12, 45, 67, 23, 89, 34};

        int largest = findLargest(numbers);
        System.out.println("The largest element is: " + largest);
    }

    public static int findLargest(int[] arr) {
        if (arr == null || arr.length == 0) {
            throw new IllegalArgumentException("Array must not be null or empty.");
        }

        int max = arr[0];
        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > max) {
                max = arr[i];
            }
        }
        return max;
    }
}
