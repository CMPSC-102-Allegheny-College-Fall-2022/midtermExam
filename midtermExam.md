# Midterm Examination for Computer Science 102 Fall 2022

## Name
Add Your Name Here

## Dates

Handed out: 26 October 2022

Due: 27 October 2022, 11:59pm

Please note the following.

* In this midterm, you are not allowed to discuss your work with others. 

* Each problem has a piece of code that you are to address. It is recommended that you use Jupyter to work on the code and then copy your modified code back into this test document for submission. Please be sure that your code runs correctly without crashing. 

* There are several questions following each coded exercises. Please replace the "to-do's" with your responses. 

* The exam is due at the deadline. Missing exams will receive a zero. 

* Best of luck.

## Questions for the Midterm Examination

---

# 1. Binet's Formula

The Fibonacci sequence is shown below for the first 10 numbers of the sequence. 
Sequence: `0, 1, 1, 2, 3, 5, 8, 13, 21, 34.`

We note that the Fibonacci sequence may be grown by adding the two previous numbers (after starting initially at $F_0 = 0$ and $F_1 = 1$) to obtain the next sequence value. The rule for growing the Fibonacci sequence is the following: 

$F_n = F_{n-1} + F_{n-2}$ for $F_0 = 0$ and $F_1 = 1$. 


For example, below is a worked out example for the first calculated sequence value ($F_3$).
```
F_0 = 0
F_1 = 1
F_3 = F_0 + F_1 = 0 + 1 = 1
```


Interestingly, there is another way to calculate the Fibonacci sequence for an arbitrarily chosen position of the sequence. If we let ($n$) be a position in the sequence of a value, then we can use Binet's Formula to determine the value at that position using Binet's formula, shown below.

For $n \in \mathbb(Z)$ (i.e., a sequence position),  

$F_n = \frac{ ( \frac{(1 + \sqrt(5) )}{2} )^{n}-( \frac{(1 - \sqrt(5) )}{2} )^{n}}{\sqrt{5}}$

## Task to Complete

Finish the below code to apply Binet's formula to calulate Fibonacci values according to sequence position in the sequence. It is suggested that you use Jupyter to complete your code and then to copy and paste the code back into the below fenced-in code area.

### Code to Fix

``` python
import math
def calcFib(n:int) -> None:
    """ a function that takes an integer to be applied to Binet's formula to determine the Finobacci Sequence value at the loction."""
    # TODO: Add Binet's Formula to complete calculation.
    # Note it may be more convenient to chop
    # up Binet's formula into smaller groups
    # to calculate and then take the sum of
    # the groups.
    print(f" fib sequence at position {n} is :{int(seqValue)}")
# end of calcFib()

for i in range(10):
    calcFib(i)
```

### Output

Your output should look like the following. 

```
Fib sequence at position 0 is :0
Fib sequence at position 1 is :1
Fib sequence at position 2 is :1
Fib sequence at position 3 is :2
Fib sequence at position 4 is :3
Fib sequence at position 5 is :5
Fib sequence at position 6 is :8
Fib sequence at position 7 is :13
Fib sequence at position 8 is :21
Fib sequence at position 9 is :34
```

#### Q1

Discuss the efficiency in using Binet's Formula to calculate the Fibonacci sequence, as opposed to, simply calculating the sequence by adding the two previous values as defined by $F_n = F_{n-1} + F_{n-2}$. 

```

TODO

```

#### Q2

We have spent time in class to cover Monoids and their properties. In the code above, and certainly in the code that you provided, there are demonstrations of the properties of monoids. Describe the property and argue how your piece of the code for this question demonstrates this property.

```

TODO

```

---

# 2. Lucas Numbers

Lucas numbers are defined in a similar way to Fibonacci sequence values, however, there is a difference in the initial values.

Lucas numbers are defined as $F_n = F_{n-2} + F_{n-1}$, for initial values $F_{n-2} = 2$ and $F_{n-1} = 1$. Each subsequent Lucas value is found by the sum of the previous two values.


### Code to Fix

Complete the code below to fix the Lucas number generator. Your code is to produce the first twelve Lucas numbers for the initial two values: $F_{n-2} = 2$ and $F_{n-1} = 1$. Your code is to use a `while` repetition statement to stop the iterative code.

``` python
import math

def lucas(a:int, b:int, n:int) -> None:
    """ calculates lucas number progression from a and b, 
    the initial starting points of sequence, and n the 
    number of positions to which to grow the sequence. """
    count = 0
    currSeqVal = 1
    print(f"\t Lucas: {a}")
    print(f"\t Lucas: {b}")
    while #TODO complete the condition to terminate loop
        #TODO implement system of equations to calculate Lucas numbers. 

        print(f"\t Lucas: {currSeqVal}")
# end of lucas

lucas(2,1,10) # first two sequence values and # of iterations
```

### Output

Your output should look like the following. 

```
Lucas: 2
Lucas: 1
Lucas: 3
Lucas: 4
Lucas: 7
Lucas: 11
Lucas: 18
Lucas: 29
Lucas: 47
Lucas: 76
Lucas: 123
Lucas: 199
```

#### Q3

What role do `a` and `b` serve in the initiation of the function `lucas()`?

```

TODO

```

#### Q4
Explain how the `while` function is able to stop the iterations at a set point after the code has been executed. Describe the specific pointat which the iteration halts?

```

TODO

```

#### Q5
Explain how a `for` loop could be used to replace the `while` loop iteration. In your response, describe what the condition of the `for` block would be. 

```

TODO

```

#### Q6 
What change (if any) would be required to change the `while` code block to a `for` code block in the above code to find Lucas numbers?

```

TODO

```

---
# 3. The Golden Ratio

The Golden Ratio (known mathematically as $\phi$) is an irrational number which has been found in many calculations involving data from nature. 

The value of $\phi$ can be calculated by the equation $\frac{1 + \sqrt(5)}{2}$ = 1.618033988749895, however it can also be calculated by using Lucas numbers as well. For two adjacent Lucas values, $\phi = \frac{F_{n-2}}{F_{n-1}}$. For example, below is a worked out example for finding $\phi$ from $F_{11} = 123$ and $F_{12} = 199$

$\phi = F_{12} / F_{11} = 199/123 = 1.6178861788617886$ 

Note: as the adjacent Lucas values get larger, the precision of $\phi$ increases.

## Task to Complete

Going back to your code from above where you completed the Lucas generator, please __copy the code below__ and then modify this new copy to now calculate the Golden Ratio ($\phi$) using the sequence of numbers. 

## Output

Your output should look like the following. 
```
Lucas: 2
Lucas: 1,	 GR: 0.5
Lucas: 3,	 GR: 3.0
Lucas: 4,	 GR: 1.3333333333333333
Lucas: 7,	 GR: 1.75
Lucas: 11,	 GR: 1.5714285714285714
Lucas: 18,	 GR: 1.6363636363636365
Lucas: 29,	 GR: 1.6111111111111112
Lucas: 47,	 GR: 1.6206896551724137
Lucas: 76,	 GR: 1.6170212765957446
Lucas: 123,	 GR: 1.618421052631579
Lucas: 199,	 GR: 1.6178861788617886
```

## Add your code here

``` python

TODO

```

#### Q7

Describe the mechanism to calculate $\phi$ in your code. Please introduce each variable of your code and state why it is necessary the calculation method.

```

TODO

```

#### Q8

In the template code, the function is defined with the following parameters in the code `(a:int, b:int, n:int)`. Explain what this code does and why one might add this code to define a function in Python.

```

TODO

```

---
# 4. An Entropy Calculator

In a part of mathemematics called Information Theory, Shannon's Entropy is a measurement of the uncertainty for the occurrence of certain event. Probabilities pertaining to the event are used as inputs for the calculation of uncertainty. To calculate the value of Shannon's Entropy, called $H(X)$, we use the below equation for the $N$ probabilities.

$H(X) = - \sum_{i = 1}^{N} \log_2 p(x_i) * p(x_i)$

Where $p(x_i)$ is one of the $N$ probabilities.

### Code to Fix

Complete the below code to calculate the Shannon's entropy value from the inputted list of probabilies in `a_list`.

``` python
import math

def getEntropy(prob:list) -> None:
    """ Calculate the entropy from an inputted list."""
    entropy = 0 
    for i in prob:
        print(f"processing frequency : {i}")
        entropy = entropy - (i*math.log(i,2))
    print(f"\nEntropy: {entropy}")
# end of getEntropy()

a_list = [2/10, 3/10, 2/10, 1/10, 1/10, 1/10]
getEntropy(a_list)
```

## Output

Your output should look like the following. 

```
processing frequency : 0.2
processing frequency : 0.3
processing frequency : 0.2
processing frequency : 0.1
processing frequency : 0.1
processing frequency : 0.1

Entropy: 2.4464393446710155
```

### Code to Fix

``` python
import math

def getEntropy(prob:list) -> None:
    """ Calculate the entropy from an inputted list."""
    entropy = 0 
    for i in prob:
        print(f"processing frequency : {i}")
        # TODO Add formula work to calculate entropy.
        # Note: it might be more convenient
        # to break up the equation into smaller
        # parts to sum at the conclusion.
        # Note, find the log base 2 of 3 using the following: math.log(3,2)

    print(f"\nEntropy: {entropy}")
# end of getEntropy()

a_list = [2/10, 3/10, 2/10, 1/10, 1/10, 1/10]
getEntropy(a_list)
```

#### Q8

Above the `for` block, we define the variable `entropy`. This value is extensively used inside the `for` code block. Why is it necessary to define this value __before__ the code block and _not_ inside the `for` block?

```

TODO

```

#### Q9

In the header of the function, what does the `-> None` indicate?

```

TODO

```

---


## An Integer Tester

A real number value can be determine to be an integer (i.e., a counting number, and not a decimal value) in Python by using the below command.

```
myValue = 3.14
print(isinstance(myValue, int)) # prints False
myValue = 3
print(isinstance(myValue, int)) # prints True
```

A simple mathematical function for determining whether $x$ is an integer is described below. 

 $f(x) = abs[cos(\pi * x)] = 1.0$, for $ x \in \mathbb{R}$

Here, we note that $f(x) == 1.0$ when $x$ is an integer, otherwise, $f(x) != 1.0$ for a floating point values.

The general results this function when tested with different values is shown in the table below.

Value | Test | Conclusion 
---- | ------- | -------
 0.4|$abs[cos(\pi * 0.4)] != 1.0$  |  0.4 is not an integer
 4 |$abs[cos(\pi * 4)] == 1.0$    |  4 is an integer
 0.99 |$abs[cos(\pi * 0.99)] != 1.0$  |  0.99 is not an integer
 99 |$abs[cos(\pi * 99)] == 1.0$    |  99 is an integer


## Task to Complete

Complete the below code to finish the integer checker. Note, the absolute value function, `getAbsoluteValue()` must also be fixed for the whole program to run correctly. You cannot use Python's built-in `abs()` command for this task.

### Code to Fix

``` python
import math
def isInt(x):
    if getAbsoluteValue # TODO determine the test for integers:
        print(f"{x} is an integer")
    else:
        print(f"{x} is NOT an integer")
# end of isInt()
    
def getAbsoluteValue(x):
    # TODO determine the polarity of the value
    # TODO return opposite polarity.
# end of getAbsoluteValue()

myVal = -3.414
print(f" Value: {myVal}; absolute value: {getAbsoluteValue(myVal)}")
isInt(myVal)

myVal = 3
print(f" Value: {myVal}; absolute value: {getAbsoluteValue(myVal)}")
isInt(myVal)
```

## Output

Your output should look like the following. 

```
 Value: -3.414; absolute value: 3.414
-3.414 is NOT an integer
 Value: 3; absolute value: 3
3 is an integer
```

#### Q10
Explain why the absolute value is required in the Function `isInt()`. For instance, would the code work to determine integers from floats without finding the absolute value?

```

TODO

```

#### Q11
Would it make sense to use a `list` to import the test value into `isInt()`? Why or why not?

```

TODO

```
