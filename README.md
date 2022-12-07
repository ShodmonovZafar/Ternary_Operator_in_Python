# Ternary Operator in Python

Ternary operators are also known as conditional expressions are operators that evaluate something based on a condition being true or false. It was added to Python in version 2.5. 
It simply allows testing a condition in a single line replacing the multiline if-else making the code compact.

#### Syntax : 

```[on_true] if [expression] else [on_false] ```

* Simple Method to use ternary operator:

```
# Program to demonstrate conditional operator
a, b = 10, 20

# Copy value of a in min if a < b else copy b
min = a if a < b else b

print(min)
```
#### Output:
```10```

* Direct Method by using tuples, Dictionary, and lambda

```
# Python program to demonstrate ternary operator
a, b = 10, 20

# Use tuple for selecting an item
# (if_test_false,if_test_true)[test]
# if [a<b] is true it return 1, so element with 1 index will print
# else if [a<b] is false it return 0, so element with 0 index will print
print( (b, a) [a < b] )

# Use Dictionary for selecting an item
# if [a < b] is true then value of True key will print
# else if [a<b] is false then value of False key will print
print({True: a, False: b} [a < b])

# lambda is more efficient than above two methods
# because in lambda we are assure that
# only one expression will be evaluated unlike in
# tuple and Dictionary
print((lambda: b, lambda: a)[a < b]())

```

#### Output:
```
10
10
10
```

Time Complexity: O(1)

Auxiliary Space: O(1)