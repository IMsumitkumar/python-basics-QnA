## Set

### 1. What is a set in Python and how is it different from a list or tuple?

  A set in Python is a collection of unique items. It is different from a list or tuple because it does not allow duplicate items and is unordered. For example, you can have a set of numbers like {1, 2, 3} but you cannot have duplicate numbers in it like {1, 2, 3, 3}.

### 2. How do you create a set in Python?
  To create a set in Python, you use the curly brackets {} and put the items inside. For

  example, you can create a set of numbers like this:

  `numbers = {1, 2, 3}`

### 3. What are the methods available for adding and removing elements from a set in Python?

To add an element to a set, you can use the "add" method. For example:

`numbers.add(4)`

To remove an element from a set, you can use the `remove` method. However, if the element is not present in the set, it will raise a "KeyError". So, you can use `discard` method it will not raise any error if element is not present in the set.

### 4. How do you check if an item is present in a set in Python?
To check if an item is present in a set, you can use the "in" keyword. For example:

`print(4 in numbers) # True`

### 5. How do you find the length of a set in Python?

To find the length of a set, you can use the "len" function. For example:

`print(len(numbers)) # 4`

### 6. How do you perform union and intersection operations on sets in Python?

- To perform union operation on sets, you can use the "|" operator or the "union" method. For example:
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
```
```python
## using the "|" operator

union_set = set1 | set2
print(union_set) # {1, 2, 3, 4, 5}

## using the "union" method

union_set = set1.union(set2)
print(union_set) # {1, 2, 3, 4, 5}
```

- To perform intersection operation on sets, you can use the "&" operator or the "intersection" method. For example:

```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}

## using the "&" operator

intersection_set = set1 & set2
print(intersection_set) # {2, 3}

## using the "intersection" method

intersection_set = set1.intersection(set2)
print(intersection_set) # {2, 3}
```

### 7. How do you compare two sets in Python?
To compare two sets, you can use the "==" operator. For example:

```python
set1 = {1, 2, 3}
set2 = {1, 2, 3}

print(set1 == set2) # True
```
### 8
### 9. How do you remove all elements from a set in Python?
To remove all elements from a set, you can use the "clear" method. For example:

```python
numbers = {1, 2, 3}
numbers.clear()
print(numbers) # set()
```


### 10. How do you check if one set is a subset of another set in Python?

A subset is a set that contains only elements that are also in another set. To check if a set is a subset of another set, we can use the `issubset()` method. This method will return `True` if all the elements of the set being checked are present in the other set and `False` otherwise. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {1, 2, 3, 4, 5}
set3 = {4, 5, 6}

print(set1.issubset(set2)) # True
print(set1.issubset(set3)) # False
```


### 11. How do you check if a set is disjoint with another set in Python?

Two sets are disjoint if they have no common elements. To check if a set is disjoint with another set, we can use the `isdisjoint()` method. This method will return `True` if the sets have no common elements, and `False` otherwise. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {4, 5, 6}
set3 = {3, 4, 5}

print(set1.isdisjoint(set2)) # True
print(set1.isdisjoint(set3)) # False
```

In the above example, we created three sets `set1`, `set2`, `set3`. We then checked if set1 is disjoint with set2 using `isdisjoint()` method which will return True and set1 is not disjoint with set3 which will return False because both set have common element 3.

### 12. How do you perform set difference in Python?

The set difference is the operation of finding the difference between two sets. To perform a set difference, we can use the `-` operator or the `difference()` method. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}

# using the "-" operator
diff_set = set1 - set2
print(diff_set) # {1}

# using the "difference" method
diff_set = set1.difference(set2)
print(diff_set) # {1}
```

In the above example, we created two sets `set1`, `set2`. We then perform set difference between set1 and set2 using `-` operator and `difference()` method. The result of the set difference is {1} which is present in set1 but not in set2

### 13. How do you copy a set in Python?

To copy a set in Python, we can use the `copy()` method. This method returns a new set with a copy of the elements in the original set. Here's an example:

```python
original_set = {1, 2, 3}
copy_set = original_set.copy()

print(original_set) # {1, 2, 3}
print(copy_set) # {1, 2, 3}
```

In the above example, we created a set `original_set` and then created a copy of that set using `copy()` method. The two sets original_set and copy_set are identical

### 14. How do you update a set in Python?

To update a set in Python, we can use the `update()` method. This method adds all the elements from another set to the original set. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

set1.update(set2)
print(set1) # {1, 2, 3, 4, 5}
```

In the above example, we created two sets `set1`, `set2`. We then update set1 with set2 using `update()` method. The updated set1 will contain all the elements of both set1 and set2, so the final set will be {1, 2, 3, 4, 5}.

### 15. How do you use set comprehensions in Python?

Set comprehensions are a concise way to create sets using a single line of code. They have a similar syntax to list comprehensions, but with curly brackets {} instead of square brackets []. Here's an example:

```makefile
numbers = [1, 2, 3, 4, 5]
squared_numbers = {x**2 for x in numbers}

print(squared_numbers) # {1, 4, 9, 16, 25}
```

In the above example, we created a list `numbers` and then used a set comprehension to create a set of the squared values of each element in the list. The final set will be {1, 4, 9, 16, 25}

`It is important to note that the elements of set are unique and unordered.`


### 16. How do you convert a list to a set in Python?

To convert a list to a set in Python, we can use the `set()` constructor. Here's an example:

```python
numbers = [1, 2, 3, 1, 2, 3]
unique_numbers = set(numbers)

print(unique_numbers) # {1, 2, 3}
```

In the above example, we created a list `numbers` which contains some duplicate values. We then used the `set()` constructor to convert the list to a set, which automatically removes duplicate values and the final set will be {1, 2, 3}

### 17. How do you convert a tuple to a set in Python?

To convert a tuple to a set in Python, we can use the `set()` constructor. Here's an example:

```python
numbers = (1, 2, 3, 1, 2, 3)
unique_numbers = set(numbers)

print(unique_numbers) # {1, 2, 3}
```

In the above example, we created a tuple `numbers` which contains some duplicate values. We then used the `set()` constructor to convert the tuple to a set, which automatically removes duplicate values and the final set will be {1, 2, 3}

### 18. How do you convert a set to a list in Python?

To convert a set to a list in Python, we can use the `list()` constructor. Here's an example:

```python
numbers = {1, 2, 3}
number_list = list(numbers)

print(number_list) # [1, 2, 3]
```

In the above example, we created a set `numbers` and then used the `list()` constructor to convert the set to a list. The final list will be [1, 2, 3]

### 19. How do you convert a set to a tuple in Python?

To convert a set to a tuple in Python, we can use the `tuple()` constructor. Here's an example:

```python
numbers = {1, 2, 3}
number_tuple = tuple(numbers)

print(number_tuple) # (1, 2, 3)
```

In the above example, we created a set `numbers` and then used the `tuple()` constructor to convert the set to a tuple. The final tuple will be (1, 2, 3)

### 20. How do you perform set symmetric difference in Python?

The symmetric difference of two sets is the set of elements that are in either set but not in their intersection. To perform a set symmetric difference, we can use the `^` operator or the `symmetric_difference()` method. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}

# using the "^" operator
symmetric_diff_set = set1 ^ set2
print(symmetric_diff_set) # {1, 4}

# using the "symmetric_difference" method
symmetric_diff_set = set1.symmetric_difference(set2)
print(symmetric_diff_set) #
```

### 21. How do you remove an element from a set in Python?

To remove an element from a set in Python, we can use the `remove()` method. This method raises an error if the element is not found in the set. Here's an example:

```python
numbers = {1, 2, 3}
numbers.remove(2)

print(numbers) # {1, 3}
```

In the above example, we created a set `numbers` and then remove element 2 from it using `remove()` method. The final set will be {1,3}

### 22. How do you add multiple elements to a set in Python?

To add multiple elements to a set in Python, we can use the `update()` method. This method takes an iterable (list, tuple, set, etc.) and adds all its elements to the set. Here's an example:

```python
numbers = {1, 2, 3}
numbers.update([3, 4, 5])

print(numbers) # {1, 2, 3, 4, 5}
```

In the above example, we created a set `numbers` and then add multiple element [3, 4, 5] to it using `update()` method. The final set will be {1, 2, 3, 4, 5}

### 23. How do you remove multiple elements from a set in Python?

To remove multiple elements from a set in Python, we can use the `difference_update()` method. This method takes an iterable (list, tuple, set, etc.) and removes all its elements from the set. Here's an example:

```python
numbers = {1, 2, 3, 4, 5}
numbers.difference_update([3, 4])

print(numbers) # {1, 2, 5}
```

In the above example, we created a set `numbers` and then remove multiple elements [3, 4] from it using `difference_update()` method. The final set will be {1, 2, 5}

### 24. How do you find the difference between two sets in Python?

To find the difference between two sets in Python, we can use the `difference()` method. This method returns a new set containing all the elements of the first set that are not in the second set. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}

diff_set = set1.difference(set2)
print(diff_set) # {1}
```

In the above example, we created two sets `set1` and `set2`. We then found the difference between the two sets using the `difference()` method. The final set will be {1}, which contains all the elements of set1 that are not in set2.

It's important to note that the `difference()` method returns a new set and does not modify the original sets.


### 25. How do you find the intersection of two sets in Python?

To find the intersection of two sets in Python, we can use the `intersection()` method. This method returns a new set containing all the elements that are common to both sets. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}

intersection_set = set1.intersection(set2)
print(intersection_set) # {2, 3}
```

In the above example, we created two sets `set1` and `set2`. We then found the intersection of the two sets using the `intersection()` method. The final set will be {2, 3}, which contains all the elements that are common to both set1 and set2.

### 26. How do you find the union of two sets in Python?

To find the union of two sets in Python, we can use the `union()` method. This method returns a new set containing all the elements from both sets. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

union_set = set1.union(set2)
print(union_set) # {1, 2, 3, 4, 5}
```

In the above example, we created two sets `set1` and `set2`. We then found the union of the two sets using the `union()` method. The final set will be {1, 2, 3, 4, 5}, which contains all the elements from both set1 and set2.

### 27. How do you check if two sets are equal in Python?

To check if two sets are equal in Python, we can use the `==` operator. This operator returns `True` if the two sets have the same elements, and `False` otherwise. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {3, 2, 1}
set3 = {1, 2, 3, 4}

print(set1 == set2) # True
print(set1 == set3) # False
```

In the above example, we created three sets `set1`, `set2`, `set3`. We then used the `==` operator to check if set1 is equal to set2 and set3. The operator returns True for set1 and set2 as both sets contain same elements, but returns False for set1 and set3 as both sets contain different elements

### 28. How do you check if two sets are not equal in Python?

To check if two sets are not equal in Python, we can use the `!=` operator. This operator returns `True` if the two sets have different elements, and `False` otherwise. Here's an example:

```python
set1 = {1, 2, 3}
set2 = {3, 2, 1}
set3 = {1, 2, 3, 4}

print(set1 != set2) # False
print(set1 != set3) # True
```

In the above example, we created three sets `set1`, `set2`, `set3`. We then used the `!=` operator to check if set1 is not equal to set2 and set3. The operator returns False for set1 and set2 as both sets contain same elements, but returns True for set1 and set3 as both sets contain different elements

### 29. How do you check if a set is empty in Python?

To check if a set is empty in Python, we can use the `len()` function or the `not` keyword. Here's an example:

```python
numbers = set()

print(len(numbers) == 0) # True
print(not numbers) # True
```

In the above example, we created an empty set `numbers`. We then used the `len()` function to check if the set has a length of 0, which returns `True`. We also used the `not` keyword to check if the set is empty, which also returns `True`.
