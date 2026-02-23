# Lab - Lists in Python
Joshua Vega CISC 179

## 1. Lists

**a. Generate 100 integers**
I created the list using `range` and checked the type. Then I used 4 methods from the documentation.

```python
my_list = list(range(100))
print(type(my_list)) # This confirms it is a list

# Using 4 methods
my_list.append(101)    # Adds to the end
my_list.pop()          # Removes the last item
my_list.sort()         # Sorts the list
my_list.reverse()      # Reverses the order

```

b. Move last 3 items to the beginning
I used slicing to take the last part and put it at the front.

```python

items = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
new_list = items[-3:] + items[:-3]
print(new_list)
```

c. Result of len [[1,2]] * 3)

My guess: 3

Python result: 3
Explanation: The list [1,2] is repeated 3 times inside the main list, so it has 3 elements.

d. & e. Memory addresses and Delete
I made the list with duplicates and used id() to see the memory.

```python

my_list_ten = [10, 20, 10, 30, 40, 50, 20, 60, 70, 80]
my_list_ten_mem = []

for x in my_list_ten:
    my_list_ten_mem.append(id(x))

print(my_list_ten_mem)

# Delete the list
del my_list_ten
```

f. New list comparison
I created the list again and compared the IDs.
```python
my_new_list = [10, 20, 10, 30, 40, 50, 20, 60, 70, 80]
for x in my_new_list:
    print(id(x))
    ```

    I see that the memory addresses IDC for the same numbers are the same as before. Python points to the same object in memory for the same integer value to save space.
```python
    import copy
x = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
y = copy.deepcopy(x)

    ```

    h. Multiple expressions in list comprehension?
Yes, it is possible. You can use multiple for or if clauses in one line.

i. Count spaces
```python
phrase = "To be, or not to be, this is the question"
spaces = [s for s in phrase if s == " "]
print("Spaces found:", len(spaces))

```

j. 5 List operations
I picked these 5 from the documentation:

extend(): To add many items from another list.

insert(): To put an item in a specific index.

remove(): To delete an item by its value.

count(): To count how many times a value appears.

clear(): To remove everything from the list.

Challenges
The hardest part was the memory addresses. I was confused why different lists have the same id() for the same numbers, but then I read it is how Python works. Also, I had a problem with point (d) because the instructions said my-list-ten, but Python doesn't allow dashes - in variable names, so I changed it to my_list_ten. The list comprehension was a bit hard to write but it makes the code shorter.
