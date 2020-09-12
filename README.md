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
i. List
ii. Dictionary
iii. Set
iv. Tuple
v. Array


#####  List 
Lists in Python are used to store collection of heterogeneous items. These are mutable, which means that you can change their content without changing their identity. You can recognize lists by their square bracket [] that hold elements, separated by a comma ,. Lists are built into Python: you do not need to invoke them separately.They are ordered sequence and elements can be accessed by their index values.

ordered, mutable, []


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
    

#####  Dictionary 
Dictionaries are made up of key-value pairs. key is used to identify the item and the value holds as the name suggests, the value of the item like {key:value},they are  mutable and unordered.

unordered, mutable,{key:value}


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
    dict_values([2, 3, 4])
    

#####  Set
Sets are a collection of distinct (unique) objects. These are useful to create lists that only hold unique values in the dataset. It is an unordered collection but a mutable one, this is very helpful when going through a huge dataset.

unordered, unique elements,mutable,{}


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

    {'O', 'A', 'E', '&', 'K', 'C'}
    {'O', 'I', 'E', 'K', 'C'}
    {'A', '&'}
    {'O', 'A', 'I', 'E', '&', 'K', 'C'}
    {'C', 'O', 'E', 'K'}
    

##### Tuple
They are same like list but the  difference between tuples and list is that tuples are immutable, which means once defined you cannot delete, add or edit any values inside it.Tuple is faster than list.

ordered, immutable,()



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

    <ipython-input-4-22d6d77f2408> in <module>
          5 
          6 # Cannot change values inside a tuple
    ----> 7 x_tuple[0] = 0 ## gives error bcz its immutable`
    

    TypeError: 'tuple' object does not support item assignment


#####  Array 
All the entries in an array must be of the same data type.For Python, arrays can be seen as a more efficient way of storing a certain kind of list(of same data types). In Python, arrays are supported by the array module and need to be imported before you start inititalizing and using them. The elements stored in an array are constrained in their data type. The data type is specififed during the array creation and specified using a type code, which is a single character usually."I" for integer, "u" for unicode and "f" for float.NumPy arrays are very heavily used in the data science world to work with multidimensional arrays. They are more efficient than the array module and Python lists in general. Reading and writing elements in a NumPy array is faster, and they support "vectorized" operations such as elementwise addition.Commonly used arrays include
1. 2D Array
2. Matrix


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


#Adding a column
matrix_column_added = insert(matrix,[5],[[1],[2],[3],[4],[5],[6],[7]],1)

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
    

##### Maps
Python Maps also called ChainMap is a type of data structure to manage multiple dictionaries together as one unit. The combined dictionary contains the key and value pairs in a specific sequence eliminating any duplicate keys. The best use of ChainMap is to search through multiple dictionaries at a time and get the proper key-value pair mapping. We also see that these ChainMaps behave as stack data structure.Creating a ChainMap
We create two dictionaries and club them using the ChainMap method from the collections library. Then we print the keys and values of the result of the combination of the dictionaries. If there are duplicate keys, then only the value from the first key is preserved.When the element of the dictionary is updated, the result is instantly updated in the result of the ChainMap.


```python
# Maps
import collections

dict1 = {'day1': 'Mon', 'day2': 'Tue'}
dict2 = {'day3': 'Wed', 'day1': 'Thu'}

res = collections.ChainMap(dict1, dict2)

# Creating a single dictionary
print(res.maps,'\n')

print('Keys = {}'.format((res.keys())))
print('Values = {}'.format((res.values())))
print()

# Print all the elements from the result
print('elements:')
for key, val in res.items():
    print('{} = {}'.format(key, val))
print()

# Find a specific value in the result
print('day3 in res: {}'.format(('day1' in res)))
print('day4 in res: {}'.format(('day4' in res)))

 
```

    [{'day1': 'Mon', 'day2': 'Tue'}, {'day3': 'Wed', 'day1': 'Thu'}] 
    
    Keys = KeysView(ChainMap({'day1': 'Mon', 'day2': 'Tue'}, {'day3': 'Wed', 'day1': 'Thu'}))
    Values = ValuesView(ChainMap({'day1': 'Mon', 'day2': 'Tue'}, {'day3': 'Wed', 'day1': 'Thu'}))
    
    elements:
    day3 = Wed
    day1 = Mon
    day2 = Tue
    
    day3 in res: True
    day4 in res: False
    

##### Linked list
A linked list is a sequence of data elements, which are connected together via links. Each data element contains a connection to another data element in form of a pointer. Python does not have linked lists in its standard library. We implement the concept of linked lists using the concept of nodes. 


```python
# Linked list
class Node:
    def __init__(self, dataval=None):
        self.dataval = dataval
        self.nextval = None

class SLinkedList:
    def __init__(self):
        self.headval = None
    def listprint(self):
        printval = self.headval
        while printval is not None:
            print (printval.dataval)
            printval = printval.nextval

list1 = SLinkedList()
list1.headval = Node("Mon")
t2 = Node("Tue")
t3 = Node("Wed")
# Link first Node to second node
list1.headval.nextval = t2

# Link second Node to third node
t2.nextval = t3
list1.listprint()

```

    Mon
    Tue
    Wed
    

##### Hash tables
Hash tables are a type of data structure in which the address or the index value of the data element is generated from a hash function. That makes accessing the data faster as the index value behaves as a key for the data value. In other words Hash table stores key-value pairs but the key is generated through a hashing function.

So the search and insertion function of a data element becomes much faster as the key values themselves become the index of the array which stores the data.

In Python, the Dictionary data types represent the implementation of hash tables. The Keys in the dictionary satisfy the following requirements.

The keys of the dictionary are hashable i.e. the are generated by hashing function which generates unique result for each unique value supplied to the hash function.
The order of data elements in a dictionary is not fixed.


```python
# Declare a dictionary 
dict = {'Name': 'Zaiva', 'Age': 27, 'Job': 'Developer'}

# Accessing the dictionary with its key
print ("dict['Name']: ", dict['Name'])
print ("dict['Age']: ", dict['Age'])

dict['Age'] = 8; # update existing entry
dict['Job'] = "Front-end Developer"; # Add new entry

del dict['Name']; # remove entry with key 'Name'
dict.clear();     # remove all entries in dict
del dict ;        # delete entire dictionary
```

    dict['Name']:  Zaiva
    dict['Age']:  27
    

### II) User-Defined data structures

#### a) Linear Data Sltructures

i. Stack
ii. Queue

#### b)Non-Linear Data Structures
i. Graph
ii. Trees

##### Stack
A stack is a container of objects that are inserted and removed according to the Last-In-First-Out (LIFO) concept. In computer science, this concept is used for evaluating expressions and syntax parsing, scheduling algortihms/routines, etc.
Stacks can be implemented using lists in Python. When you add elements to a stack, it is known as a push operation, whereas when you remove or delete an element it is called a pop operation. Note that you have actually have a pop() method at your disposal when you're working with stacks in Pytho.

linear, last in-first out(LIFO),array structure, push, pop,recursive and reversal operation,only performed on top



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
    

##### Queue
A queue is a container of objects that are inserted and removed according to the First-In-First-Out (FIFO) principle.Lists are not efficient to implement a queue, because append() and pop() from the end of a list is not fast and incur a memory movement cost. Also, insertion at the end and deletion from the beginning of a list is not so fast since it requires a shift in the element positions.

linear, first in-first out(FIFO), array structures, operations can be performed on both ends(tail and head),enqueue(add element) and dequeue(delete element). Network buffer , job scheduling


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
    

##### Deque
A double-ended queue, or deque, supports adding and removing elements from either end. The more commonly used stacks and queues are degenerate forms of deques, where the inputs and outputs are restricted to a single end.


```python
# Deque
import collections

DoubleEnded = collections.deque(["Mon","Tue","Wed"])

DoubleEnded.append("Thu")

print ("Appended at right - ")
print (DoubleEnded)

DoubleEnded.appendleft("Sun")

print ("Appended at right at left is - ")
print (DoubleEnded)

DoubleEnded.pop()

print ("Deleting from right - ")
print (DoubleEnded)

DoubleEnded.popleft()

print ("Deleting from left - ")
print (DoubleEnded)
```

    Appended at right - 
    deque(['Mon', 'Tue', 'Wed', 'Thu'])
    Appended at right at left is - 
    deque(['Sun', 'Mon', 'Tue', 'Wed', 'Thu'])
    Deleting from right - 
    deque(['Sun', 'Mon', 'Tue', 'Wed'])
    Deleting from left - 
    deque(['Mon', 'Tue', 'Wed'])
    

##### Graph
A graph in mathematics and computer science are networks consisting of nodes, also called vertices which may or may not be connected to each other. The lines or the path that connects two nodes is called an edge. If the edge has a particular direction of flow, then it is a directed graph, with the direction edge being called an arc. Else if no directions are specified, the graph is called an undirected graph.
Social networks, molecular studies in chemistry and biology, maps, recommender system all rely on graph and graph theory principles.![graph.PNG](attachment:graph.PNG)



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
    

##### Trees
The root is always at the top of the tree. The other nodes that follow are called the branches with the final node in each branch being called leaves. The root is often called the parent and the nodes that it refers to below it called its children. The nodes with the same parent are called siblings
root (data originate)and nodes(other data point), parent, child and leaves, Trees used  for searching ,html pages
Link-list-linear data structure, not stored consequently but have a pointer to the related one,data and pointer(next), image viewer, music player
Graph-data collection of points(vertices and edges), maps, least path between nodes
Hash maps-same like dictionary, phonebook



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
    

##### Binary Tree
Tree represents the nodes connected by edges. It is a non-linear data structure. It has the following properties.
One node is marked as Root node.
Every node other than the root is associated with one parent node.
Each node can have an arbiatry number of chid node.
We create a tree data structure in python by using the concept os node 


```python
# Create Root
class Node:

    def __init__(self, data):

        self.left = None
        self.right = None
        self.data = data

# Inserting into a Tree
    def insert(self, data):

# Compare the new value with the parent node
        if self.data:
            if data < self.data:
                if self.left is None:
                    self.left = Node(data)
                else:
                    self.left.insert(data)
            elif data > self.data:
                if self.right is None:
                    self.right = Node(data)
                else:
                    self.right.insert(data)
        else:
            self.data = data

# Print the tree
    def PrintTree(self):
        if self.left:
            self.left.PrintTree()
        print( self.data),
        if self.right:
            self.right.PrintTree()

root = Node(10)
root.insert(6)
root.insert(14)
root.insert(3)

root.PrintTree()
```

    3
    6
    10
    14
    

#####  Binary Search Tree
A Binary Search Tree (BST) is a tree in which all the nodes follow the below-mentioned properties − The left sub-tree of a node has a key less than or equal to its parent node's key. The right sub-tree of a node has a key greater than to its parent node's key. Thus, BST divides all its sub-trees into two segments; the left sub-tree and the right sub-tree and can be defined as –

left_subtree (keys)  ≤  node (key)  ≤  right_subtree (keys)
Search for a value in a B-tree
Searching for a value in a tree involves comparing the incoming value with the value exiting nodes. Here also we traverse the nodes from left to right and then finally with the parent. If the searched for value does not match any of the exitign value, then we return not found message else the found message is returned.


```python
# Binary Search Tree
class Node:

    def __init__(self, data):

        self.left = None
        self.right = None
        self.data = data

# Insert method to create nodes
    def insert(self, data):

        if self.data:
            if data < self.data:
                if self.left is None:
                    self.left = Node(data)
                else:
                    self.left.insert(data)
            elif data > self.data:
                if self.right is None:
                    self.right = Node(data)
                else:
                    self.right.insert(data)
        else:
            self.data = data
# findval method to compare the value with nodes
    def findval(self, lkpval):
        if lkpval < self.data:
            if self.left is None:
                return str(lkpval)+" Not Found"
            return self.left.findval(lkpval)
        elif lkpval > self.data:
            if self.right is None:
                return str(lkpval)+" Not Found"
            return self.right.findval(lkpval)
        else:
            print(str(self.data) + ' is found')
# Print the tree
    def PrintTree(self):
        if self.left:
            self.left.PrintTree()
        print( self.data),
        if self.right:
            self.right.PrintTree()


root = Node(12)
root.insert(6)
root.insert(14)
root.insert(3)
print(root.findval(7))
print(root.findval(14))
```

    7 Not Found
    14 is found
    None
    

### Algorithms in Python
Algoriths are rules and instructions to solve a specific problems. They should have clear I/O and steps and flexible, defined results.Algorithm is a step-by-step procedure, which defines a set of instructions to be executed in a certain order to get the desired output. Algorithms are generally created independent of underlying languages, i.e. an algorithm can be implemented in more than one programming language.

#### Most popular Algorith classes are:

##### 2. Dynamic Algorithm
It seperate the problems in to different sub problems ,but remember the results of each sub problems and applied to similar ones

##### 3. Greedy Algorithm
Takes easiest step on solving a complex problem without worrying about the complexity of future steps

##### 1. Divide and conquer-divide 
In divide and conquer approach, the problem in hand, is divided into smaller sub-problems and then each problem is solved independently. When we keep on dividing the subproblems into even smaller sub-problems, we may eventually reach a stage where no more division is possible. Those "atomic" smallest possible sub-problem (fractions) are solved. The solution of all sub-problems is finally merged in order to obtain the solution of an original problem.
-Problem is divided into sub part and solve each seperately



```python
# Divide-and-conquer programming approach where the binary search is implemented
def bsearch(list, val):

    list_size = len(list) - 1

    idx0 = 0
    idxn = list_size
# Find the middle most value

    while idx0 <= idxn:
        midval = (idx0 + idxn)// 2

        if list[midval] == val:
            return midval
# Compare the value the middle most value
        if val > list[midval]:
            idx0 = midval + 1
        else:
            idxn = midval - 1

    if idx0 > idxn:
        return None
# Initialize the sorted list
list = [2,7,19,34,53,72]

# Print the search result
print(bsearch(list,72))
print(bsearch(list,11))
```

##### Recursion Algorithm
Recursion allows a function to call itself. Fixed steps of code get executed again and again for new values.
##### Binary Search using Recursion
We implement the algorithm of binary search using python as shown below. We use an ordered list of items and design a recursive function to take in the list along with starting and ending index as input. Then the binary search function calls itself till find the the searched item or concludes about its absence in the list.


```python
# Binary Search using Recursion
def bsearch(list, idx0, idxn, val):

    if (idxn < idx0):
        return None
    else:
        midval = idx0 + ((idxn - idx0) // 2)
# Compare the search item with middle most value

        if list[midval] > val:
            return bsearch(list, idx0, midval-1,val)
        elif list[midval] < val:
            return bsearch(list, midval+1, idxn, val)
        else:
            return midval

list = [8,11,24,56,88,131]
print(bsearch(list, 0, 5, 24))
print(bsearch(list, 0, 5, 51))
```

    2
    None
    

##### Backtracking Algorithm
Backtracking is a form of recursion. But it involves choosing only option out of any possibilities. We begin by choosing an option and backtrack from it, if we reach a state where we conclude that this specific option does not give the required solution. We repeat these steps by going across each available option until we get the desired solution.


```python
# Backtracking
# Find all possible order of arrangements of a given set of letters all backtracking.
def permute(list, s):
    if list == 1:
        return s
    else:
        return [ y + x
                 for y in permute(1, s)
                 for x in permute(list - 1, s)
                 ]

print(permute(1, ["a","b","c"]))
print(permute(2, ["a","b","c"]))
```

    ['a', 'b', 'c']
    ['aa', 'ab', 'ac', 'ba', 'bb', 'bc', 'ca', 'cb', 'cc']
    

##### Tree Traversal Algorithm
Trees are non-linear data structures- this algorithm visit each node only once in update or check them.
Traversal is a process to visit all the nodes of a tree and may print their values too. Because, all nodes are connected via edges (links) we always start from the root (head) node. That is, we cannot randomly access a node in a tree. There are three ways which we use to traverse a tree:

i. In-order Traversal
ii. Pre-order Traversal
iii. Post-order Traversal

###### In-order Traversal
In this traversal method, the left subtree is visited first, then the root and later the right sub-tree. We should always remember that every node may represent a subtree itself.
###### Left -> Root -> Right

##### Pre-order Traversal
In this traversal method, the root node is visited first, then the left subtree and finally the right subtree.
##### Root -> Left ->Right


##### Post-order Traversal
In this traversal method, the root node is visited last, hence the name. First we traverse the left subtree, then the right subtree and finally the root node.
##### Left ->Right -> Root




```python
class Node:

    def __init__(self, data):

        self.left = None
        self.right = None
        self.data = data
# Insert Node
    def insert(self, data):

        if self.data:
            if data < self.data:
                if self.left is None:
                    self.left = Node(data)
                else:
                    self.left.insert(data)
            elif data > self.data:
                if self.right is None:
                    self.right = Node(data)
                else:
                    self.right.insert(data)
        else:
            self.data = data

# Print the Tree
    def PrintTree(self):
        if self.left:
            self.left.PrintTree()
        print( self.data),
        if self.right:
            self.right.PrintTree()

# Inorder traversal
# Left -> Root -> Right
    def inorderTraversal(self, root):
        res = []
        if root:
            res = self.inorderTraversal(root.left)
            res.append(root.data)
            res = res + self.inorderTraversal(root.right)
        return res

# Preorder traversal
# Root -> Left ->Right
    def PreorderTraversal(self, root):
        res = []
        if root:
            res.append(root.data)
            res = res + self.PreorderTraversal(root.left)
            res = res + self.PreorderTraversal(root.right)
        return res
    

# Postorder traversal
# Left ->Right -> Root
    def PostorderTraversal(self, root):
        res = []
        if root:
            res = self.PostorderTraversal(root.left)
            res = res + self.PostorderTraversal(root.right)
            res.append(root.data)
        return res

root = Node(27)
root.insert(14)
root.insert(35)
root.insert(10)
root.insert(19)
root.insert(31)
root.insert(42)
print(root.inorderTraversal(root))
print(root.PreorderTraversal(root))

```

#### Sorting Algorithms
Sorting refers to arranging data in a particular format. Sorting algorithm specifies the way to arrange data in a particular order. Most common orders are in numerical or lexicographical order.

The importance of sorting lies in the fact that data searching can be optimized to a very high level, if data is stored in a sorted manner. Sorting is also used to represent data in more readable formats. Below we see five such implementations of sorting in python.

i. Bubble Sort
ii. Merge Sort
iii. Insertion Sort
iv. Shell Sort
v. Selection Sort

##### Bubble Sort
It is a comparison-based algorithm in which each pair of adjacent elements is compared and the elements are swapped if they are not in order.Progressively compare adjacent elements and swap


```python
# Bubble Sort
def bubblesort(list):

# Swap the elements to arrange in order
    for iter_num in range(len(list)-1,0,-1):
        for idx in range(iter_num):
            if list[idx]>list[idx+1]:
                temp = list[idx]
                list[idx] = list[idx+1]
                list[idx+1] = temp


list = [19,2,31,45,6,11,121,27]
bubblesort(list)
print(list)
```

    [2, 6, 11, 19, 27, 31, 45, 121]
    

##### Merge Sort
Merge sort first divides the array into equal halves and then combines them in a sorted manner.


```python
#Merge Sort
def merge_sort(unsorted_list):
    if len(unsorted_list) <= 1:
        return unsorted_list
# Find the middle point and devide it
    middle = len(unsorted_list)// 2
    left_list = unsorted_list[:middle]
    right_list = unsorted_list[middle:]
    left_list = merge_sort(left_list)
    right_list = merge_sort(right_list)
    return (merge(left_list, right_list))


# Merge the sorted halves
def merge(left_half,right_half):
    res = []
    while len(left_half) != 0 and len(right_half) != 0:
        if left_half[0] < right_half[0]:
            res.append(left_half[0])
            left_half.remove(left_half[0])
        else:
            res.append(right_half[0])
            right_half.remove(right_half[0])
    if len(left_half) == 0:
        res = res + right_half
    else:
        res = res + left_half
    return res


unsorted_list = [64, 34, 25, 12, 22, 11, 90]
print(merge_sort(unsorted_list))
```

    [11, 12, 22, 25, 34, 64, 90]
    

#### Insertion Sort
Insertion sort involves finding the right place for a given element in a sorted list. So in beginning we compare the first two elements and sort them by comparing them. Then we pick the third element and find its proper position among the previous two sorted elements. This way we gradually go on adding more elements to the already sorted list by putting them in their proper position.Given a list, take the current element and insert it at the appropriate position of the list, adjusting the list every time you insert. It is similar to arranging the cards in a Card game.


```python
#  Insertion Sort
def insertion_sort(InputList):
    for i in range(1, len(InputList)):
        j = i-1
        nxt_element = InputList[i]
# Compare the current element with next one
        while (InputList[j] > nxt_element) and (j >= 0):
            InputList[j+1] = InputList[j]
            j=j-1
        InputList[j+1] = nxt_element

list = [19,2,31,45,30,11,121,27]
insertion_sort(list)
print(list)
```

    [2, 11, 19, 27, 30, 31, 45, 121]
    

##### Shell Sort
Shell Sort involves sorting elements which are away from ech other. We sort a large sublist of a given list and go on reducing the size of the list until all elements are sorted. The below program finds the gap by equating it to half of the length of the list size and then starts sorting all elements in it. Then we keep resetting the gap until the entire list is sorted.Shell Sort is just a variation of Insertion Sort. divide the number of elements /2 to get and sort using insertion sort


```python
# Shell Sort
def shellSort(input_list):
    
    gap = len(input_list) // 2
    while gap > 0:

        for i in range(gap, len(input_list)):
            temp = input_list[i]
            j = i
# Sort the sub list for this gap

            while j >= gap and input_list[j - gap] > temp:
                input_list[j] = input_list[j - gap]
                j = j-gap
            input_list[j] = temp

# Reduce the gap for the next element

        gap = gap//2

list = [19,2,31,45,30,11,121,27]

shellSort(list)
print(list)
```

    [2, 11, 19, 27, 30, 31, 45, 121]
    

##### Selection Sort
In selection sort we start by finding the minimum value in a given list and move it to a sorted list. Then we repeat the process for each of the remaining elements in the unsorted list. The next element entering the sorted list is compared with the existing elements and placed at its correct position. So at the end all the elements from the unsorted list are sorted.Given a list, take the current element and exchange it with the smallest element on the right hand side of the current element.


```python
def selection_sort(input_list):

    for idx in range(len(input_list)):

        min_idx = idx
        for j in range( idx +1, len(input_list)):
            if input_list[min_idx] > input_list[j]:
                min_idx = j
# Swap the minimum value with the compared value

        input_list[idx], input_list[min_idx] = input_list[min_idx], input_list[idx]


l = [19,2,31,45,30,11,121,27]
selection_sort(l)
print(l)
```

    [2, 11, 19, 27, 30, 31, 45, 121]
    

#### Searching Algorithm
Searching is a very basic necessity when you store data in different data structures. The simplest appraoch is to go across every element in the data structure and match it with the value you are searching for. This is known as Linear search. It is inefficient and rarely used, but creating a program for it gives an idea about how we can implement some advanced search algorithms.

##### Linear Search
In this type of search, a sequential search is made over all items one by one. Every item is checked and if a match is found then that particular item is returned, otherwise the search continues till the end of the data structure.If key element present return index if element else return -1


```python
# Linear Search
def linear_search(values, search_for):
    search_at = 0
    search_res = False

# Match the value with each data element
    while search_at < len(values) and search_res is False:
        if values[search_at] == search_for:
            search_res = True
        else:
            search_at = search_at + 1

    return search_res

l = [64, 34, 25, 12, 22, 11, 90]
print(linear_search(l, 12))
print(linear_search(l, 91))
```

    True
    False
    

##### Interpolation Search
This search algorithm works on the probing position of the required value. For this algorithm to work properly, the data collection should be in a sorted form and equally distributed. Initially, the probe position is the position of the middle most item of the collection.If a match occurs, then the index of the item is returned. If the middle item is greater than the item, then the probe position is again calculated in the sub-array to the right of the middle item. Otherwise, the item is searched in the subarray to the left of the middle item. This process continues on the sub-array as well until the size of subarray reduces to zero.There is a specific formula to calculate the middle position.


```python
# Interpolation Search
def intpolsearch(values,x ):
    idx0 = 0
    idxn = (len(values) - 1)

    while idx0 <= idxn and x >= values[idx0] and x <= values[idxn]:

# Find the mid point
        mid = idx0 +\
               int(((float(idxn - idx0)/( values[idxn] - values[idx0]))
                    * ( x - values[idx0])))

# Compare the value at mid point with search value 
        if values[mid] == x:
            return "Found "+str(x)+" at index "+str(mid)

        if values[mid] < x:
            idx0 = mid + 1
    return "Searched element not in the list"


l = [2, 6, 11, 19, 27, 31, 45, 121]
print(intpolsearch(l, 2))
```

    Found 2 at index 0
    

#### Graph Algorithm
There are two common established methods to do graph traversal
i. Depth First Traversal :
ii. Breadth First Traversal


##### Depth First Traversal :
Also called depth first search (DFS),this algorithm traverses a graph in a depth ward motion and uses a stack to remember to get the next vertex to start a search, when a dead end occurs in any iteration. We implement DFS for a graph in python using the set data types as they provide the required functionalities to keep track of visited and unvisited nodes.


```python
# Depth First Traversal :

class graph:

    def __init__(self,gdict=None):
        if gdict is None:
            gdict = {}
        self.gdict = gdict
# Check for the visisted and unvisited nodes
def dfs(graph, start, visited = None):
    if visited is None:
        visited = set()
    visited.add(start)
    print(start)
    for next in graph[start] - visited:
        dfs(graph, next, visited)
    return visited

gdict = { "a" : set(["b","c"]),
                "b" : set(["a", "d"]),
                "c" : set(["a", "d"]),
                "d" : set(["e"]),
                "e" : set(["a"])
                }


dfs(gdict, 'a')
```

    a
    b
    d
    e
    c
    




    {'a', 'b', 'c', 'd', 'e'}



##### Breadth First Traversal
Also called breadth first search (BFS),this algorithm traverses a graph breadth ward motion and uses a queue to remember to get the next vertex to start a search, when a dead end occurs in any iteration. Please visit this link in our website to understand the details of BFS steps for a graph.

We implement BFS for a graph in python using queue data structure. When we keep visiting the adjacent unvisited nodes and keep adding it to the queue. Then we start dequeue only the node which is left with no unvisited nodes. We stop the program when there is no next adjacent node to be visited.


```python
import collections
class graph:
    def __init__(self,gdict=None):
        if gdict is None:
            gdict = {}
        self.gdict = gdict

def bfs(graph, startnode):
# Track the visited and unvisited nodes using queue
        seen, queue = set([startnode]), collections.deque([startnode])
        while queue:
            vertex = queue.popleft()
            marked(vertex)
            for node in graph[vertex]:
                if node not in seen:
                    seen.add(node)
                    queue.append(node)

def marked(n):
    print(n)

# The graph dictionary
gdict = { "a" : set(["b","c"]),
                "b" : set(["a", "d"]),
                "c" : set(["a", "d"]),
                "d" : set(["e"]),
                "e" : set(["a"])
                }

bfs(gdict, "a")
```

    a
    b
    c
    d
    e
    



