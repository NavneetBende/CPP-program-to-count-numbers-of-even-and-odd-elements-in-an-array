Count Even and Odd Elements in C++
Here, in this page we will discuss the count even and odd elements in C++ programming language. We are given with an array and need to print the count of the even elements and odd elements in the given input array.

count numbers of even and odd elements
While loop in C
Method discussed :
Method 1 : Using Modulo Operator
Method 2 : Using Bit-wise AND operator.
Let’s go through with above two methods one by one,

Method 1 :
Declare two variables say count_even=0, count_odd=0.
Start iterating over the array,
Check if(arr[i]%2==0) set even_count++.
Else set odd_count++
Print the value of even_count and odd_count.
Time and Space Complexity :
Time Complexity : O(n)
Space Complexity : O(1)
Modulo Operator
The modulo operator, denoted by %, is an arithmetic operator. The modulo division operator produces the remainder of an integer division. Syntax: If x and y are integers, then the expression: x % y. produces the remainder when x is divided by y.
So, if a number is even then it return 0 on modulo it by 2, otherwise it return 1
Method 1  : Code in C++
Run

#include<bits/stdc++.h>
using namespace std;

int main(){

   int arr[] = {1, 7, 8, 4, 5, 16, 8};
   int n = sizeof(arr)/sizeof(arr[0]);

   int even_count=0, odd_count=0;

   for(int i=0; i<n; i++){
     if(arr[i]%2==0)
       even_count++;

     else 
       odd_count++;
   }
   cout<<"Even Elements count : " <<even_count<< "\nOdd Elements count : " << odd_count;
}
Output :
Even Elements count : 4
Odd Elements count : 3
Related Pages
Finding Minimum scalar product of two vectors

Finding Maximum scalar product of two vectors in an array

Find all Symmetric pairs in an array 

Find maximum product sub-array in a given array

Finding Arrays are disjoint or not

Method 2 :
In this method we will use bit-wise AND operator. By doing AND of 1 with array element, if the result comes out to be 1 then the number is odd otherwise even.

Bit-wise AND Operator
The bitwise AND operator ( & ) compares each bit of the first operand to the corresponding bit of the second operand. If both bits are 1, the corresponding result bit is set to 1.
Otherwise, the corresponding result bit is set to 0. Both operands to the bit-wise AND operator must have integral types.
Method 2  : Code in C++
Run

#include<bits/stdc++.h>
using namespace std;

int main(){

   int arr[] = {1, 7, 8, 4, 5, 16, 8};
   int n = sizeof(arr)/sizeof(arr[0]);

   int even_count=0, odd_count=0;

   for(int i=0; i<n; i++){
     if(arr[i]&1==0)
       even_count++;

     else 
       odd_count++;
   }
   cout<<"Even Elements count :" <<even_count<< "\nOdd Elements count : " << odd_count;
}
Output :
Even Elements count : 4
Odd Elements count : 3
