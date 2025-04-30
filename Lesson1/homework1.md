

### 🟩 **Problem 1: Calculate Perimeter of a Rectangle**

 **Task** :

Write a program that asks the user to input the width and height of a rectangle, and then prints the perimeter.

 **Formula** :

Perimeter = 2 × (width + height)

**Example Input:**

```
Width: 7  
Height: 3
```

**Example Output:**

```
Perimeter: 20
```

---

### 🟩 **Problem 2: Time Until Midnight**

 **Task** :

Ask the user to enter the current time in hours and minutes (24-hour format), and output how many hours and minutes remain until midnight.

**Example Input:**

```
Hour: 22  
Minute: 15
```

**Example Output:**

```
Time until midnight: 1 hour(s) and 45 minute(s)
```

 **Hint** :

There are 1440 total minutes in a day. Convert the input time to minutes, subtract, then convert back to hours and minutes.

---

### 🟩 **Problem 3: Motivational Milk Display**

🧠 Based on the official USACO Bronze problem:

📎 [https://usaco.org/index.php?page=viewproblem2&amp;cpid=761](https://usaco.org/index.php?page=viewproblem2&cpid=761)

Farmer John purchases three cows: Bessie, Elsie, and Mildred, each of whom initially produces 7 gallons of milk per day. Since the milk output of a cow is known to potentially change over time, Farmer John takes periodic measurements over the next 100 days and scribbles them down in a log book. Entries in his log look like this:

```
35 Bessie -2  
14 Mildred +3
```

The first entry indicates that on day 35, Bessie's milk output was 2 gallons lower than it was when last measured. The next entry indicates that on day 14, Mildred's milk output increased by 3 gallons from when it was last measured.

Farmer John has only enough time to make at most one measurement on any given day. Unfortunately, he is a bit disorganized, and doesn't necessarily write down his measurements in chronological order.

To keep his cows motivated, Farmer John proudly displays on the wall of his barn the picture of whichever cow currently has the highest milk output (if several cows tie for the highest milk output, he displays all of their pictures). Please determine the number of days on which Farmer John would have needed to change this display.

**INPUT FORMAT (`measurement.in`):**

* First line: `N` (number of measurements, 1 ≤ N ≤ 100)
* Next `N` lines: each contains

  `day cow_name change`

  Example: `35 Bessie -2`

**OUTPUT FORMAT (`measurement.out`):**

* One integer: number of days the motivational display changes

**SAMPLE INPUT:**

```
4  
7 Mildred +3  
4 Elsie -1  
9 Mildred -1  
1 Bessie +2
```

**SAMPLE OUTPUT:**

```
3
```

**Explanation:**

* Day 1: Bessie increases to 9 → display changes
* Day 4: Elsie drops to 6 → no change
* Day 7: Mildred rises to 10 → display changes
* Day 9: Mildred drops to 9, ties with Bessie → display changes
