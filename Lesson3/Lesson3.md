---

# **Lesson: Time Complexity and Efficiency in C++**

## **Objective:**

Understand how to measure and analyze the efficiency of programs using time complexity notation (`O(n)`), compare algorithm speeds, and learn how to apply these concepts when writing and analyzing C++ code.

---

## **1. What is Time Complexity?**

**Definition:**
Time complexity is a way to describe the amount of time an algorithm takes to run, in terms of the size of its input.

* It is not measured in seconds, but rather in terms of **operations**.
* We use **Big-O notation** to express the upper bound (worst-case scenario) of an algorithm’s running time.

---

## **2. Big-O Notation**

| Notation     | Name                    | Example Use Case                      | Speed               |
| ------------ | ----------------------- | ------------------------------------- | ------------------- |
| O(1)         | Constant Time           | Accessing an array element            | Fastest             |
| O(log n)     | Logarithmic Time        | Binary search                         | Very fast           |
| O(n)         | Linear Time             | Single loop through data              | Acceptable          |
| O(n log n)   | Linearithmic Time       | Efficient sorting (merge sort)        | Good for large data |
| O(n²)        | Quadratic Time          | Nested loops                          | Slow                |
| O(2ⁿ), O(n!) | Exponential / Factorial | Recursive backtracking / permutations | Very slow           |

---

## **3. Why Does Efficiency Matter?**

### Example:

* Sorting 10 elements with `O(n²)` may be fast.
* Sorting 100,000 elements with `O(n²)` can be painfully slow.
* Instead, using an `O(n log n)` algorithm like **merge sort** is necessary.

---

## **4. How to Analyze Time Complexity**

### Basic Rules:

1. **Loops**

   * `for (int i = 0; i < n; ++i)` → O(n)
   * Nested: `for (int i = 0; i < n; ++i) for (int j = 0; j < n; ++j)` → O(n²)

2. **Sequential Statements**

   * Two loops one after another → O(n + n) = O(n)

3. **Recursive Calls**

   * `f(n) = 2 * f(n/2)` → O(n)
   * `f(n) = f(n - 1) + f(n - 2)` (Fibonacci) → O(2ⁿ)

4. **Function Calls**

   * Time complexity adds up based on how often the function is called.

---

## **5. Real C++ Examples**

### Example 1: O(n)

```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 100;
    for (int i = 0; i < n; ++i) {
        cout << i << " ";
    }
    return 0;
}
```

### Example 2: O(n²)

```cpp
int main() {
    int n = 100;
    for (int i = 0; i < n; ++i) {
        for (int j = 0; j < n; ++j) {
            cout << i << "," << j << endl;
        }
    }
    return 0;
}
```

### Example 3: O(log n) - Binary Search

```cpp
int binarySearch(int arr[], int left, int right, int x) {
    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (arr[mid] == x)
            return mid;
        else if (arr[mid] < x)
            left = mid + 1;
        else
            right = mid - 1;
    }
    return -1;
}
```

---

## **6. Common Misconceptions**

* `O(n)` does NOT mean exactly n steps.
* `O(n²)` does NOT always mean “bad” – it's just slow for large `n`.
* Focus is on how runtime **grows** with input size.

---

## **7. Space Complexity**

**Definition:**
Measures how much extra memory an algorithm uses.

* Like time complexity, it uses Big-O.
* Example: Using an array of size `n` → O(n) space.

---

## **8. Practice Questions**

### **A. Fill in the complexity**

Match the code with its time complexity:

1. Single `for` loop from 0 to n
2. Nested `for` loops from 0 to n
3. `while (n > 0) { n /= 2; }`
4. `for (int i = 0; i < n; i++) cout << i;` followed by another same loop
5. Triple nested loop

**Choices:**
O(n), O(log n), O(n log n), O(n²), O(n³), O(2ⁿ)

---

### **B. Analyze the following code:**

```cpp
int sum = 0;
for (int i = 1; i <= n; ++i) {
    for (int j = 1; j <= i; ++j) {
        sum += j;
    }
}
```

**Q:** What is the time complexity?

---

## **9. Challenge Coding Problems**

### Problem 1: Constant Time Check

Write a function that checks if a number is even. Analyze its time complexity.

---

### Problem 2: Find Maximum Element (Linear Time)

Write a function that takes an array and returns the largest number.

---

### Problem 3: Sort Efficiency Comparison

Implement Bubble Sort and compare its runtime with `std::sort()` for 10,000 elements.

---

## **10. Summary**

* Time complexity helps predict performance.
* Big-O notation gives an upper-bound estimate.
* Efficient algorithms scale better with large input sizes.
* Understand `O(1)`, `O(n)`, `O(n log n)`, `O(n²)`, `O(2ⁿ)` patterns.
