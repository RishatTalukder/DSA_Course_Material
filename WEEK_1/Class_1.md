# The Basics

The basic building blocks of programming are:

1. Variables
2. Data Types
3. Arrays
4. Conditional Statements
5. Loops
6. Functions

## Variables and Data Types
**Variables** are like a `box` that holds a `value` of certain `data type`.

We can write a variable in the following way:

```
variable_name = value
```

Here, `variable_name` is the name of the variable and `value` is the value that it holds.

For example:

```
name = "John Doe"
```

The above line will assign the value `"John Doe"` to the variable `name`.

Now, like I said earlier the variable hold a value of a `data type`. In this case the variable `name` holds a value of `string` data type.

Values can be mainly of the following types:

1. String
2. Integer
3. Float
4. Boolean

String values are a `set of characters` that are written inside `double quotes` or `single quotes`.

For example:

```
"Why did I came here?"
```

In the above line we see a set of characters that are written inside double quotes. This is called a `string`.

The integer values are `whole numbers`.

For example: 1, 2, 3, 42069

The float values are `decimal numbers`.

For example: 1.0, 2.0, 3.9, 42069.42069

each language has its own set of data types. But in the end they all mean the same thing; what kind of data a variable holds.

The boolean values are `true` or `false` or `0` or `1`.

## Arrays

Arrays (or lists in Python) are ordered collections of values.

In some languages all elements must have the same type.

For example:

```
array = [1, 2, 3, 4, 5]
```

Where ever you look you'll see an array in programming.

> Will discuss more about arrays later as it is a data structure and has a lot of applications.

## Conditional Statements

Conditional statements are a way to make a decision based on a `condition` that is `true` or `false`.

this is the flow control of a program and is generally used to make a program more logical.

The syntax is as follows:

```
if condition:
    statement
else:
    statement
```

The `condition` can be anything that is `true` or `false`. Mainly it is a `boolean value`. The `statement` is a block of code that is executed if the `condition` is `true`. If the `condition` is `false` then the `statement` is not executed.

Else part is optional and is executed if the `condition` is `false`.

## Loops

`Loops` are a way to repeat a block of code multiple times.

For example, Let's say you want to multiply a number by 2, 10 times.

You have to write the same code 10 times.

We don't want that. So, instead of writing the same code 10 times, we can use a loop.

The syntax is as follows:

```
Loop from 1 to 10:
    print(5 * 2)
```

This will print the value 10 times.

There are mainly 2 types of loops:

1. For Loop
2. While Loop

For loop is used when you `know` the number of times you want to repeat the code.

While loop is used when you `don't know` the number of times you want to repeat the code but the code is repeated until a certain condition is `true`.

## Functions

Functions are a way to reuse a block of code.

Let's say you have a code that finds the number of even numbers in a list.

```
a = 10
b = 20
count = 0

loop from a to b -> i:
    if i % 2 == 0:
        count = count + 1

print(count)
```

> `->` means while the loop is running from `a` to `b`, the variable `i` holds the value of the current number being checked.

> i%2 == 0, is the condition that checks if the current number is even or not.
        
Now, this same code might be needed multiple times later on. So, instead of writing the same code multiple times, we can make this a function.

So, let's break it down.

In a sense, the main idea of the above code is to take two numbers as input and produce the number of even numbers between them.

So, What we can do is pack the above code where we can `pass` the two numbers as input and `return` the number of even numbers between them.

```
function count_even_numbers(a, b):
    count = 0

    loop from a to b -> i:
        if i % 2 == 0:
            count = count + 1

    return count
```
> `a` and `b` inside the bracket right after the function name are called `arguments`. These are the values that will be considered as input to the function.

this process is called `defining` a `function`. We can name the function whatever we want.

Now, what we can do is `call` the function by just writing the name of the function followed by the arguments.

```
count = count_even_numbers(10, 20)

print(count)
```

Here, inside the function, at the very last line we have a `return` statement. This is the value that will be `returned` by the function after all the calculations are done.

We can then use the returned value in any other part of the program.

Functions are specially useful because it makes the code more `modular` and `reusable`.

These are the tools and rules that we are bound to use in programming. Every programming language has these tools and rules. We will only use these tools to make our logic and solve a lot of problems.

Now, let's talk about `DSA`

## What is DSA?

> Data Structures and Algorithms are the building blocks of programming.

Data structure is the way to store, manage and organize data so that it can be easily accessed and manipulated.

A program heavily relies on data structures to perform its tasks quickly and efficiently.

Algorithms are the methods of manipulating data structures to solve a particular problem.

As DSA is the main topic of this course, we'll be talking about Data Structures and Algorithms in the coming weeks.

There a lot of data structures and each data structure has its own set of algorithms. 

Like, array has algorithms like searching, sorting, etc. Tree has algorithms like BFS, DFS etc.


# Some problems

Let's say you have 2 numbers `a` and `b` can you swap them?

Simple, we can take a third variable `c` and assign `a` to `c` and `b` to `a` and `c` to `b`.

```
a = 10
b = 20

c = a

a = b

b = c
```

But what if I tell you to find the maximum number between `a` and `b`?

We can compare `a` and `b` and assign the maximum number to a new variable.

```
a = 10
b = 20

if a > b:
    max = a

else:
    max = b

print(max)
```

Noice, How about maximum of three or an unknown number of numbers?

That'll be a pain to do manually because we have to compare all the numbers one by one.

But the only thing we are doing is `comparing`. So, to do this repeated comparing we can use a loop.

The idea is to just think that the first number is the maximum number and we start comparing it with the rest of the numbers. If we encounter a number that is greater than the maximum number, then we found the new maximum number.

And by the end of the comparison we are most definitely going to have the maximum number.

```
nums = [3,1,4,2,5,3]

max = nums[0]

loop from 1 to len(nums) -> i:
    if nums[i] > max:
        max = nums[i]

print(max)
```

Now, what about finding the second maximum number? then the third maximum number?

If we keep on `removing` the maximum number and then finding the `next` maximum number then we will get an interesting result.

```
nums = [3,1,4,2,5,3]
            ↓
1st max     5
            ↓
2nd         4
            ↓
3rd         3
            ↓
4th         3
            ↓
5th         2
            ↓
6th         1
```

We get a list of numbers that are sorted in descending order.

I just wanted to show you how almost all algorithms are connected and are improved from one problem to another.
