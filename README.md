insertionSort is the name of the function, and it accepts a single argument arr, which is an array that you want to sort.

.......................................................................................................................
........................................................................................................................

Outer Loop (Iterating through the Array) : 

This loop starts at i = 1 and goes until i = arr.length - 1, meaning it processes each element in the array from the second element to the last.
The reason we start at i = 1 is that we consider the first element (arr[0]) to be trivially sorted (since there’s nothing to compare it to).
For each iteration of this loop, we will insert the element at index i into the correct position in the sorted portion of the array (arr[0] to arr[i-1]).

........................................................................................................................
........................................................................................................................

Current Element to be Inserted : 

currentElement is the value at index i of the array. This is the element we want to insert into the correct position in the sorted part of the array.

........................................................................................................................
........................................................................................................................
Inner Loop (Finding the Correct Position) : 

j is initialized to i - 1. This is the index of the last element in the sorted portion of the array. We’ll compare currentElement to the elements in this portion (from index j down to 0).

........................................................................................................................
........................................................................................................................

while (j >= 0 && arr[j] > currentElement) {
This while loop checks two things:
j >= 0: Ensures we don’t go out of bounds of the array.
arr[j] > currentElement: If the element at index j is greater than currentElement, we need to shift it to the right to make space for currentElement.
If both conditions are true, we proceed with the loop.
........................................................................................................................
........................................................................................................................

Shifting Elements:
This line shifts the element at index j one position to the right (i.e., arr[j] is moved to arr[j + 1]).
This is done because the element at arr[j] is greater than the currentElement, so it needs to be moved one position to the right to make space for currentElement.
j--;
After shifting the element, we decrement j to move one position to the left, so we can continue comparing and shifting until we find the correct position for currentElement.

........................................................................................................................
........................................................................................................................

Inserting the Current Element : 
After the while loop ends (when either j < 0 or arr[j] <= currentElement), this line inserts currentElement at the correct position (index j + 1).
........................................................................................................................
........................................................................................................................
finally return




