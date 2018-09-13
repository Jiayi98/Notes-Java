## Arrays

Object that stores many values of the same type

### Declaration

```java
Syntax:

  <type>[] variableName = new <type>[length];
  
  2D-Array:
  <type>[][] variableName = new <type>[length1][length2];
```
note: arrays have 0-based index which allows you access an element from an array directly. Index has range \[0,length). 
#### The default value of elements in an array: 
  - int:0
  - double: 0.0
  - boolean: false
  - Object: null
  
###  Quick Array Initialization
```java
  <type>[] array = {<value>,<value>,<value>...};
```
note: compiler will calculate the length of array automatically.

### Access Elements/Assign Value
```java
Syntax:
  variableName[index] \\ access
  variableName[index] = value \\ assign or modify
```
note: index has range 0 to length-1 inclusively, otherwise there will be ArrayOutOfBoundsException.

### Length
```java
Syntax:
  arrray.length \\ unlike String object s.length()
```

### Iterating

```java
Syntax:
  for(int i = 0; i < array.length; i++){}
  
  for(<type> obj : array){} \\ for-each loop
  
  int i = 0;
  while(i < array.length){}
```

### Limitations of Arrays
1. Cannot resize an existing array
2. Cannot compare arrays with == or .equals()
3. Cannot be printed directly

#### Arrays Class
in java.util package

| Methods        |            | 
| ------------- |-------------|
| binarySearch(\<array\>,\<value\>)      | return the index of the given value, return -1 if it doesn't exist |
| copyOf(\<array\>,\<length\>)    | shallow copy of this array, return a new array with specific length    | 
|copyOfRange(\<arr\>,\<start index\>, \<stop index\>)||
| equals(\<arr1\>,\<arr2\>)| return true if elements in 2 arrays are same and in the same order      |  
|sort(\<arr\>)| |
|toString(\<arr\>)| return a string representing the array|
```java
 Syntax:
    import java.util.Arrays;
    Arrays.methodName(<parameters>)
```
### Reference Semantics
When one variable is assigned to another, the object is not copied. Both variables refer to the same object. Thus, modifying the value of one variable will affect other one.
```java
example:

  int[] a = {1,2,3,4};
  int[] b = a;
  b[0] = 10; \\ a will be {10,2,3,4}
  
```

### Reversal Array's elements
Arrays and objects use reference semantics.
When arrays are passed as parameter, they are no copied. The parameter, which is a copy of the same reference the argument stores, refers to the same object. 
```java
  for(int i = 0; i < arr.length; i++){
    int temp = arr[i];
    arr[i] = arr[arr.length-1-i];
    arr[arr.length-1-i] = temp;
  }
```


