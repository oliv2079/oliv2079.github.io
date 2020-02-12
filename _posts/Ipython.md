# The python exercises

**Ex 0**: The Jupyter Notebooks are organized as a list of cells. There are two central kinds of cells, they are called **Code** and **Markdown**. The cell type can be set [using a keyboard shortcut](http://sowingseasons.com/blog/jupyter-keyboard-shortcuts.html), or using the menu above.

The **Code** cells simply contain the Python code, no big deal.

The **Markdown** cells contain text (explanations, sections, etc). The text is written in Markdown. Markdown allows you to write using an easy-to-read, easy-to-write plain text format, then convert it to structurally valid XHTML (or HTML). You can read about it here:

http://daringfireball.net/projects/markdown/

In the cell below, write a short text that demonstrates that you can
* Create a section
* Write words in bold and italics
* Create lists
* Establish a [hyperlink](https://en.wikipedia.org/wiki/Hyperlink)

*[Write the answer to **Ex 0** here]*

**Ex 1**: Create a list `a` that contains the numbers from $1$ to $1110$, incremented by one, using the `range` function.


```python

```

**Ex 2**: Show that you understand [slicing](http://stackoverflow.com/questions/509211/explain-pythons-slice-notation) in Python by extracting a list `b` with the numbers from $543$ to $779$ from the list created above.


```python

```

**Ex 3**: Using `def`, define a function that takes as input a number $x$ and outputs the number multiplied by itself plus three $f(x) = x(x+3)$. 


```python

```

**Ex 4**: Apply this function to every element of the list `b` using a `for` loop. 


```python

```

**Ex 5**: Do the same thing using a list comprehension.


```python

```

**Ex 6**: Write the output of your function to a text file with one number per line.


```python

```

**Ex 7**: Show that you know about strings using this example from https://learnpythonthehardway.org/python3/ex6.html (code reproduced below).

1. Go through the code below and write a code comment above each line explaining it.
1. Find all the places where a string is put inside a string. There are four places.
1. Are you sure there are only four places? How do you know? Maybe I like lying.
1. Explain why adding the two strings w and e with + makes a longer string.


[**Hint**: If you feel this is too complex, try completing the prior learningthehardway exercises first. Start [here](https://learnpythonthehardway.org/python3/). 


```python
# Note from Sune: In Python, code comments follow the "#" character

types_of_people = 10
x = f"There are {types_of_people} types of people."

binary = "binary"
do_not = "don't"
y = f"Those who know {binary} and those who {do_not}."

print(x)
print(y)

print(f"I said: {x}")
print(f"I also said: '{y}'")

hilarious = False
joke_evaluation = "Isn't that joke so funny?! {}"

print(joke_evaluation.format(hilarious))

w = "This is the left side of..."
e = "a string with a right side."

print(w + e)
```

    There are 10 types of people.
    Those who know binary and those who don't.
    I said: There are 10 types of people.
    I also said: 'Those who know binary and those who don't.'
    Isn't that joke so funny?! False
    This is the left side of...a string with a right side.
    

*[Write the answer to **Ex 7**, 2-4 here]*

**Ex 8**: First, learn about JSON by reading the **[wikipedia page](https://en.wikipedia.org/wiki/JSON)**. Then answer the following two questions in the cell below. 

* What is `json`? What do the letters stand for?
* Why is `json` superior to `xml`? (... or why not?)

*[Write your answer to **Ex 8** here]*

**Ex 9a**: Use the `json` module (instructions on usage here: https://docs.python.org/3/library/json.html). 

First use `urllib` (https://docs.python.org/3/library/urllib.html), or another Python library, to download **[this file](https://raw.githubusercontent.com/suneman/socialgraphs2019/master/files/test.json)**. 

The downloaded file is a string when you first download it, but you can use the `json` library to "load" the string and decode it to a Python object, using `json.loads()`. (The decoded string is a python object, a list with a single element, a dictionary (with nested dictionaries inside it)).


```python

```

**Ex 9b**: Now, let's take a look at the file you downloaded. First, just write the name of the variable that contains the decoded file content and hit enter to take a look at it. It's  the list of Twitter Trending topics, a few days ago.


```python

```

**Ex 9c**: The thing you've just decoded is now a list of length 1. What are the names of the keys organizing the dictionary at position 0 in the list? (Just write the code to produce the answer.) 

**Hint** use the `.keys()` method to easily get the keys of any dictionary.


```python

```

**Ex 9d**: Two small questions 
* What time did I create the list of Trending Topics?
* Print the names of the trending topics (bonus for using a list comprehension)

(Just write the code to produce the answer.)


```python

```
