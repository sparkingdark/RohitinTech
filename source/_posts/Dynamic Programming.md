title: Dynamic Programming 
tags: ["Dynamic Programming"] 
---
# Dynamic Programming

Dynamic Programming (DP) is a method for solving problems by breaking them down into a collection of simpler subproblems, solving each of those subproblems just once, and storing their solutions. It is only an optimization technique. [ [1](https://www.freecodecamp.org/news/follow-these-steps-to-solve-any-dynamic-programming-interview-problem-cc98e508cd0e/) ]

After this definition, I have a claim:

> DP is a child of recursion.

You want proof?

Let me break it down for you —

In recursion, we follow a top-down approach. We start with the biggest instance, break it down into smaller instances then combine answers to get the final solution.

But in DP we follow a bottom-up approach. We first start with smaller instances and then use those solutions to compute the final solution ( bigger instances ).

Notice, how similar they sound.

## How to identify a DP problem?

DP is just an optimization technique.

You need to first see how to solve the problem recursively.

If the sub problems overlap, you can use DP to optimize the solution.

### How to check if a problem can be solved recursively?

- There will be choices.

    For each individual input data, you will have a choice to either include it into your final solution or discard it.

    Problem with such choices should be solved using Recursion.

    But there is a type of recursive solution in which there is an overlap between function calls i.e. there is a possibilty where some function calls are computing same value using same input multiple times.

    In this type of situation, we use DP to optimize the solution.

- Some optimal solution would be asked.

    Minimum/ Maximum or some optimal case.

## How to solve a DP problem?

First try finding a recursive solution.

Trust me with this.

I have tried multiple times to to come up with the top down approach first.

But it is really hard and it takes time.

During a competition or a job interview, the only thing that you don’t have is time.

Plus what takes time, can increase chances of messing up.

So please trust me and try to find the recursive solution first.

Steps to find the recursive solution -

1. Try thinking of the bigger problem in terms of subproblems. subproblems that are small enough to be solved easily and yet they contribute to the final solution.
2. Conclude how the subproblems contribute to the final solution.
3. Write Return type of the recursive solution.
4. Write inputs for the recursive solution ( function arguments )
5. Write Base Condition.
6. Create a Decision Tree. Based on it complete rest of the function.
7. Then memoize your recursive solution using a table. This will help you when there are multiple function call that have the same input.
- Just in case you want to know what memoize means:

    **Memoization** means the optimization technique where
    you memorize previously computed results, which will be used whenever
    the same result will be needed.

    Memoization comes from the word "memoize" or "memorize". [ [2](https://cs.stackexchange.com/questions/99513/dynamic-programming-vs-memoization) ]

I know this steps seems vague.

But you will start drawing meaning from it once you actually follow the process.

If you use this approach, the solution will be able to pass all the test cases.

### Top down approach.

Once you have a recursive solution in place. Convert it into an iterative solution. There you go, you have a top down approach based solution.