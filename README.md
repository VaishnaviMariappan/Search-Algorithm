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
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Vaishnavi M
RegisterNumber: 21500310

def binarySearchIter(array, a, low, high):
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    while(low<=high):
        mid = low+(high-low)//2
        if array[mid]==a:
            return mid
        elif array[mid]<a:
            low=mid+1
        else:
            high = mid+1
    return -1
    
array = eval(input())
#sort the array
array.sort()
a = eval(input()) #k-item to be searched
result = binarySearchIter(array, a, 0, len(array)-1)
# use the binary search function to find the item in the list
if result>=0:
    print(array)
    print("Element found at index: ",result)
else:
    print(array)
    print("Element not found")
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Vaishnavi M
RegisterNumber: 21500310

def binarySearchIter(array, a, low, high):
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    while(low<=high):
        mid = low+(high-low)//2
        if array[mid]==a:
            return mid
        elif array[mid]<a:
            low=mid+1
        else:
            high = mid+1
    return -1
    
array = eval(input())
#sort the array
array.sort()
a = eval(input()) #k-item to be searched
result = binarySearchIter(array, a, 0, len(array)-1)
# use the binary search function to find the item in the list
if result>=0:
    print(array)
    print("Element found at index: ",result)
else:
    print(array)
    print("Element not found")
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Vaishnavi M
RegisterNumber: 21500310

def BinarySearch(arr, a, low, high):
# Write your code here for binary search using recursive method
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==a:
            return mid
        elif arr[mid]<a:
            return BinarySearch(arr,a,mid+1,high)
        else:
            return BinarySearch(arr,a,low,mid+1)
    return -1
arr = eval(input())
#sort the array
arr.sort()
print(arr)
# k is the element to be searched for
a = eval(input()) 
low=0
high=len(arr)-1
# use the binary search function to find the result
result=BinarySearch(arr, a, low, high)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")

```
## Sample Input and Output

![input](./input.jpeg)
![output](./output1.png)
![output](./output2.png)
![output](./output3.png)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.