Maximum profit by buying and selling a share at most twice
Here on this page, we will learn to create Python Program to calculate Maximum profit by buying and selling a share at most twice when all the prices are given in an array.

Example :

Input : price = [2, 30, 15, 10, 8, 25, 80]
Output : 100
Maximum profit by buying and selling a share at most twice in Python

Algorithm
Initialize a variable ans with value zero
Iterating from 0 to l using for loop with variable i
Run the nested loop with variable j from i+1 to l
If arr[j] > arr[i] then put a equals to arr[j] – arr[i] & b = next(arr[ j+1 :  ]. Check if ans is less then b+a then put ans = b +a
Algorithm for next function
Initialize a variable ans with value zero
Iterate using for loop between range 0 to the length of arr
Run a nested loop using variable j from i+1 to length of arr
For each iteration put a equals to arr[i] and b = arr[j]
check if b is greater than a and and is lea then b – a then assign b-a to ans
Python Code
Run
def next(arr):
    ans = 0
    for i in range(len(arr)):
        for j in range(i + 1, len(arr)):
            a = arr[i]
            b = arr[j]
            if b > a and ans < b - a:
                ans = b - a
    return ans


def stock_price(arr, l):
    ans = 0
    for i in range(l):
        for j in range(i + 1, l):
            if arr[j] > arr[i]:
                a = arr[j] - arr[i]
                b = next(arr[j + 1:])
                if ans < b + a:
                    ans = b + a

    return ans


price = [2, 30, 15, 10, 8, 25, 80]
print("Maximum profit is :", stock_price(price, len(price)))
Output
Maximum profit is : 100
