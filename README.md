

# Largest and Second Largest Element Finder

## Description
This Java program finds the largest and second-largest elements in a user-defined array. It takes input for the array size and elements, sorts them using a nested loop, and identifies the largest and second-largest elements.

## Features
- Accepts user input for array size and elements.
- Uses nested loops to sort the array in ascending order.
- Identifies and prints the largest and second-largest elements.

---

## Code Explanation

### **1. Importing Scanner Class**
The program imports the `Scanner` class from the `java.util` package to take user input.

```java
import java.util.Scanner;
```

### **2. Class and Main Method**
The `LargestElement_inArray` class contains the `main` method, which is the entry point of the program.

```java
public class LargestElement_inArray
{
    public static void main(String[] args)
    {
```

### **3. Taking User Input**
The program prompts the user to enter the size of the array and then the elements.

```java
Scanner s = new Scanner(System.in);
System.out.println("Enter the Size");
int size = s.nextInt();
int arr[] = new int[size];
System.out.println("Enter the Elements");
for(int i = 0; i <= arr.length - 1; i++)
{
    arr[i] = s.nextInt();
}
```

- `Scanner s = new Scanner(System.in);` → Creates a Scanner object to read input.
- `size = s.nextInt();` → Reads the array size.
- `int arr[] = new int[size];` → Declares an array of given size.
- The `for` loop iterates from `0` to `size - 1`, reading array elements one by one.

---

### **4. Sorting the Array using Nested Loops**
```java
for(int i = 0; i <= arr.length - 1; i++)
{
    for(int j = 0; j <= i - 1; j++)
    {
        if(arr[j] > arr[i])
        {
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
    }
}
```
#### **Outer `for` Loop**
- Runs from `i = 0` to `arr.length - 1`.
- Controls the passes required to sort the array.

#### **Inner `for` Loop**
- Runs from `j = 0` to `i - 1`.
- Compares elements and swaps them if necessary.
- **Issue:** The logic is incorrect for sorting; it should use `arr.length - 1` and proper iteration. A better approach would be using `Arrays.sort(arr);`

#### **`if` Condition**
- `if(arr[j] > arr[i])` checks if the previous element is greater than the current element.
- If true, it swaps `arr[j]` and `arr[i]`.

#### **Swapping Logic**
- `int temp = arr[i];` → Stores `arr[i]` in `temp`.
- `arr[i] = arr[j];` → Assigns `arr[j]` to `arr[i]`.
- `arr[j] = temp;` → Assigns `temp` to `arr[j]`.

---

### **5. Finding Largest and Second Largest Elements**
```java
int largest = arr[arr.length - 1];
System.out.println("Largest Element:-" + largest);
System.out.println("Second Largest Element:-" + arr[arr.length - 2]);
```

- `largest = arr[arr.length - 1];` → Assigns the last element (largest) to `largest`.
- `arr[arr.length - 2]` → Second last element is the second largest.
- The program prints both values.

## **Example Execution**
### **Input:**
```
Enter the Size
5
Enter the Elements
10 20 30 40 50
```
### **Output:**
```
Largest Element:-50
Second Largest Element:-40
```

---

## **Conclusion**
This Java program demonstrates fundamental array operations, nested loops, and conditional logic. While functional, the sorting approach should be improved for efficiency. Proper error handling should be added to manage edge cases gracefully.

---

## Clone
```
git clone https://github.com/Ananthadatta02/Java-Largest_Element_In_Array.git
```
