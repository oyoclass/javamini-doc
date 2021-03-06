#Arrays
### 1-Dimensional Arrays

<span style="color:blue">**How to Declare an Array**</span>    
It is declared in the following format:  
**type[] name**: the type represents the type of variable ie. int, and the name is the name of the new array

```java
int[] arr1; //Creates an array called arr1 that holds integer values
float[] arr2; //Creates an array called arr2 that holds floating-point values
```

<span style="color:blue">**How to Initialize the Size of an Array** </span>   
In Java, you must declare the size of the array. If not, the size will _always_ be zero.

* **type[] name;**  
  **name = new type[size];**  
  You declare the array first and then you create the size of the array after the declaration.

```java
int[] arr1; //This is the initial declaration of an array.
arr1 = new int[2]; //This sets the newly created array to size 2.
```

* **type[] name = new type[size]**: You declare and initialize the array in the same line, and make an array of a type that has a certain size.

```java
int[] arr2 = new int[10]; //This makes an array that can hold 10 integers.
String[] arr3 = new String[5]; //This makes an array that can hold 5 Strings.
```

<span style="color:blue">**How to Reference the Indices in an Array**  </span>  
The indices of an array start at 0. So, the first element of an array would be at the 0th position.  
The highest position would then be _size - 1_.
```java
int[] arr4 = new int[20];
arr4[1] = 20; //Sets the 2nd integer in the array to 20.
arr4[0] = 40; //Sets the 1st integer in the array to 40.

String[] arr5 = new String[25];
arr5[0] = "Hi"; //Sets the 1st indice to "Hi"
```

<span style="color:blue">**How to Find the Length in an Array**  </span>  
You can find the length of an array using the .length function.  
```java
int[] arr4 = new int[20];
System.out.print(arr4.length); //This would print out 20
```
---
### 2-Dimensional Arrays  
<span style="color:blue">** How to Declare a 2-Dimensional Array ** </span>  
Declaring a 2-dimensional array is similar to the way that the 1-dimensional array is declared. Instead of only having a "size" parameter, the 2-dimensional array has two size parameters, usually denoted with row and column.  

It is declared in the following format:  
**type[][] name**: the type represents the type of variable ie. int, and the name is the name of the new array
```java
int[][] arr1; //Creates an array called arr1 that holds integer values
float[][] arr2; //Creates an array called arr2 that holds floating-point values
```

<span style="color:blue">**How to Initialize the Size of a 2-Dimensional Array** </span>  

* **type[][] name;**  
  **name = new type[row][col];**  
  You declare the array first and then you create the size of the array after the declaration.  
  There are "row" x "col" elements in an array.

```java
int[][] arr1; //This is the initial declaration of an array.
arr1 = new int[2][3]; //Sets the newly created array to 2 by 3. There are 6 elements in the array.
```

* **type[][] name = new type[row][col]**: You declare and initialize the array in the same line, and make an array of a type that has a certain size.

```java
int[][] arr2 = new int[10][2]; //This makes an array that can hold 20 integers.
String[][] arr3 = new String[5][3]; //This makes an array that can hold 15 Strings.
```

<span style="color:blue">**How to Reference the Indices in a 2D Array**  </span>  
The indice of a 1-Dimensional Array starts at 0. Similarly, the 2-Dimensional array would start at index 0 too, but since there are two size parameters, the array would start at arr[0][0].
The highest position would then be _arr[size-1][size-1]_.

Think of a 2-Dimensional array like a table. The first index you place is the row number, the second number you place is the column number.
```java
int[][] arr4 = new int[20][5];
arr4[19][4] = 20; //Sets the last element at row 19 and col 4 in the array to 20.
arr4[0][0] = 40; //Sets the first integer, at index [0][0] in the array to 40.

String[][] arr5 = new String[2][5];
arr5[0][0] = "Hello"; //Sets the element at row 0 and col 0 to "Hi"
```

<span style="color:blue">**How to Find the Length in an Array**  </span>  
To find the length of the row and the length of the column.

* arr.length: Find the number of rows in the array "arr".
* arr[i].length: Find the number of columns in the row "i" in the array "arr".

```java
int[][] arr4 = new int[20][5];
System.out.println(arr4.length); //This would print out 20
System.out.println(arr4[0].length); //This would print out 5
```
---
### Initializing Arrays with a List
<span style="color:blue">**How to Initialize in an 1-Dimensional Array with a List**  </span>  

You need to use the "{" and "}" to denote the beginning and the end of the new list.

* Declare the array first and then initialize the array afterwards:  
&nbsp;&nbsp;**int[] arrays;**  
&nbsp;&nbsp;**arrays = new int[]{w,x,y...};**  
The order that the values are in the list corresponds to the index of the values in the array, ie. arrays[0] = w, and arrays[2] = y.

```java
int[] arrays; //Declares a new array called arrays
arrays = new int[]{4,5,6,7,8}; //Initialized arrays with the values, 4, 5, 6, 7, and 8.
//arrays[0] = 4, arrays[4] = 8
```

* Declare and initialize the array at the same time:  
&nbsp;&nbsp;**int[] arrays = {w,x,y...};**   
The order that the values are in the list corresponds to the index of the values in the array, ie. arrays[0] = w, and arrays[2] = y.

```java
int[] arrays = {4,5,6,7,8}; //Initialized arrays with the values, 4, 5, 6, 7, and 8.
// arrays[0] = 4, arrays[4] = 8
```

<span style="color:blue">**How to Initialize in an 2-Dimensional Array with a List**  </span>  
The main difference between initializing a 2-Dimensional Array and a 1-Dimensional array is the addition of a second parameter for size.  

Rather than just using the "{}", to denote the new list, you need to nest "{" and "}". The notation for this is usually {{a,b,c}, {d,e,f}, {g,h,i}, {j,k,l}}.  

The first "{" and the last "}" denotes the entire list. The first pair of "{}" that encloses a,b, and c denotes the first row of index 0. The value a would be in index [0][0], the value b would be in [0][1], and the value b would be in [0][2]. The last grouping represented by {j,k,l} would be the fourth row, which has the index 0.


* Declare the array first and then initialize the array afterwards:  
&nbsp;&nbsp;**int[][] arrays;**  
&nbsp;&nbsp;**arrays = new int[][]{{w,x,y...}, {w2, x2, y2...}, ... {wz, xz, yz..};**  
The order that the values are in the list corresponds to the index of the values in the array, ie. arrays[0][1] = x, and arrays[1][2] = y2.

```java
int[][] arrays; //Declares a new array called arrays
arrays = new int[]{
  {4,5,6,7,8},
  {2,1,2,9,5}
}; //Initialized arrays with the values from the list.
//arrays[0][0] = 4, arrays[1][3] = 9
```

* Declare and initialize the array at the same time:  
&nbsp;&nbsp;**int[] arrays = {{w,x,y...}, {w2, x2, y2...}, ... {wz, xz, yz..};**   
The order that the values are in the list corresponds to the index of the values in the array, ie. arrays[0][0] = w, and arrays[1][1] = x2.

```java
int[][] array4 = {
  {4,5,6,7,8},
  {0,1,3,2,11}
}; //Initialized arrays with the list values.
// arrays[0][0] = 4, arrays[1][4] = 11
```
