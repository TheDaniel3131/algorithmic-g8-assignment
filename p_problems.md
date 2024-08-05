Your definition and explanation of P problems is correct and well-articulated. Here is an integrated version with slight enhancements for clarity and detail:

### Part B: Complexity Classification

#### i) Explain P (Deterministic Polynomial time) problems with a suitable example. [10 Marks]

**Example of a P Problem: E-commerce Product Sorting by Price**

**Definition and Explanation:**

Polynomial-time problems, also known as P Problems, are a type of problem that can be solved efficiently by a deterministic algorithm in polynomial time. This means that as the size of the input (𝑛) increases, the time taken to solve the problem grows polynomially, typically as \( O(n^k) \), where \( k \) is a constant. The class P includes a variety of natural tasks such as sorting, linear programming, primality testing, and matching problems (Jebara, 2014).

**Example Explanation:**

One real-world example of a P problem is e-commerce product sorting by price. E-commerce platforms, such as Amazon, Shopee, and Lazada, need to sort products based on various criteria, with price being one of the most commonly used. When a user selects the "sort by price: low to high" option, the platform must display the products in ascending order of their prices. An efficient algorithm to achieve this is Merge Sort, which operates in \( O(n \log n) \) time, making it a polynomial time algorithm.

**Application to the Problem:**

To understand how Merge Sort is applied to the problem of sorting e-commerce products by price, let's break down the steps involved in the algorithm:

- **Divide:** The product list is divided into smaller sub-lists. This step involves recursively splitting the list into two halves until each sub-list contains a single element or is empty. This division ensures that the problem of sorting is broken down into manageable sub-problems.
- **Conquer:** Each sub-list is sorted individually. Since each sub-list contains only one element, it is inherently sorted. The algorithm then recursively sorts and merges these sub-lists.
- **Combine:** The sorted sub-lists are merged to form the final sorted list. During the merge process, the algorithm compares the elements of each sub-list and arranges them in ascending order to create a fully sorted list.

**Explanation:**

Using Merge Sort for sorting e-commerce products by price ensures that even for large lists of products, the sorting process remains efficient and responsive. The \( O(n \log n) \) time complexity indicates that the algorithm scales well with the size of the input, making it suitable for handling vast amounts of product data typically found on e-commerce platforms. This efficiency is crucial for providing a seamless user experience, allowing customers to quickly find the products they are looking for without experiencing delays, even during peak traffic periods such as sales events.

By employing an efficient sorting algorithm like Merge Sort, e-commerce platforms can maintain high performance and user satisfaction. This approach ensures that product sorting operations do not become a bottleneck, contributing to a smooth and responsive browsing experience for users.

---

This revised version incorporates your definition and explanation while seamlessly integrating with the example provided.
