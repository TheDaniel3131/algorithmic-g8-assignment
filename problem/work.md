## Real-Life Problem: E-commerce Product Sorting
Problem Description:
E-commerce platforms handle massive amounts of data, including product listings that need to be sorted based on various criteria such as price, popularity, ratings, or relevance to a search query. Efficient sorting is crucial for providing a smooth and responsive user experience, allowing customers to quickly find the products they are interested in.

Real-Life Examples:
1. Sorting Products by Price
Scenario:
An e-commerce website needs to display a list of products sorted by price in ascending order when a user selects the "sort by price: low to high" option.

Relevance:
Customers often sort products by price to find the most affordable options. Efficient sorting ensures that the website can quickly respond to user actions, especially during high-traffic periods like sales events.

2. Sorting Products by Popularity
Scenario:
An online store wants to sort products by popularity, where popularity is determined by the number of purchases or views a product has received.

Relevance:
Displaying popular products at the top of the list can drive more sales and enhance user satisfaction. Sorting by popularity helps customers discover trending items, improving their shopping experience.

<hr>

#### References:
- Help: https://chatgpt.com/share/e735a8b3-5c39-4b06-baaa-3feef6556d19

1. https://www.geeksforgeeks.org/quick-sort-vs-merge-sort/
2. https://www.geeksforgeeks.org/quick-sort-algorithm/

1. https://www.youtube.com/watch?v=Vtckgz38QHs&ab_channel=BroCode
2. https://www.youtube.com/watch?v=3j0SWDX4AtU


```python
# mergesort.py

import time
import random

def test_merge_sort(arr):
    start_time = time.time()
    merge_sort(arr)
    end_time = time.time()
    return end_time - start_time

def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2
        left_half = arr[:mid]
        right_half = arr[mid:]

        merge_sort(left_half)
        merge_sort(right_half)

        i = j = k = 0

        while i < len(left_half) and j < len(right_half):
            if left_half[i] < right_half[j]:
                arr[k] = left_half[i]
                i += 1
            else:
                arr[k] = right_half[j]
                j += 1
            k += 1

        while i < len(left_half):
            arr[k] = left_half[i]
            i += 1
            k += 1

        while j < len(right_half):
            arr[k] = right_half[j]
            j += 1
            k += 1

# Arrays with 10,000,000 elements
sorted_arr = list(range(10000000))
reverse_sorted_arr = list(range(10000000, 0, -1))
random_arr = [random.randint(0, 10000000) for _ in range(10000000)]

# Display Arrays for comparison
# print(sorted_arr)
# print(reverse_sorted_arr)
# print(random_arr)

# Test Merge Sort on best-case scenario (Already Sorted)
best_case_time = test_merge_sort(sorted_arr)
print(f"Merge Sort (Best Case) took {best_case_time:.6f} seconds")

# Test Merge Sort on worst-case scenario (Reverse Sorted)
worst_case_time = test_merge_sort(reverse_sorted_arr)
print(f"Merge Sort (Worst Case) took {worst_case_time:.6f} seconds")
```


```python
# quicksort.py

import time
import random

def quick_sort(arr, low, high):
    if low < high:
        pivot_index = random.randint(low, high)  # Choose a random pivot index
        pivot = arr[pivot_index]
        arr[pivot_index], arr[high] = arr[high], arr[pivot_index]  # Move pivot to the end
        i = low
        for j in range(low, high):
            if arr[j] < pivot:
                arr[i], arr[j] = arr[j], arr[i]
                i += 1
        arr[i], arr[high] = arr[high], arr[i]  # Move pivot to its final position
        quick_sort(arr, low, i - 1)
        quick_sort(arr, i + 1, high)

def test_quick_sort(arr):
    arr_copy = arr.copy()
    start_time = time.time()
    quick_sort(arr_copy, 0, len(arr_copy) - 1)
    end_time = time.time()
    return end_time - start_time

# Arrays with 10,000,000 elements
sorted_arr = list(range(10000000))
reverse_sorted_arr = list(range(10000000, 0, -1))
random_arr = [random.randint(0, 10000000) for _ in range(10000000)]

# Display Arrays for comparison
# print(sorted_arr)
# print(reverse_sorted_arr)
# print(random_arr)

# Test Quick Sort on best-case scenario (Already Sorted)
best_case_time = test_quick_sort(sorted_arr)
print(f"Quick Sort (Best Case) took {best_case_time:.6f} seconds")

# Test Quick Sort on worst-case scenario (Reverse Sorted)
worst_case_time = test_quick_sort(reverse_sorted_arr)
print(f"Quick Sort (Worst Case) took {worst_case_time:.6f} seconds")



```
