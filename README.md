#### This programming assignment has three parts.

Work on this dataset Download this dataset. The dataset contains 1000 baskets, each with 3 to 10 items. There are 20 different items in the dataset. 

---

Part I

Plot the distribution of item counts in the dataset. Compute frequent items with support 260.  Output the list of frequent items sorted in increasing order.   

Submit your code, output, and distribution figure.  

--- 

Part II

Compute frequent pairs with support 260. Output the list of frequent pairs sorted in increasing order.       

Submit your code and output. 

---

Part III

Implement PCY algorithm for finding frequent pairs. 

Follow this pseudocode:

Input parameter: (s, b).    s - support; b - number of bucket.

#### items have integer IDs

1st Pass:
```code
FOR (each basket) 
    FOR (each item in the basket)
           add 1 to item’s count;
    FOR (each pair of items in the basket)
           hash the pair to a bucket; (Use this hash function for pair {i, j}:  i+j modulo b.)
           add 1 to the count for that bucket; (Buckets are indexed as integer 0, 1, ..., b-1.) 
```
2nd Pass:
```code
FOR (each basket) 
    FOR (each pair of items in the basket)
           hash the pair to a bucket;  (Use this hash function for pair {i, j}:  i+j modulo b.)
           IF (the counts of both items and the bucket are all equal to or larger than s)
                    add 1 to the pair's count;
```
Output: number of frequent pairs, a list of the frequent pairs sorted in increasing order.       

 

#### Run your program on 

Run your program with the following parameters:

1)  s = 260, b = 10

2)  s = 260, b = 20

 

Submit your code and outputs of the two runs.