
---

# **Homework: Time Complexity and Efficiency in C++**

**Name:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
**Date:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
**Class:** \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

---

## **Part 1: Vocabulary and Definitions (Write the definitions)**

Define the following terms in your own words:

1. **Time Complexity**
   →

2. **Big-O Notation**
   →

3. **Space Complexity**
   →

4. **Linear Time – O(n)**
   →

5. **Logarithmic Time – O(log n)**
   →

---

## **Part 2: Complexity Matching (Circle the correct answer)**

Match the following code snippets with their most likely time complexity.

### A.

```cpp
for (int i = 0; i < n; i++) {
    cout << i;
}
```

* O(1)
* O(log n)
* **O(n)**
* O(n²)

---

### B.

```cpp
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        cout << i + j;
    }
}
```

* O(n)
* **O(n²)**
* O(n log n)
* O(log n)

---

### C.

```cpp
int i = n;
while (i > 1) {
    i = i / 2;
}
```

* O(n)
* O(n²)
* **O(log n)**
* O(n!)

---

### D.

```cpp
for (int i = 0; i < n; i++) {
    doSomething(); // O(1)
}
```

* O(n log n)
* **O(n)**
* O(1)
* O(n²)

---

## **Part 3: Code Analysis**

Analyze the following function. Determine the time complexity and explain your answer.

```cpp
void printSum(int n) {
    for (int i = 1; i <= n; ++i) {
        for (int j = 1; j <= i; ++j) {
            cout << i + j;
        }
    }
}
```

**What is the time complexity? Why?**
→

---

## **Part 4: Coding Problems (In C++)**

### **1. Write a function to check if a number is even. What is the time complexity?**

```cpp
bool isEven(int x) {
    // Your code here
}
```

---

### **2. Write a function to find the maximum number in an array of size `n`.**

```cpp
int findMax(int arr[], int n) {
    // Your code here
}
```

**What is the time complexity?**
→

---

### **3. Implement a simple Bubble Sort on an array of 10 elements and count the number of comparisons.**

```cpp
void bubbleSort(int arr[], int n) {
    // Your code here
}
```

**Total Comparisons Made:** \_\_\_\_\_\_\_
**What is the time complexity of Bubble Sort?**
→

---

## **Part 5: Challenge (Optional)**

Suppose a function contains the following:

```cpp
for (int i = 0; i < n; i++) {
    for (int j = i; j < n; j++) {
        cout << i << ", " << j << endl;
    }
}
```

**Q: What is the time complexity?**
→

**Bonus:** Can you improve it? 
