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

### JavaScript Binary Search
- [JSBin Practice](http://jsbin.com/sotiqafeva/7/edit?js,console)
```
function binary_search(list, item) {
  let low = 0;
  let high = list.length - 1;

  while(low <= high) {
    let mid = Math.floor((low+high)/2);
    let guess = list[mid];

    if (item === guess) {
      return mid;
    } else if (item < guess) {
      high = mid - 1;
    } else if (item > guess) {
      low = mid + 1;
    }
  }
  return null;
}

const my_list = [1, 3, 5, 7, 9];

console.log(binary_search(my_list, 3)); // 1
console.log(binary_search(my_list, -1)); // null
```


## Big O
- The way to analyze how efficient algorithms (or code in this case) without getting too mired in the details
- Can model how much time any function is going to take given n inputs
- Big O establishes a worst-case run time
- Common Big O run times
  - O(n): Simple Search
  - O(log n): Binary Search
  - O(n * log n): Fast sorting like quick search
  - O(n^2): Slow sorting like selection search
  - O(n!): Traveling Salesperson Problem

-----------------

## Selection Sort
- Selection sort is a neat algorithm, but it’s not very fast
- Selection Sort Steps:
  - Run through the entire list
  - Get the smallest element in each run
  - Append it to the final sorted list
- Big O: O(n^2)

### Array
- Array stores item continuously
- Insertion: O(n)
- Search: O(1)

### List
- List stores item anywhere in memory linked with each other
- Insertion: O(1)
- Search: O(n)
-----------------


## Recursion
- A function that calls itself
- Make the code very simple for some problems
- Potentially large footprint with it as every time you call the function, it adds another call to the stack
