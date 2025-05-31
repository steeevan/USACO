
# 📚 Homework: Introduction to Data Structures in C++

## ✍️ Section A: Short Answer (Answer in 1–2 sentences)

1. **What is the difference between a static array and a vector in C++?**
2. **When would you use a `pair` instead of two separate variables?**
3. **Explain one advantage of using STL containers like `vector` or `tuple`.**
4. **Why is `memset()` unsafe for setting values other than 0 or -1?**
5. **What does this loop print?**

```cpp
vector<int> v = {1, 2, 3};
for (int x : v) cout << x * 2 << " ";
```

---

## 💻 Section B: Code Practice (Write and run in your IDE)

### 1. **Initialize and Print**

Write a program that:

* Asks the user for a number `n`
* Creates a vector of size `n` initialized to `0`
* Changes every value to `i * 2` (where `i` is the index)
* Prints the vector

```cpp
// Your code here:
```

---

### 2. **Working with Strings and Loops**

Write a program that:

* Takes a string from the user
* Counts how many vowels are in the string
* Prints the number of vowels

```cpp
// Your code here:
```

---

### 3. **Pair Practice**

Create a list of 3 `pair<int, string>` representing a student ID and name.

Then print each student's ID and name.

```cpp
// Your code here:
```

---

## 🧠 Section C: Logic and Tracing

### 1. What will the following code output?

```cpp
vector<int> nums = {5, 10, 15};
nums.erase(nums.begin() + 1);
for (int n : nums) cout << n << " ";
```

**Answer:** ___________________________________

---

### 2. What is printed?

```cpp
tuple<int, string, double> t = make_tuple(3, "data", 7.2);
int x; string y; double z;
tie(x, y, z) = t;
cout << y << " " << z;
```

**Answer:** ___________________________________

---

## 🎯 Section D: Challenge – Brute Force Search

Write a complete program that:

* Searches for all 2-digit numbers where the **sum of the digits equals 10**
* Prints each number found

Example Output:

```
19
28
...
```

```cpp
// Your code here:
```

---

## ✅ Submission Checklist

* [ ] Short answers written clearly
* [ ] All code segments completed
* [ ] Challenge program written and tested
* [ ] Code runs without errors
