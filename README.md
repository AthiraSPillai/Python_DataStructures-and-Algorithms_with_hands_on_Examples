## Learn Data Structures in python with hands-on examples

The data structures in python can be broadly classified as Primitive and Non-primitive.![data_structures%20in%20python.PNG](attachment:data_structures%20in%20python.PNG)
                            ref:https://www.datacamp.com/community/tutorials


### Primitive Data Structures
These are the most primitive or the basic data structures. They are the building blocks for data manipulation and contain pure, simple values of a data. Python has four primitive variable types:

1) Integers
2) Float
3) Strings
4) Boolean

#### i) Integers
Integer represent numeric data or whole numbers from negative infinity to infinity, eg: 10, 3, or -5.



```python
a=10
b=-5
#multiplication
print(a*b)

#addition
print(a+b)

#substraction
print(a-b)

# Returns the quotient
print(a/b)

# Returns the remainder
print(a % b)

# Absolute value
print(abs(a))


# a to the power b
print(b**a)

```

    -50
    5
    15
    -2.0
    0
    10
    9765625
    

####  ii) Float
Floating point numbers or float represents rational numbers,i.e. usually numbers with a decimal figure, eg: 3.14, 1.998


```python
# Floats
x = 2.0
y = 5.0

# Addition
print(x + y)

# Subtraction
print(x - y)

# Multiplication
print(x * y)

# Returns the quotient
print(x / y)

# Returns the remainder
print(x % y) 

# Absolute value
print(abs(x))

# x to the power y
print(x ** y)
```

    7.0
    -3.0
    10.0
    0.4
    2.0
    2.0
    32.0
    

#### Strings
Strings are collections of alphabets, words or other characters. In Python, you can create strings by enclosing a sequence of characters within a pair of single or double quotes. eg: 'test', "learning". Python has many built-in methods or helper functions to manipulate strings. Replacing a substring, capitalising certain words in a paragraph, finding the position of a string within another string are some common string manipulations


```python
position="Developer"
location='Toronto'

### concatenate(+)
print(position +' located in '+location )

#Operations on Strings

### Repeat(*)
print(position*2)

### Range Slicing([:])
print(position[2:5])

### Capitalize strings
print(position.capitalize())

### Retrive length of  the string(len())
print(len(position))

### Check whether a string consists of only digits(.isdigit())

print(position.isdigit())

### Replace parts of strings with other strings(.replace())
print(position.replace('er','---replaced--' ))

### Find substrings in other strings; Returns the lowest index or position within the string at which the substring is found:

sub_string='elo'
print(position.find(sub_string))

```

    Developer located in Toronto
    DeveloperDeveloper
    vel
    Developer
    9
    False
    Develop---replaced--
    3
    

#### Boolean
This built-in data type that can take up the values: True and False


```python
x=10
y=2
print(x>y)
```

    True
    

#### Data Type Conversion
To check the type of an object in Python, use the built-in type() function.
There can be two kinds of data conversions possible: implicit termed as coercion and explicit, often referred to as casting.

##### 1. Implicit Data Type Conversion : 
This is an automatic data conversion and the compiler handles this for you


##### 2. Explicit Data Type Conversion :
This type of data type conversion is user defined using  built-in data conversion functions that you can use here are: int(), float(), and str()


```python
##### 1. Implicit Data Type Conversion : 

x = 8.0 

# An integer
y = 2 

# Divide x by y- compiler automatically convert integer to float to allow float division
z = x/y

# Check the type of z
type(z)
```




    float




```python
##### 2. Explicit Data Type Conversion :

x = 1
y = "Number of certification: "
fav_movie = (y) + str(x)
print(fav_movie)
```

    Number of certification: 1
    

### Non-primitive Data Structures
These include:

##### 1) Built-in data Structure
##### 2) User defined data Structures

#### Built-in data Structures
Buit in Data Structures include : 

##### 1. List 
Lists in Python are used to store collection of heterogeneous items. These are mutable, which means that you can change their content without changing their identity. You can recognize lists by their square bracket [] that hold elements, separated by a comma ,. Lists are built into Python: you do not need to invoke them separately.They are ordered sequence and elements can be accessed by their index values.

ordered, mutable, []

##### 2. Dictionary 
Dictionaries are made up of key-value pairs. key is used to identify the item and the value holds as the name suggests, the value of the item like {key:value},they are  mutable and unordered.

unordered, mutable,{key:value}


##### 3. Set
Sets are a collection of distinct (unique) objects. These are useful to create lists that only hold unique values in the dataset. It is an unordered collection but a mutable one, this is very helpful when going through a huge dataset.

unordered, unique elements,mutable,{}

##### 4. Tuple
They are same like list but the  difference between tuples and list is that tuples are immutable, which means once defined you cannot delete, add or edit any values inside it.Tuple is faster than list.

ordered, immutable,()


##### 5. Array 
All the entries in an array must be of the same data type.For Python, arrays can be seen as a more efficient way of storing a certain kind of list(of same data types). In Python, arrays are supported by the array module and need to be imported before you start inititalizing and using them. The elements stored in an array are constrained in their data type. The data type is specififed during the array creation and specified using a type code, which is a single character usually."I" for integer, "u" for unicode and "f" for float.NumPy arrays are very heavily used in the data science world to work with multidimensional arrays. They are more efficient than the array module and Python lists in general. Reading and writing elements in a NumPy array is faster, and they support "vectorized" operations such as elementwise addition.Commonly used arrays include
1. 2D Array
2. Matrix


```python
##### 1. List 

## Declare a list

# Empty list
x = [] 
print(type(x))

#Homogeneous List
x1 = [1,2,3]
print(type(x1))

# Heterogeneous list
x2 = list([1,'apple',3])
type(x2)

## Operations on List

x=[1,2,'python',10.5, 'java']

# Accessing element of a list using index
print(x[0])

# Update the value of a list using index method
x[1] = 3.0
print(x)

# 1. Adding new items to a list using .append(). By default, this number will be added to the end of the list.
#NOTE: append is a mutating (destructive) operation (it modifies the list in place instead of of returning a new list) and if you do an inline printing eg: print(x.append(10), it returns None)
x.append(11)
print(x)

# 2. Inserting an element using insert(index,value) at index or particular position in list.#NOTE: insert is a mutating (destructive) operation (it modifies the list in place instead of of returning a new list) and if you do an inline printing eg: print(x.insert(3,10), it returns None)
x.insert(5,7)
print(x)

# 3. Removing an items from a list
x.remove('java')
print(x)

#4.Remove the item at a particular index  from list
x.pop(2) # Removes the item at the specified inde position i.e  2 if index leaves blank it removes last item of the list
print(x)

# 5.  Sorting or reversing a list 
x.sort() # In-place sorting,sort is a mutating (destructive) operation
print(x)

# Reverse a list
x.reverse()
print(x)

```

    <class 'list'>
    <class 'list'>
    1
    [1, 3.0, 'python', 10.5, 'java']
    [1, 3.0, 'python', 10.5, 'java', 11]
    [1, 3.0, 'python', 10.5, 'java', 7, 11]
    [1, 3.0, 'python', 10.5, 7, 11]
    [1, 3.0, 10.5, 7, 11]
    [1, 3.0, 7, 10.5, 11]
    [11, 10.5, 7, 3.0, 1]
    


```python
##### 2. Dictionary 
x_dict = {'Developer':1, 'Tester':2, 'Devops':3, 'Admin':4}

# Delete an item from dictionary by key
del x_dict['Developer']
print(x_dict)

#Access element by key
print(x_dict['Tester'])

# Find number of itens/length of dictionary
print(len(x_dict))

# Get all they keys of dictionary
print(x_dict.keys())

# Get all they values of dictionary
print(x_dict.values())




```

    {'Tester': 2, 'Devops': 3, 'Admin': 4}
    2
    3
    dict_keys(['Tester', 'Devops', 'Admin'])
    


```python
##### 3. Set
x_set = set('CAKE&COKE')
y_set = set('COOKIE')

print(x_set)
print(y_set) # Single unique 'o' and unorderd
print(x_set - y_set) # All the elements in x_set but not in y_set
print(x_set|y_set) # Unique elements in x_set or y_set or both
print(x_set & y_set) # Elements in both x_set and y_set
```

    {'&', 'O', 'E', 'K', 'C', 'A'}
    {'O', 'E', 'K', 'C', 'I'}
    {'&', 'A'}
    {'&', 'O', 'E', 'K', 'C', 'A', 'I'}
    {'K', 'C', 'O', 'E'}
    


```python
##### 4. Tuple
x_tuple = 1,2,3,4,5
y_tuple = ('c','a','k','e')
print(x_tuple[0])

# Cannot change values inside a tuple
x_tuple[0] = 0 ## gives error bcz its immutable`

```

    1
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-104-22d6d77f2408> in <module>
          5 
          6 # Cannot change values inside a tuple
    ----> 7 x_tuple[0] = 0 ## gives error bcz its immutable`
    

    TypeError: 'tuple' object does not support item assignment



```python
##### 5. Array :
import array as arr
a = arr.array("u",['3','6','9'])
type(a)

# With arrays, you can perform an operations on all its item individually easily, which may not be the case with lists
array_char = arr.array("u",["c","a","t","s"])
array_char.tostring()
print(array_char)


## the same can be done in list using the below code
l=['c','a','t','s']
listToStr=''.join(str(ele) for ele in l)
print(listToStr)
# or 
listToStr = ''.join(map(str, l)) 
print(listToStr)


## NumPy array
import numpy as np
arr_a = np.array([3, 6, 9])
arr_b = arr_a/3 # Performing vectorized (element-wise) operations 
print(arr_b)
arr_ones = np.ones(4)
print(arr_ones)
multi_arr_ones = np.ones((3,4)) # Creating 2D array with 3 rows and 4 columns
print(multi_arr_ones)

#2D Array
#Two dimensional array is an array within an array. It is an array of arrays
multi_array = [[11, 12, 5, 2], [15, 6,10], [10, 8, 12, 5], [12,15,8,6]]
from array import *

multi_array = [[11, 12, 5, 2], [15, 6,10], [10, 8, 12, 5], [12,15,8,6]]

print(multi_array[0])

print(multi_array[1][2])

for row in multi_array:
    for column in row:
        print(column,end=" ")
    print()
# Python’s print() function comes with a parameter called ‘end’. By default, the value of this parameter is ‘\n’, i.e. the new line character. You can end a print statement with any character/string using this parameter.


#insert an element to 2D array
multi_array.insert(2, [0,5,11,13,6])

#Delete an element from 2D array
del multi_array[3]


#Update an element in 2D array

multi_array[2] = [11,9]
multi_array[0][3] = 7

#Matrix - Matrix is a special case of two dimensional array where each data element is of strictly same size

# reshaping to a matrix
from numpy import * 
weekly_data = array([['Mon',18,20,22,17],['Tue',11,18,21,18],
        ['Wed',15,21,20,19],['Thu',11,20,22,21],
        ['Fri',18,17,23,22],['Sat',12,22,20,18],
        ['Sun',13,15,19,16]])
    
matrix = reshape(weekly_data,(7,5))
print(matrix)

# Accessing values in matrix
print(matrix[2])

# Print data for friday evening
print(matrix[4][3])

#Adding a row
matrix_row_added = append(matrix,[['Avg',12,15,13,11]],0)
print(matrix_row_added)


#Adding a column
matrix_column_added = insert(matrix,[5],[[1],[2],[3],[4],[5],[6],[7]],1)
print(matrix_column_added)

#Delete a row form a Matrix
# We can delete a row from a matrix using the delete() method. We have to specify the index of the row and also the axis value which is 0 for a row and 1 for a column.
matrix_row_deleted = delete(matrix,[2],0)
print(matrix_row_deleted)

#Delete a column from a Matrix
matrix_column_deleted = delete(matrix,s_[2],1)
print(matrix_column_deleted)

#Update a row in in a Matrix
matrix[3] = ['Thu',0,0,0,0]
print(matrix)


```

    array('u', 'cats')
    cats
    cats
    [1. 2. 3.]
    [1. 1. 1. 1.]
    [[1. 1. 1. 1.]
     [1. 1. 1. 1.]
     [1. 1. 1. 1.]]
    [11, 12, 5, 2]
    10
    11 12 5 2 
    15 6 10 
    10 8 12 5 
    12 15 8 6 
    [['Mon' '18' '20' '22' '17']
     ['Tue' '11' '18' '21' '18']
     ['Wed' '15' '21' '20' '19']
     ['Thu' '11' '20' '22' '21']
     ['Fri' '18' '17' '23' '22']
     ['Sat' '12' '22' '20' '18']
     ['Sun' '13' '15' '19' '16']]
    ['Wed' '15' '21' '20' '19']
    23
    [['Mon' '18' '20' '22' '17']
     ['Tue' '11' '18' '21' '18']
     ['Wed' '15' '21' '20' '19']
     ['Thu' '11' '20' '22' '21']
     ['Fri' '18' '17' '23' '22']
     ['Sat' '12' '22' '20' '18']
     ['Sun' '13' '15' '19' '16']
     ['Avg' '12' '15' '13' '11']]
    [['Mon' '18' '20' '22' '17' '1']
     ['Tue' '11' '18' '21' '18' '2']
     ['Wed' '15' '21' '20' '19' '3']
     ['Thu' '11' '20' '22' '21' '4']
     ['Fri' '18' '17' '23' '22' '5']
     ['Sat' '12' '22' '20' '18' '6']
     ['Sun' '13' '15' '19' '16' '7']]
    [['Mon' '18' '20' '22' '17']
     ['Tue' '11' '18' '21' '18']
     ['Thu' '11' '20' '22' '21']
     ['Fri' '18' '17' '23' '22']
     ['Sat' '12' '22' '20' '18']
     ['Sun' '13' '15' '19' '16']]
    [['Mon' '18' '22' '17']
     ['Tue' '11' '21' '18']
     ['Wed' '15' '20' '19']
     ['Thu' '11' '22' '21']
     ['Fri' '18' '23' '22']
     ['Sat' '12' '20' '18']
     ['Sun' '13' '19' '16']]
    [['Mon' '18' '20' '22' '17']
     ['Tue' '11' '18' '21' '18']
     ['Wed' '15' '21' '20' '19']
     ['Thu' '0' '0' '0' '0']
     ['Fri' '18' '17' '23' '22']
     ['Sat' '12' '22' '20' '18']
     ['Sun' '13' '15' '19' '16']]
    

### II) User-Defined data structures


#### a) Linear Data Sltructures

##### Stack
A stack is a container of objects that are inserted and removed according to the Last-In-First-Out (LIFO) concept. In computer science, this concept is used for evaluating expressions and syntax parsing, scheduling algortihms/routines, etc.
Stacks can be implemented using lists in Python. When you add elements to a stack, it is known as a push operation, whereas when you remove or delete an element it is called a pop operation. Note that you have actually have a pop() method at your disposal when you're working with stacks in Pytho.

linear, last in-first out(LIFO),array structure, push, pop,recursive and reversal operation,only performed on top


##### Queue
A queue is a container of objects that are inserted and removed according to the First-In-First-Out (FIFO) principle.Lists are not efficient to implement a queue, because append() and pop() from the end of a list is not fast and incur a memory movement cost. Also, insertion at the end and deletion from the beginning of a list is not so fast since it requires a shift in the element positions.

linear, first in-first out(FIFO), array structures, operations can be performed on both ends(tail and head),enqueue(add element) and dequeue(delete element). Network buffer , job scheduling

#### b)Non-Linear Data Structures

##### Graph
A graph in mathematics and computer science are networks consisting of nodes, also called vertices which may or may not be connected to each other. The lines or the path that connects two nodes is called an edge. If the edge has a particular direction of flow, then it is a directed graph, with the direction edge being called an arc. Else if no directions are specified, the graph is called an undirected graph.
Social networks, molecular studies in chemistry and biology, maps, recommender system all rely on graph and graph theory principles.



##### Trees
The root is always at the top of the tree. The other nodes that follow are called the branches with the final node in each branch being called leaves. The root is often called the parent and the nodes that it refers to below it called its children. The nodes with the same parent are called siblings
root (data originate)and nodes(other data point), parent, child and leaves, Trees used  for searching ,html pages
Link-list-linear data structure, not stored consequently but have a pointer to the related one,data and pointer(next), image viewer, music player
Graph-data collection of points(vertices and edges), maps, least path between nodes
Hash maps-same like dictionary, phonebook



```python
#### Stack
# Bottom -> 1 -> 2 -> 3 -> 4 -> 5 (Top)
stack = [1,2,3,4,5] 
stack.append(6) # Bottom -> 1 -> 2 -> 3 -> 4 -> 5 -> 6 (Top)
print(stack)
stack.pop() # Bottom -> 1 -> 2 -> 3 -> 4 -> 5 (Top)
print(stack)
stack.pop() # Bottom -> 1 -> 2 -> 3 -> 4 (Top)
print(stack)
```

    [1, 2, 3, 4, 5, 6]
    [1, 2, 3, 4, 5]
    [1, 2, 3, 4]
    


```python
#### Queue

class Queue:
    
    def __init__(self):
        self.items=[]
    
    def isEmpty(self):
        return self.items==[]

    
    def enqueue(self, val):
        return self.items.insert(0,val)
    
    def dequeue(self):
        return self.items.pop()
    def size(self):
        return len(self.items)
        

q=Queue()   

print(q.size())
print(q.isEmpty())

q.enqueue(8.4)
q.enqueue('QA')
q.enqueue(1)

q.enqueue('CI/CD')

print(q.dequeue())

print(q.size())

```

    0
    True
    8.4
    3
    


```python
#### Graph
graph = { "a" : ["c", "d"],
          "b" : ["d", "e"],
          "c" : ["a", "e"],
          "d" : ["a", "b"],
          "e" : ["b", "c"]
        }

def define_edges(graph):
    edges = []
    for vertices in graph:
        for neighbour in graph[vertices]:
            edges.append((vertices, neighbour))
    return edges

print(define_edges(graph))
```

    [('a', 'c'), ('a', 'd'), ('b', 'd'), ('b', 'e'), ('c', 'a'), ('c', 'e'), ('d', 'a'), ('d', 'b'), ('e', 'b'), ('e', 'c')]
    


```python
#### Tree
class Tree:
    def __init__(self,info,Left=None,Right=None):
        self.info=info
        self.Left=Left
        self.Right=Right
    def __str__(self):
        return  str('Tree: ' + str(self.info) + ' Left Child : '+str(self.Left) + ' Right Child: '+ str(self.Right))
    
tree=Tree(1,Tree(2,2,3),Tree(3,1,3))
print(tree)
```

    Tree: 1 Left Child : Tree: 2 Left Child : 2 Right Child: 3 Right Child: Tree: 3 Left Child : 1 Right Child: 3
    

####  Other commonly used Data Structures are: 

##### Maps
Python Maps also called ChainMap is a type of data structure to manage multiple dictionaries together as one unit. The combined dictionary contains the key and value pairs in a specific sequence eliminating any duplicate keys. The best use of ChainMap is to search through multiple dictionaries at a time and get the proper key-value pair mapping. We also see that these ChainMaps behave as stack data structure.If there are duplicate keys, then only the value from the first key is preserved.

##### Updating Map
When the element of the dictionary is updated, the result is instantly updated in the result of the ChainMap. In the below example we see that the new updated value reflects in the result without explicitly applying the ChainMap method again.


```python
import collections

dict1 = {'day1': 'Mon', 'day2': 'Tue'}
dict2 = {'day3': 'Wed', 'day1': 'Thu'}

res = collections.ChainMap(dict1, dict2)
print(res)

# Creating a single dictionary
print(res.maps) #returns a list of dictionaries

print('Keys = {}'.format(list(res.keys())))
print('Values = {}'.format(list(res.values())))
print()

# Find a specific value in the result
print('day3 in res: {}'.format(('day1' in res)))
print('day4 in res: {}'.format(('day4' in res)))

```

    ChainMap({'day1': 'Mon', 'day2': 'Tue'}, {'day3': 'Wed', 'day1': 'Thu'})
    [{'day1': 'Mon', 'day2': 'Tue'}, {'day3': 'Wed', 'day1': 'Thu'}]
    Keys = ['day3', 'day1', 'day2']
    Values = ['Wed', 'Mon', 'Tue']
    
    day3 in res: True
    day4 in res: False
    

##### Linked Lists
A linked list is a sequence of data elements, which are connected together via links. Each data element contains a connection to another data element in form of a pointer. Python does not have linked lists in its standard library.
A linked list is created by creating  a Node object and create another class to use this node object. We pass the appropriate values thorugh the node object to point the to the next data elements. The below program creates the linked list with three data elements.Singly linked lists can be traversed in only forwrad direction starting form the first data element. We simply print the value of the next data element by assgining the pointer of the next node to the current data element.


```python
class Node:
    def __init__(self, val=None):
        self.val = val
        self.nextval = None

class LinkedList:
    
    def __init__(self):
        self.rootval = None
    
    def listprint(self):
        printval = self.rootval
        print(printval.val,printval.nextval)
        while printval is not None:
            print (printval.val)
            printval = printval.nextval


t1=Node("Mon")

list1 = LinkedList()
list1.rootval = t1

t2 = Node("Tue")
t3 = Node("Wed")

# Link first Node to second node
list1.rootval.nextval = t2

# Link second Node to third node
t2.nextval = t3

list1.listprint()

```

    Mon <__main__.Node object at 0x05934988>
    Mon
    Tue
    Wed
    


```python

```


```python

```


```python

```

### Algorithms in Python
Algoriths are rules and instructions to solve a specific problems. They should have clear I/O and steps and flexible, defined results.

#### Most popular Algorith classes are:

##### 1. Divide and conquer-divide 
problem is divided into sub part and solve each seperately

##### 2. Dynamic 
It seperate the problems in to different sub problems ,but remember the results of each sub problems and applied to similar ones

##### 3. Greedy
Takes easiest step on solving a complex problem without worrying about the complexity of future steps

##### Tree Traversal
Trees are non-linear data structures- this algorithm visit each node only once in update or check them.

###### i)inorder traversal
leftnode followed by root and then right node)

######  ii)Pre-order traversal
visit root node followed by leftnode and right)

###### iii) post-order traversal
visit leftnode followed by rightnode and then root

##### Sorting algorithm

i) Merge Sort-divide and conquer rule -divide and merge the sorted list
ii) Bubble Sort-progressively compare and swap
iii)Insertion sort-Given a list, take the current element and insert it at the appropriate position of the list, adjusting the list every time you insert. It is similar to arranging the cards in a Card game.
iv)selection sort-Given a list, take the current element and exchange it with the smallest element on the right hand side of the current element.
v)shell sort-Shell Sort is just a variation of Insertion Sort. divide the number of elements /2 to get and sort using insertion sort
Search Algorithms
i) linear search-if key element present return index if element else return -1
ii)Binary search- on sorted array check with middle element, divide by half, check on sub array left/right depending key is greater or less

Ref: https://www.tutorialspoint.com/python_data_structure/python_graph_algorithms.htm

```python

```


```python

```


```python

```


```python

```


```python

```


```python

```
