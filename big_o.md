# Introductions to Big O notation

An algorithms can be seen as a recipe for a computer to follow.
It is a set of instructions that a computer will follow step-by-step
to solve a problem.

Algorithms take an input and produce an output. The output
will be the answer to a question regarding the input.
For example, let's say you had  a non-empty array of positive integers called `nums`,
and you wanted to answer the question: "What is the largest number in `nums`?".

To answer this question, you would write an algorithm that takes an array called `nums`
as **input**, and **outputs** the largest number in `nums`. Here is and example of such 
an algorithm:

1. Create a variable `maxNum` and initialize it to `0`;
2. Iterate over each element `num` in `nums`;
3. If `num` is greater than `maxNum`, update `maxNum = num`;
4. Output `maxNum`;

Here, we have written down a set of instructions that when follow, will solve the problem.
We can now implement these instructions in code so that a computer can quickly solve the problem.
There are some important requirements for algorithms:

1. Algorithms should be **deterministic**. Given the same **input**, 
the algorithm should **always** produce the same **output**. Basically, there shouldn't be any randomness;
2. The algorithm should be correct for any arbitrary valid **input**.
In our example, we said that `nums` is a non-empty array of positive integers.
There are infinitely many of such arrays, and our algorithm works for **all** of them.
Note that if `nums` had negative numbers, the input would be invalid since we stated the integers are positive.
In fact, our algorithm would actually break because we initialized `maxNum` to `0`, so if all of `nums` was negative,
we would incorrectly output `0`.

<hr>

# Big O

Big O is a notation used to describe the computational complexity of an algorithm.
The computational complexity of an algorithm is split into two parts: time complexity and space complexity.
The time complexity of an algorithm is the amount of time the algorithm needs to run relative to the input size.
The space complexity of an algorithm is the amount of memory allocated by the algorithm whe run relative 
to the input size.

> Typically, people care about the time complexity more than
> space complexity, but both are important to know.

Time complexity: as the input size grows, how much longer does the algorithm take to complete?

Space complexity: as the input size grows, how much more memory does the algorithm use?

<hr>