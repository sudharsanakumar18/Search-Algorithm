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
def linearsearch(array,n,k):
    for i in range(0,n):
        if array[i]==k:
            print("Element found at index: ",i)
            break
    else:
        print("Element not found")
array = eval(input())
array.sort()
print(array)
k = int(input())
n=len(array)
result=linearsearch(array,n,k)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binarysearch(arr,k,low,high):
    if low<=high:
        m=(low+high)//2
        if k==arr[m]:
            return m
        elif k>arr[m]:
            low=m+1
            return binarysearch(arr,k,low,high)
        elif k<arr[m]:
            high=m-1
            return binarysearch(arr,k,low,high)
    else:
        return -1
array=eval(input())
array.sort()
print(array)
k=eval(input())
n=len(array)
t=binarysearch(array,k,0,n-1)
if t==-1:
    print("Element not found")
else:
    print("Element found at index: ",t)
    




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```

def binarysearch(arr,k,low,high):
    if low<=high:
        m=(low+high)//2
        if k==arr[m]:
            return m
        elif k>arr[m]:
            low=m+1
            return binarysearch(arr,k,low,high)
        elif k<arr[m]:
            high=m-1
            return binarysearch(arr,k,low,high)
    else:
        return -1
array=eval(input())
array.sort()
print(array)
k=eval(input())
n=len(array)
t=binarysearch(array,k,0,n-1)
if t==-1:
    print("Element not found")
else:
    print("Element found at index: ",t)
    



```
## Output:
Output 1:
![image](https://raw.githubusercontent.com/sudharsanakumar18/Search-Algorithm/main/python%203b%20a.png)

Output 2:
![image](https://raw.githubusercontent.com/sudharsanakumar18/Search-Algorithm/main/python%203b%20b1.png)
![image](https://raw.githubusercontent.com/sudharsanakumar18/Search-Algorithm/main/pyhton%203b%20b2.png)

Output 3:
![image](https://raw.githubusercontent.com/sudharsanakumar18/Search-Algorithm/main/python%203b%20c1.png)
![image](https://raw.githubusercontent.com/sudharsanakumar18/Search-Algorithm/main/python%203b%20c2.png)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
