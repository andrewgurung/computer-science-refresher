# Computer Science Refresher
Grokking Algorithms

Author Info
-----------
Author: Andrew Gurung <br>
URL: http://www.andrewgurung.com/

Table of Contents
-----------------
- Introduction to Algorithms
- Selection Sort
- Recursion
- Quicksort
- Hash Tables
- Breadth-first Search
- Dijkstra’s algorithm
- Greedy algorithms
- Dynamic programming
- K-nearest neighbors

-----------------

## Introduction to Algorithms
- An algorithm is a set of instructions for accomplishing a task
- A binary search can reduce 4 billion steps down to 32
- Running time is calculated in Big O notation

### Binary Search
- Algorithms that searches a **sorted** list, and returns its position. Returns `null` if not found
- Searching through a telephone directory of 1024 people
- Simple search may take up to 1024 guesses
- Binary search will divide the list into half, and focuses on the probable half neglecting the other half
  - Reduces the search list into half each time. Total steps required = log 1024 = 10
  - log is the opposite of exponent
  - 2^10 = 1024. Exponent = 10
  - log 1024 = 10. Log of a value = Exponent of base. [Base is 2 for this case]


## Big O
- The way to analyze how efficient algorithms (or code in this case) without getting too mired in the details
- Can model how much time any function is going to take given n inputs
- Instead of exact figure, we are concerned in the order of magnitude of the number
- For a 3x² + x + 1, we just interested in the x²
- One for loop = O(n)
- Two nested for loop = O(n²)
- No loops = O(1)
- O(log n) if a code employs a divide-and-conquer strategy (often recursive)
  - As you add more terms, the increases in time as you add input diminishes

-----------------

## Recursion
- A function that calls itself
- Make the code very simple for some problems
- Potentially large footprint with it as every time you call the function, it adds another call to the stack
