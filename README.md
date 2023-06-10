# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1

array = eval(input())
k = eval(input())
n=len(array)
array.sort()
result = linearSearch(array,n,k)
print(array)
if(result== -1):
    print("Element not found")
else:
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binarySearchIter(array, k, low, high):
    while low <= high:
        mid = low + (high - low) // 2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low=mid+1
        else:
            high = mid - 1
    return -1
array = eval(input())
array.sort()
k = eval(input())
n=len(array)
result=binarySearchIter(array, k, 0, n-1)
print(array)

if result == -1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def BinarySearch(arr, k, low, high):
    if low<=high:
        mid = low + (high - low) // 2
        if arr[mid] == k:
            return mid
        elif arr[mid] > k:
            return BinarySearch(arr, k, low, mid-1)
        elif arr[mid] < k:
            return BinarySearch(arr, k, mid+1, high)
    else:
        return -1
    
arr = eval(input())
arr.sort()
k = eval(input())
n = len(arr)
result = BinarySearch(arr, k, 0, n-1)
print(arr)

if result == -1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
## Output
![image](https://github.com/Aswinth21/Search-Algorithm/assets/120236638/a078b379-32db-44fb-b480-325afb2dfced)

![image](https://github.com/Aswinth21/Search-Algorithm/assets/120236638/f59f65bf-379b-467f-b694-a2ea44449057)

![image](https://github.com/Aswinth21/Search-Algorithm/assets/120236638/89e749ec-e321-4332-ac7f-7f6c9aaf3680)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
