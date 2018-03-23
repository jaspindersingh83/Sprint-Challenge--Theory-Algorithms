* Exercise 1
a) O(n)
b) Infinite loop for worst case
c) O(sqrt n)
d) O(n2)
e) O(n3)
f) O(n)
g) O(n)


* Exercise 2

Algorithms

* a) Time Complexity O(n). Space Complexity O(1)
    1) The max difference will be between minimum element in the arr and max element in the array. So we just need to find min and max in the array.
    2) Define two integer pointers min and max. Set min and max to arr[0]
    3) Iterate through the array and set min to array[index] if array[index] < min.
    For max check and set if array[index] > max.
    4) return (max-min)

* b) Do a binary search on n story building 
    Time Complexity O(logn). Space Complexity O(1)
    1) Have a current floor pointer and set it to n initially.
    2) Drop the egg from current floor. It doesn't break then return index of current floor.
    3) Else come to middle of current 'n'. If it breaks come to middle of middle. For eg: n -> n/2 -> n/4. If it doesn't break then go to (n-middle)/2 floors up the current floor.
    4) Run a recursive funtion on current floor. When we hit the base case return index.
    We will not be breaking more than 30 eggs ever.

* Exercise 3

a) Time Complexity O(n2). We practically are not left with any left array to work with after running the first iteration through the loop and right array will have n-1, n-2 , n-3 ......after successive recursive calls.
b) O(nLogn) will be the worst case complexity if we choose median as pivot. It will enable equal partitions in divide and conquer.
