## Practice Quiz: Recursion

__Grade received: 100%__

<br>

## Question 1

What is recursion used for?

* Recursion is used to create loops in languages where other loops are not available.
* We use recursion only to implement mathematical formulas in code.
* Recursion is used to iterate through sequences of files and directories.
* **Recursion lets us tackle complex problems by reducing the problem to a simpler one.**

> You nailed it! By reducing the problem to a smaller one each time a recursive function is called, we can tackle complex problems in simple steps.

<br>

## Question 2

Which of these activities are good use cases for recursive programs? Check all that apply.

```python
def factorial(n):
    result = 1
    for x in range(1,n+1):
        result = result * x
    return result

for n in range(0,9):
    print(n, factorial(n))
```

> Great work! The pieces of code you're tackling keep getting
more complex, you're doing a great job!

<br>

## Question 3

Write a script that prints the first 10 cube numbers (x**3), starting with x=1 and ending with x=10.


```python
for x in range(1,11):
  print(x**3)
```

> You nailed it! You got the code to print the first 10 cubes.

<br>

## Question 4

Write a script that prints the multiples of 7 between 0 and 100. Print one multiple per line and avoid printing any numbers that aren't multiples of 7. Remember that 0 is also a multiple of 7.

```python
for x in range(0, 100):
    if (x % 7) == 0:
        print(x)
```

>Awesome! You're getting Python to do all the work for you.

<br>

## Question 5

The retry function tries to execute an operation that might fail, it retries the operation for a number of attempts.  Currently the code will keep executing the function even if it succeeds. Fill in the blank so the code stops trying after the operation succeeded.

```python
def retry(operation, attempts):
  for n in range(attempts):
    if operation():
      print("Attempt " + str(n) + " succeeded")
      break;
    else:
      print("Attempt " + str(n) + " failed")

retry(create_user, 3)
retry(stop_service, 5)
```

> Well done, you! You've fixed the code to stop executing once
the function is successful.