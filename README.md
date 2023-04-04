# Time Complexity and Big O Notation
Time complexity is an important concept in computer science that refers to the amount of time it takes for an algorithm or program to run as a function of its input size. In this tutorial, I will explore the time complexity of loops, nested loops, if-else statements, and different Python data structures, and discuss which ones are optimized for various use cases.

## Time Complexity of Loops

Loops are a common programming construct used to repeat a block of code a certain number of times. The time complexity of a loop depends on the number of times the loop runs as a function of its input size.

### Example: Simple for loop

    for i in range(n):
        print(i)

The time complexity of this loop is O(n), where n is the input size. This is because the loop runs exactly n times, printing the value of i each time.

### Example: Nested for loops

    for i in range(n):
	    for j in range(n):
	        print(i, j)

The time complexity of this loop is O(n^2), because the loop runs n^2 times. This is because for each value of i, the inner loop runs n times, so the total number of iterations is n * n = n^2.

## Time Complexity of If-Else Statements

If-else statements are used to conditionally execute code based on a given condition. The time complexity of an if-else statement is typically O(1), as the code will only execute once regardless of the input size.

### Example: Simple if-else statement

	if x > 0:
	    print("x is positive")
	else:
	    print("x is non-positive")

The time complexity of this if-else statement is O(1), as the code inside the if or else block will only execute once.

### Example: Nested if-else statements
	if x > 0:
	    if y > 0:
	        print("x and y are positive")
	    else:
	        print("x is positive, y is non-positive")
	else:
	    print("x is non-positive")

The time complexity of this nested if-else statement is still O(1), as the code inside the if or else blocks will only execute once.

## Time Complexity of Python Data Structures

Different Python data structures have different time complexities for common operations such as accessing, inserting, and deleting elements.

### Lists

Lists are a common data structure in Python that can hold a sequence of elements. Lists are implemented as an array, and have the following time complexities:

-   Accessing an element by index: O(1)
-   Appending an element: O(1)
-   Inserting an element at a specific index: O(n)
-   Removing an element: O(n)
-   Sorting the list: O(n log n)

		my_list = [1, 2, 3, 4, 5]
		
		print(my_list[0])     # O(1)
		
		my_list.append(6)     # O(1)
		
		my_list.insert(2, 7)  # O(n)
		
		my_list.remove(3)     # O(n)
		
		my_list.sort()        # O(n log n)

### Tuples

Tuples are similar to lists, but are immutable (i.e. cannot be changed after creation). Tuples have the following time complexities:

-   Accessing an element by index: O(1)

		my_tuple = (1, 2, 3, 4, 5)
		print(my_tuple[0])  # O(1)

### Dictionaries

Dictionaries are a data structure that maps keys to values. Dictionaries are implemented as a hash table, and have the following time complexities:

-   Accessing a value by key: O(1)
-   Inserting a new key-value pair: O(1)
-   Deleting a key-value pair: O(1)

		my_dict = {"apple": 1, "banana": 2, "orange": 3} 
		  
		print(my_dict["banana"])  # O(1)
		my_dict["grape"] = 4      # O(1)
		del my_dict["orange"]     # O(1)

### Sets

Sets are a data structure that holds a collection of unique elements. Sets are implemented as a hash table, and have the following time complexities:

-   Adding an element: O(1)
-   Checking if an element is in the set: O(1)
-   Removing an element: O(1)

		my_set = {1, 2, 3, 4, 5}
		
		my_set.add(6)       # O(1)
		print(2 in my_set)  # O(1)
		my_set.remove(3)    # O(1)

### Which Data Structure to Use

Choosing the right data structure for a given problem depends on the specific requirements of the problem and the expected input size. Generally, if quick access or modification of elements is required, lists and dictionaries are good choices. If uniqueness of elements is required, sets should be used. If the elements cannot be changed after creation, tuples should be used.

## Conclusion

Understanding time complexity is important for designing efficient algorithms and choosing appropriate data structures for different use cases. By knowing the time complexity of loops, if-else statements, and Python data structures, we can make informed decisions about which algorithms and data structures to use to optimize performance.