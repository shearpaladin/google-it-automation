## Practice Quiz: Lists

__Grade received: 80%__

<br>

## Question 1

Fill in the blank using any of the methods you’ve learned thus far, like a for loop or a list comprehension. With the given list of "filenames", this code should rename all files with the extension .hpp to the extension .h. The function should then generate a new list called "newfilenames" that contains the file names with the new extension. 

```python
filenames = ["program.c", "stdio.hpp", "sample.hpp", "a.out", "math.hpp", "hpp.out"]
# Generate newfilenames as a list containing the new filenames
# using as many lines of code as your chosen method requires.
newfilenames = []
for f in filenames:
    if f.endswith("hpp"):
        newfilenames.append(f.replace(".hpp", ".h"))
    else:
        newfilenames.append(f)



print(newfilenames) 
# Should be ["program.c", "stdio.h", "sample.h", "a.out", "math.h", "hpp.out"]
```

> Great work! You're starting to see the benefits of knowing
how to operate with lists and strings.

<br>

## Question 2

Create a function that turns text into pig latin. Pig latin is a simple text transformation that modifies each word by: 

moving the first character to the end of each word;

then appending the letters "ay" to the end of each word. 

For example, python ends up as ythonpay.

```python
def pig_latin(text):
  say = []
  # Separate the text into words
  words = text.split()
  for word in words:
    # Create the pig latin word and add it to the list
    new = word[1:]+word[0]+"ay"
    # Turn the list back into a phrase
    say.append(new)
  result = ' '.join(say)
  return result
    
print(pig_latin("hello how are you")) # Should be "ellohay owhay reaay ouyay"
print(pig_latin("programming in python is fun")) # Should be "rogrammingpay niay ythonpay siay unfay"
```

> Nice! You're using some of the best string and list
functions to make this work. Great job!

<br>

## Question 3

Which list method can be used to add a new element to a list at a specified index position? 

* list.pop(index)
* **list.insert(index, x)**
* list.add(index, x)
* list.append(x)

> Correct! The list.insert(index, x) method will insert the given “x” element into the list at the specified index position.

<br>

## Question 4

Tuples and lists are very similar types of sequences. What is the main thing that makes a tuple different from a list?

* A tuple is mutable
* A tuple contains only numeric characters
* **A tuple is immutable**
* A tuple can contain only one type of data at a time

> Awesome! Unlike lists, tuples are immutable, meaning they can't be changed.

<br>

## Question 5

Fill in the blanks to complete the “guest_list” function. The guest_list function reads in a list of tuples with the name, age, and profession of each party guest, and prints the sentence "Guest is _ years old and works as __." for each guest. For example, guest_list(('Ken', 30, "a Chef") should print: “Ken is 30 years old and works as a Chef.” 

```python
def guest_list(guests):
	for person in guests:
		name, age, profession = person
		print('{} is {} years old and works as a {}'.format(name, age, profession))


guest_list([('Ken', 30, "Chef"), ("Pat", 35, 'Lawyer'), ('Amanda', 25, "Engineer")])


# Click Run to submit code

# Output should match:
# Ken is 30 years old and works as a Chef
# Pat is 35 years old and works as a Lawyer
# Amanda is 25 years old and works as an Engineer

```

> * This code is correct. For some reason it doesn't pass the test case on Cousera.