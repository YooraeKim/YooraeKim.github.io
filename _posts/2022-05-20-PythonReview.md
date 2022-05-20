### Python Review - print(), input(), variable

#### print()


```python
print(1)
print([1,2,3])
print(123)
```

    1
    [1, 2, 3]
    123
    


```python
print('python')
```

    python
    


```python
print('My name is', 'Yoorae.')
# whenever you use comma(,) and list words inside of parenthesis, 
# print() function prints out the listed words with space(' ') in between them.
```

    My name is Yoorae.
    

#### input()

interactive shell prints out all the inputs, but actually it's not supposed to print out any values. It only stores the value we put in.


```python
input()
```

    aaaaa
    




    'aaaaa'




```python
input('Enter your name: ')
```

    Enter your name: Yoorae Kim
    




    'Yoorae Kim'




```python
age = input('How old are you? ')
```

    How old are you? 22
    


```python
age
```




    '22'



#### variable 변수


```python
my_int = 1
```

1 이라는 값을 my_int에 '할당'한다. (저장 X)

변수 : 변할 수 있는 할당되는 값.


```python
my_int + 3 # 1 + 3
```




    4




```python
my_int * 100 # 1 * 100
```




    100



#### Data Type

- Numeric

정수형 자료형 : 1, 2, 3, 4 . . . integer
    
실수형 자료형 : 3.14, 1.2, 4.6 . . . float


```python
my_float = 2.4
my_int = 3

type(my_float) #type : float
type(my_int) # type : integer
```




    int



- String

'Hello', "Hello"

(x) 'Hello" 


```python
print("hello world")
```

    hello world
    

- Boolean

True/False



```python
my_boolean = True

print(my_boolean)
```

    True
    

- List


```python
my_list = [1, 2, 3]

students = ['Claire', 'Casey', 'June', 'Matthew', 'Harry']

students
```




    ['Claire', 'Casey', 'June', 'Matthew', 'Harry']




```python
# using for loop 

for std in students:
    print(std)
```

    Claire
    Casey
    June
    Matthew
    Harry
    


```python
# using random

import random

print(random.choice(students)) 
#randomly prints out names in the list.
```

    Matthew
    


```python
# using .append

students.append('Sarah')
students
```




    ['Claire', 'Casey', 'June', 'Matthew', 'Harry', 'Sarah']



- Tuple

We cannot make a change in values inside of tuple.


```python
# for example, in this case, we can make a change in values inside of the list.
# we replace Claire with Esther.
students[0] = 'Esther'
students
```




    ['Esther', 'Casey', 'June', 'Matthew', 'Harry', 'Sarah']




```python
my_tuple = ('Jisoo', 'Mandy', 'Blaire')
my_tuple[0] = 'Jae'

# in this case, we get an error, because we cannot replace the value in tuple.
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-41-23063bfa98fa> in <module>
          1 my_tuple = ('Jisoo', 'Mandy', 'Blaire')
    ----> 2 my_tuple[0] = 'Jae'
    

    TypeError: 'tuple' object does not support item assignment


- Dictionary

dictionary is like a container. It holds multiple numbers of values.

{ key1 : val1, ... }


```python
my_dict = {'Che':'Male', 'Nuri':'Male', 'Shawn':'Male', 'Claire':'Female'}

# key : Che, Nuri, Shawn, Claire
# value : Male, Male, Male, Female
```


```python
my_dict['Shawn']
```




    'Male'




```python
# change the value of a certain key.
my_dict['Claire'] = 'Male'
my_dict
```




    {'Che': 'Male', 'Nuri': 'Male', 'Shawn': 'Male', 'Claire': 'Male'}



#### Changing the Data Type


```python
my_int = 1
type(my_int)
```




    int




```python
# by using float() function, change the integer value to float form.
float(my_int)
```




    1.0




```python
my_int = 1
type(my_int)
```




    int




```python
# by using str() function, change the integer value to string form.
str(my_int)
```




    '1'




```python
my_str = 'denison'
my_str

list(my_str) 
# forcing each letters to become part of the components of the list.
# ['d', 'e', 'n', 'i', 's', 'o', 'n']
```




    ['d', 'e', 'n', 'i', 's', 'o', 'n']



#### String | 문자열


```python
my_str = "Denison in Ohio"

print(my_str)
```

    Denison in Ohio
    


```python
my_str = 'Denison in Ohio'

print(my_str)
```

    Denison in Ohio
    

"""string""" and '''string'''


```python
my_str = """hello world
This is Yoorae
Majoring in DA
"""

my_str

# \n = enter key on a keyboard.
```




    'hello world\nThis is Yoorae\nMajoring in DA\n'



#### formatting

using '%'


```python
my_str = 'My name is %s' % 'Harry Kim'
my_str

#'Harry Kim' replaces %s
```




    'My name is Harry Kim'




```python
'%d %d' % (1, 2)
# we use %d when we use the integer.
```




    '1 2'




```python
'%f' % 3.14
# we use %f when we want to use the float.
```




    '3.140000'




```python
'My name is %s' % 'Yoorae Kim'
# putting the string in the spot where %s is placed at. 
```




    'My name is Yoorae Kim'




```python
# using '{}'.format() method.
'My name is {}'.format('Yoorae Kim') 

# this method allows us to put any format of the value inside of the {}.
```




    'My name is Yoorae Kim'




```python
'{} x {} = {}'.format(2, 3, 2*3)
```




    '2 x 3 = 6'




```python
'{1} x {0} = {2}'.format(2, 3, 2*3)

# in this case, it is 3 x 2, because inside of the format(), 
# index 0 : 2
# index 1 : 3
# index 2 : 2*3
# therefore, {index 1} x {index 0} = {index 2}
```




    '3 x 2 = 6'




```python
my_name = "Yoorae Kim"
# if I want to print out 'r' from my name,
# I see that the r is in index 3. 

my_name[3]
```




    'r'




```python
# if I cannot count the number of indices in this string...
# but wishing to print out the very last index character...

my_name[-1]
```




    'm'



#### Slicing | 문자열 슬라이싱

Here, we take out chunk/part of the string, not only the single character.


```python
string = 'python'
string[1:4]
```




    'yth'




```python
string2 = 'I love bubble gum'
print ( string2[:6] ) # from the beginning, all the way to e(6th).
print ( string2[7:] ) # from b(7th), all the way to the end.
```

    I love
    bubble gum
    

#### string.split() | string method

This is one of the functions.

This only applies to string type.


```python
string = 'Yoorae from Korea'
string.split()
```




    ['Yoorae', 'from', 'Korea']




```python
fruit_str = 'Grapes Strawberry Cherry Pear Peach Watermelon Mango'

fruits = fruit_str.split()
fruits
```




    ['Grapes', 'Strawberry', 'Cherry', 'Pear', 'Peach', 'Watermelon', 'Mango']



#### Docstring


```python
# this is my note
""" this is my note """ # this is the docstring
```




    ' this is my note '



#### end, escape code

print (  '   ',  end  =  '   ')

Here, we designate the end part of the print() function.

##### End


```python
# End
print('hello world', end = ' / hello python!')
```

    hello world / hello python!

##### Escape Code

\n = equivalent to 'enter key'

\t = equivalent to 'tab key'


```python
print('let us learn how to code')

print('-' * 15)

print('let us learn\nhow to code')
```

    let us learn how to code
    ---------------
    let us learn
    how to code
    


```python
print('let us learn\thow to code')

print('-' * 15)

print('let us learn\thow to \ncode')
```

    let us learn	how to code
    ---------------
    let us learn	how to 
    code
    


```python
print('hello', end = '\t'); print('world')

print('-' * 15)

print('hello', end = '\n'); print('python')
```

    hello	world
    ---------------
    hello
    python
    

#### List

immutable : unable to be changed.

mutable : liable to change.

[ val1, val2, ... ]


```python
my_list = []
print(my_list)
print(type(my_list)) # the type is 'list'
```

    []
    <class 'list'>
    


```python
my_li = [1,2,3]
print(my_li)

my_lst = ['hello', 'python', 'world']
print(my_lst)
```

    [1, 2, 3]
    ['hello', 'python', 'world']
    


```python
# Adding values to the list. Use append().

my_lst.append('candy')

print(my_lst)
```

    ['hello', 'python', 'world', 'candy']
    

#### Index / Element


```python
animals = ['Koala', 'Giraffe', 'Tiger', 'Dog', 'Cat']
```


```python
animals[3] # we take out the value in 3rd index
```




    'Dog'




```python
del animals[3] # get rid of 3rd index value
print(animals)
```

    ['Koala', 'Giraffe', 'Tiger', 'Cat']
    


```python
animals[1:3]

# index [1] and index [2] , no index [3]
```




    ['Giraffe', 'Tiger']



#### list.sort()


```python
animals = ['Koala', 'Giraffe', 'Tiger', 'Dog', 'Cat', 'Squirrel', 'Cat']
```


```python
animals.sort()
print(animals)
```

    ['Cat', 'Cat', 'Dog', 'Giraffe', 'Koala', 'Squirrel', 'Tiger']
    

#### list.count()


```python
animals.count('Cat') # there are 2 cats in this animals list
```




    2



#### len()

This is a python built-in function.


```python
len(animals) # length of the list.
```




    7



#### Tuple 

is immutable.

(val1, val2, ...)

val1, val2, ...


```python
my_tuple = ()
print(my_tuple)
print(type(my_tuple))
```

    ()
    <class 'tuple'>
    


```python
my_tuple = (1,2,3)
print(my_tuple)
```

    (1, 2, 3)
    


```python
my_tuple = 1,2,3
print(my_tuple)
```

    (1, 2, 3)
    

#### Packing and Unpacking


```python
my_tuple = 1, 2, 3

num1, num2, num3 = my_tuple
```


```python
print(num1)

print(num2)

print(num3)
```

    1
    2
    3
    

Here, we can observe that num1 is 1, and num2 is 2.

How can we switch the values as it shows num1 is 2, and num2 is 1?



```python
num1, num2 = num2, num1

print(num1)

print(num2)
```

    2
    1
    

#### for 

`for` variable `in` container:

         order 1
         
         order 2
         
           ...


```python
for animal in animals:
    print(animal)
```

    Cat
    Cat
    Dog
    Giraffe
    Koala
    Squirrel
    Tiger
    


```python
for i in [1,2,3]:
    print(i)
```

    1
    2
    3
    


```python
for my_str in 'hello world':
    print(my_str)
```

    h
    e
    l
    l
    o
     
    w
    o
    r
    l
    d
    

#### range()


```python
print(range(3))

print(type(range(3)))
```

    range(0, 3)
    <class 'range'>
    


```python
for n in range(0,3):
    print(n)
```

    0
    1
    2
    


```python
for n in range(6):
    print(n)
```

    0
    1
    2
    3
    4
    5
    

#### for x2 | 중첩반복문


```python
#let's try the multiplication table.

for i in range(1,10):
    print('{} x {} = {}'.format(2, i, 2*i))
    
    
    # 2 x 1 = 2
    # 2 x 2 = 4
    # 2 x 3 = 6
    # ...
```

    2 x 1 = 2
    2 x 2 = 4
    2 x 3 = 6
    2 x 4 = 8
    2 x 5 = 10
    2 x 6 = 12
    2 x 7 = 14
    2 x 8 = 16
    2 x 9 = 18
    


```python
for j in range(2,10):
    for i in range(1,10):
        print('{} x {} = {}'.format(j, i, j*i))
```

    2 x 1 = 2
    2 x 2 = 4
    2 x 3 = 6
    2 x 4 = 8
    2 x 5 = 10
    2 x 6 = 12
    2 x 7 = 14
    2 x 8 = 16
    2 x 9 = 18
    3 x 1 = 3
    3 x 2 = 6
    3 x 3 = 9
    3 x 4 = 12
    3 x 5 = 15
    3 x 6 = 18
    3 x 7 = 21
    3 x 8 = 24
    3 x 9 = 27
    4 x 1 = 4
    4 x 2 = 8
    4 x 3 = 12
    4 x 4 = 16
    4 x 5 = 20
    4 x 6 = 24
    4 x 7 = 28
    4 x 8 = 32
    4 x 9 = 36
    5 x 1 = 5
    5 x 2 = 10
    5 x 3 = 15
    5 x 4 = 20
    5 x 5 = 25
    5 x 6 = 30
    5 x 7 = 35
    5 x 8 = 40
    5 x 9 = 45
    6 x 1 = 6
    6 x 2 = 12
    6 x 3 = 18
    6 x 4 = 24
    6 x 5 = 30
    6 x 6 = 36
    6 x 7 = 42
    6 x 8 = 48
    6 x 9 = 54
    7 x 1 = 7
    7 x 2 = 14
    7 x 3 = 21
    7 x 4 = 28
    7 x 5 = 35
    7 x 6 = 42
    7 x 7 = 49
    7 x 8 = 56
    7 x 9 = 63
    8 x 1 = 8
    8 x 2 = 16
    8 x 3 = 24
    8 x 4 = 32
    8 x 5 = 40
    8 x 6 = 48
    8 x 7 = 56
    8 x 8 = 64
    8 x 9 = 72
    9 x 1 = 9
    9 x 2 = 18
    9 x 3 = 27
    9 x 4 = 36
    9 x 5 = 45
    9 x 6 = 54
    9 x 7 = 63
    9 x 8 = 72
    9 x 9 = 81
    

#### Comprehension


```python
numbers = [1,2,3,4,5,6,7,8,9,10]
odd_numbers = []

for number in numbers:
    if number % 2 == 1:
        odd_numbers.append(number)
        
        
print(odd_numbers)
```

    [1, 3, 5, 7, 9]
    


```python
odd_numbers = [number for number in numbers if number % 2 == 1]

print(odd_numbers)
```

    [1, 3, 5, 7, 9]
    

#### Operator

##### Assign

`=` `+=` `-=` `*=` `/=`


```python
count = 1
```


```python
count = count + 1
print(count)
```

    2
    


```python
# 'count = count + 1' => is same as 'count += 1'
count += 1
print(count)
```

    3
    

##### Arithmetic

 `+` `-` `*` `/`


```python
3 + 3
```




    6




```python
 12 / 3
```




    4.0



`**` `//` `%`


```python
3 ** 2 # same as 3^2
```




    9




```python
print( 7 / 3 )

print( 7 // 3 ) # division result. 

print( 7 % 3 ) # leftovers.
```

    2.3333333333333335
    2
    1
    


```python
numbers = [1,2,3,4,5,6,7]

for number in numbers:
    if number % 2 == 1:
        print(number)
```

    1
    3
    5
    7
    

#### String operator

`+` `*`


```python
print('hello' + ' Python')

print('Welcome' + ' ' + 'to' + ' ' + 'Python')

#connects two strings.
```

    hello python
    Welcome to python
    


```python
print('hello\n' * 3)
```

    hello
    hello
    hello
    
    


```python
def cls():
    print('\n' * 3)
    
cls()
```

    
    
    
    
    

#### Comparison operator

`==` : A == B , A equal to B (T/F)

`!=` : A != B , A is not equal to B (T/F)

`>` : A > B , A is greater than B

`<` : A < B , A is less than B

`>=` : A >= B , A is greater than or equal to B

`<=` : A <= B , A is less than or equal to B


```python
print (1 < 2)
print (3 <= 1)
print (3 == 4)
```

    True
    False
    False
    

#### Logical operator

`and` : both A and B should be True.

`or` : if one of A or B is not True, it is False.

`not` : chooses the opposite.


```python
print (True and True)
print (True and False)

print (False and False)
```

    True
    False
    False
    


```python
print (True or True)

print (True or False)

print (False or False)
```

    True
    True
    False
    


```python
print (not False)

print (not True)
```

    True
    False
    


```python
height = 120
age = 8

height > 140 and age > 10  # False and False.
```




    False




```python
height = 190
age = 9

height > 140 and age > 10  # True and False
```




    False




```python
height = 150
age = 32

height > 140 and age > 10 # True and True
```




    True



#### Membership operator

`in` 

`not in`


```python
names = ['Emily', 'Matthew', 'June', 'Mandy', 'Claire', 'Casey', 'Jisoo']

print('Claire' in names) # True. Claire is in names list.

print('Mai' in names) # False. Mai is not in names list.

print('Mai' not in names) # True. Mai is not in names list.
```

    True
    False
    True
    

#### if , else, elif

`if` condition ( True or False):

    order 1
    
    order 2 
    
`else` (if ' if ' is false, run ' else ' ):

    order 1
    
    order 2
    
`elif` another condition (True or False) :

    order 1
    
    order 2
    
    ...


```python
name = 'Claire'

if name == 'Claire':
    print('Hello. Nice to meet you, '+ name +'.' )
    
elif name == 'Judy':
    print('Hello, your name is Judy.')

elif name == 'Mandy':
    print('Hello, your name is Mandy.')
    
else:
    print('Hello, I do not know your name.')
```

    Hello. Nice to meet you, Claire.
    

#### Loop - While

`while` condition:
    
    order 1
    
    order 2
    
    ...


```python
count = 0

while count < 4:
    print('count : ', count)
    count += 1
```

    count :  0
    count :  1
    count :  2
    count :  3
    

#### continue, break


```python
count = 0

while count < 10:
    count += 1
    if count < 4:
        continue
    print('count : ', count)
    if count == 8:
        break
```

    count :  4
    count :  5
    count :  6
    count :  7
    count :  8
    

### dictionary

{ key1 : val1 , ... }


```python
my_dict = {}

my_dict['std1'] = 'Emily'
my_dict['std2'] = 'Casey'
my_dict['std3'] = 23

print(my_dict)
```

    {'std1': 'Emily', 'std2': 'Casey', 'std3': 23}
    


```python
print(my_dict['std1'])
```

    Emily
    


```python
del my_dict['std3']

print(my_dict)
```

    {'std1': 'Emily', 'std2': 'Casey'}
    


```python
for val in my_dict.values():
    print(val)
```

    Emily
    Casey
    


```python
for key in my_dict.keys():
    print(key)
```

    std1
    std2
    


```python
for key,val in my_dict.items():
    print(key, val)
```

    std1 Emily
    std2 Casey
    

#### Function def

There are three types of functions :

Built-In function, functions in modules, and UDF; User-Defined function.

Here, we are going to look at UDF.

---
`def` function name ( factor1 , . . . ) :

   command 1 

   command 2

   `return` result 

---
    
def : short for define
    


```python
def add (num1, num2):
    return num1 + num2

add( 56 , 25 ) # calling the function here.
```




    81




```python
def add_mul(num1, num2):
    return num1 + num2, num1 * num2

print(add_mul(12 , 34))
# returns two results, but only gives out '1' result as a tuple.
# function did the 'packing' on multiple results.

my_add, my_mul = add_mul(12,34) # unpacking

print(my_add)
print(my_mul)
```

    (46, 408)
    46
    408
    

#### Module

`import`



```python
import random

# generates randomly.

#random.choice()

students = ['claire','casey','joy']

print(random.choice(students))
print(random.choice(students))
```

    casey
    joy
    


```python
#random.sample()

print(random.sample(students,2)) # we can designate the sample size.

```

    ['claire', 'casey']
    


```python
# Lotto number

print(random.sample(range(1,46), 6))
```

    [29, 14, 25, 7, 42, 24]
    


```python
# random.randint()

print(random.randint(8,10)) # pick integer in between 8 ~ 10
```

    9
    
