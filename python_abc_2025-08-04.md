## basic abc


### help

vrei sa vezi ce metode sunt disponibile pe x?
interpreter
aka python3 in terminal
apoi, daca x e string
`dir("ceva")`

daca x e lista
`dir([])`

in principiu pe ele cu dunders le ignori momentan


### printing

* The end='' parameter in the print statement prevents adding spaces between numbers

print(value, end='')


## loops

### range

```python
def brr(i):
    for z in range(2):
        print("!" * i)

if __name__ == "__main__":
    brr(3)
# !!!
# !!!
```






## exercitii


### chessboard

The chessboard function works by using the mathematical property that in a chessboard pattern, the value at position (i,j) can be determined by 1 - (i + j) % 2. This creates the alternating pattern where:

When the sum of row and column indices is even, we get 0
When the sum is odd, we get 1

* This creates a checkerboard pattern starting with 1 in top-left corner

For chessboard(3), this will print:
101
010
101

* sa inceapa cu 0 in loc de 1 stanga sus:
  `value = (i+j) % 2`
* 1 stanga sus:
  `value = (i+j) % 2`


* The end='' parameter in the print statement prevents adding spaces between numbers


```python
def chessboard(n):
    for i in range(n):
        for j in range(n):
            value = 1 - (i+j) % 2
            print(value, end="")
        print()

if __name__ == "__main__":
    chessboard(3)
# 101
# 010
# 101
```

alternative:
```python
def chessboard(size):
    i = 0
    while i < size:
        if i % 2 == 0:
            row = "10"*size
        else:
            row = "01"*size
        # Remove extra characters at the end of the row
        print(row[0:size])
        i += 1
```


### squared 

Please write a function named squared, which takes a string argument and an integer argument, and prints out a square of characters as specified by the examples below.

squared("ab", 3)
aba
bab
aba

```python
def squared(chars, n):
    for i in range(n):
        for j in range(n):
            char_index = (i+j) % len(chars)
            print(chars[char_index], end="")
        print()

if __name__ == "__main__":
    squared("ab", 3)
# aba
# bab
# aba
```

The pattern works because:
Position (0,0): (0+0) % 2 = 0 → 'a'
Position (0,1): (0+1) % 2 = 1 → 'b'
Position (0,2): (0+2) % 2 = 0 → 'a'
Position (1,0): (1+0) % 2 = 1 → 'b'


### line print

Please write a function named line, which takes two arguments: an integer and a string. The function prints out a line of text, the length of which is specified by the first argument. The character used to draw the line should be the first character in the second argument. __If the second argument is an empty string, the line should consist of stars__.

An example of expected behaviour:
line(7, "%")
line(10, "LOL")
line(3, "")
Sample output
%%%%%%%
LLLLLLLLLL
***


```python
def line(i, s):
    for x in range(i):
        if len(s) > 0:
            print(s[0], end="")
        else:
            print("*", end="")
```



### a box of hashes

Please write a function named box_of_hashes, which prints out a rectangle of hash characters. The function takes one argument, which specifies the height of the rectangle. The rectangle should be ten characters wide.  

The function should call the function line from the exercise above for the actual printing out. Copy your solution to that exercise above the code for this exercise. Please don't change anything in your line function.  

Some examples of how the function should work:  

box_of_hashes(5)
print()
box_of_hashes(2)
Sample output
##########
##########
##########
##########
##########  

##########
##########

```python
def line(i, s):
    for x in range(i):
        if len(s) <= 0:
            print("*", end="")
        else:
            print(s[0], end="")
    print()
    

def box_of_hashes(height):
    while height > 0:
        line(10, "#")
        height -= 1

if __name__ == "__main__":
    box_of_hashes(5)

```

varianta oficiala:
```python
def line(size, character):
    if character == "":
        character = "*"
    print(character[0] * size)
 
def box_of_hashes(height):
    i = 0
    while i < height:
        line(10, "#")
        i += 1
```

  
### a square of hashes
Please write a function named square_of_hashes, which draws a square of hash characters. The function takes one argument, which determines the length of the side of the square.  

The function should call the function line from the exercise above for the actual printing out. Copy your solution to that exercise above the code for this exercise. Please don't change anything in the line function.  

Some examples:
square_of_hashes(5)
print()
square_of_hashes(3)
Sample output
#####
#####
#####
#####
#####

###
###
###



solutie oficiala
```python
def line(size, character):
    if character == "":
        character = "*"
    print(character[0] * size)
 
def square_of_hashes(size):
    i = 0
    while i < size:
        line(size, "#")
        i += 1
```

solutia mea
```python
def line(i, s):
    for x in range(i):
        if len(s) <= 0:
            print("*", end="")
        else:
            print(s[0], end="")
    print()

def square_of_hashes(size):
    for x in range(size):
        line(size, "#")

if __name__ == "__main__":
    square_of_hashes(5)
```


```python
```


```python
```


```python
```


```python
```










## vscode

### python interpreter and built-in debugging tool




#line 

Please write a function named line, which takes two arguments: an integer and a string. The function prints out a line of text, the length of which is specified by the first argument. The character used to draw the line should be the first character in the second argument. If the second argument is an empty string, the line should consist of stars.

An example of expected behaviour:

line(7, "%")
line(10, "LOL")
line(3, "")
Sample output
%%%%%%%
LLLLLLLLLL
***

