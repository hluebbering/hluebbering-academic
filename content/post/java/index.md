---
title: Sorting Algorithms in Java
subtitle: Sorting Algorithms and Execution Time
abstract: Sorting Algorithms and Execution Time
date: 2020-08-01
math: true
diagram: true
image:
  placement: 2

links:
- icon: github
  icon_pack: fab
  name: Java Code
  url: https://github.com/hluebbering/java-structures/tree/main/04-Sorting/src

---

Lab 5. Sorting Algorithms
================



## Insertion Sort

### Background

**Definition.** a Java sorting method where the sorted values locate to
the low end of the array, and the unsorted values locate to the high
end. There are $n-1$ passes over the array, with a new unsorted value inserted each time

- expected running time is $n$ compares and data movements –most compares will lead to movement of a data value
- best case running time performance is $O(n)$ comparisons –occurs for no movements of data within the array
- therefore, it’s best to implement insertion sort on data that is
nearly ordered

 

#### Show how Insertion Sort acts on the following List:

``` java
list X: 7 5 4 6 8 2
```

  - Iterate through the array
  - Shifting all of the elements to the right until we encounter the
    first element we don’t have to shift
  - Place the new element into its proper place within the sorted
    subarray

 

![](images/equation.svg)

 

### Java Methods

#### Method to Insertion Sort a generic type that extends the interface Relateable

1.  create a LinkedList
2.  initialize ICount
3.  walk down ArrayList and insert each element into sorted LinkedList
4.  repackage and return ArrayList
5.  method to insert a new element myObj into a sorted LinkedList
      - use a loop to traverse LinkedList
      - begin with first element (smallest T) and find where myObj
        should go
6.  debugging tool and method to dump out content in LinkedList

 

### Code Output

#### Execution Times

At the worst case scenario for the algorithm, the whole array is descending. This is because in each iteration, we’ll have to move the whole sorted list by 1, which is $O(n)$. We have to do this for each element in every array, which means it’s going to be bounded by $O(n)$.

-----

## Bubble Sort

### Background

**Definition.** Bubble sort checks and rechecks the relation between each component of the list. The method sorts the $n$ elements by linearly moving through the list

- where each pass completes $n-1$ comparisons and $n-1$ exchanges.

- After one pass, the largest integer-value should “bubble” up to the ArrayList’s high-indexed side –the operation repeats.

- After $n-1$ passes, the bubble sorting terminates.

 

### Java Methods

#### Bubble Sort Class

1.  Method sorts the elements by linearly moving through the list
2.  After a pass, the largest value “bubbles” up the ArrayList
3.  Bubble sorting repeats for (n-1) passes

 

### Code Output

#### Execution Times

From the above execution times and graph, we can see that as the number
of data points $n$ increases, the number of steps it takes to complete the bubble sort increases **exponentially**. In **big-O notation**, the Simple Bubble Sort Method for sorting $n$ elements of an array is $O(n)$; hence, the algorithm has a run time that grows quadratically as the input (data points) size grows.

-----


## Merge Sort

### Background

**Definition.** MergeSort is a recursive sorting technique that
recursively splits, sorts, and reconstructs the data. This method
recursively

  - divides the data into two unsorted lists,
  - sorts the two lists,
  - and then merges the two sorted lists.

 

### Java Methods

#### Merge Sort Algorithm

1.  Break the whole array down into two subarrays
2.  Sort the left half of the array (recursively)
3.  Sort the right half of the array (recursively)
4.  Merge the solutions

 

### Code Output

#### Execution Times

Each value $n$ in the data set must be sorted into a temporary array, allotted once before every single merge; therefore, we have $n$ compares over all the merges. From the above execution times and graph, we can see that as the number of data points $n$ increases, the number of steps it takes to complete the bubble sort increases **logarithmically**.

In **big-O notation**, since there are $\log{2n}$ split levels, we have a time execution of $n\log{2n}$; hence, the search algorithm has a run time that grows logarithmically as the input size grows.

-----

## Summary

### Sorting Techniques:

From the graph below, we can see that the number of steps to execute the
Merge Sort method is significantly lower than the number of steps to
execute the Bubble Sort method; hence, the Merge Sort is faster and more
efficient than the Bubble Sort.

<img src="images/plot.jpg" width="600" style="display: block; margin: auto;" />

-----
