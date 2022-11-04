# Algorithms

Algorithm questions are essentially Leetcode-style questions, although some companies can get a bit more creative with them.

The MOST important thing to remember about doing algorithm problems is that 

> Quant firms are looking for precise, efficient, maintainable and readable code.

This might sound obvious to you, but to dig into this a bit deeper, let's talk about red flags

- **Coding right away without asking clarifying questions**
  - How are you going to write good code if you don't know what you're writing in the first place? While you could just be a god and write perfect code the first go, this is extremely unlikely, and also just a poor strategy, even if you are extremely good at coding. Even if you can code it perfectly, asking clarifying questions shows that you have a deeper understanding of the problem, and are willing to anticipate issues if they arise.

- **Needing to iterate many times on the code to cover edge cases**
  - If you come from big tech, you may be used to iterating quickly, but for Quant interviews, that's the _opposite_ of what they want to see. Besides, if you're on the job and you need to iterate many times on a trading algorithm that is executing, that can potentially lose lots of money! Therefore, what you should be doing in your interview is thinking ahead a lot about your code, and when you do code, make sure that you cover as many cases as reasonable, and that your code is correct. 
  
  It also helps to convince your interviewer that your code is correct, as it is both frustrating to your interviewer if they have to work hard to find bugs in your code, and also shows that you're not a careful coder as well.

- **Not identifying weaknesses in the code**
  - It's cliche to say everything has tradeoffs, but that's true! When you're done with the code, it's always a good time to mention what you thought about the pros and cons of your solution, and how you may try to achieve more of one factor while sacrificing another. Also defending your solution is a good engineering skill to have, so if you can explain and defend clearly, you are doing very well.

## Types of Questions

### Data structures

These questions are usually something related to a classic data structure, such as an array, linked list, queue, hash table, etc. and you are asked to implement it from scratch, in a variety of ways, and explain the pros and cons.

Problems:

- Implement a Queue from scratch, using
  - Linked Lists (Singly, Doubly)
  - Dynamically sizable arrays
    - Circular vs. not?
- Implement LRU Cache

### Algorithms

Even though Leetcode is pretty common, more and more trading companies are giving coding questions that "actually relate to their day-to-day job." While this is probably a bit far-fetched, a lot of companies are starting to use trading-related questions. In all fairness, there aren't that many trading-type questions that you can ask in an hour time frame, so you'll notice that questions will start having a common pattern.

Problems:
- TODO

### Games

Some firms like to see you do mini-projects, and see how you can code large volumes in a short time, manage a medium-sized codebase, use object oriented programming principles, and implement medium-complex algorithms.

Examples of games:

- Tetris
- Connect Four
- Chess
- Poker
- [2048](https://play2048.co/)

It's usually not hard to understand what your task is, but to organize your thoughts, design, and actually execute the mini-project can be difficult.

## Complexity Theory

Most CS curriculums include complexity theory at some point, and some firms care about what you know about complexity analysis of algorithms, and specifically if something is `NP-hard`.

If you remember from class `NP-hard` problems are the class of problems where we have an exponential solution, but we don't know if a polynomial solution exists (actually I'm describing `NP-Complete`, since `NP-hard` problems also encompass more difficult problems as well). A classic `NP-hard` problem is subset sum, where we are given `x_1, x_2, ..., x_n`, and we want to know if some subset of the `x_i` sums up a target sum `S`. 

In this case, the exponential solution is pretty naive, just try all `2^n` subsets and see if any sum up to `S`. No polynomial algorithm is currently known (or may ever be known).

The usual question relating to `NP-hardness` is that you may be presented with an `NP-hard` problem, usually it will be disguised like another problem, and then you will need to do a subset of the following:

1. Recognize that the problem is `NP-hard`
  - Sometimes you need to prove this, usually `NP-complete`, and you do this by reducing the problem to an `NP-Complete` problem, and then doing it the other way as well.
  - This is usually the most important step, because if you don't recognize that it is `NP-hard`, then you will likely end up just using a greedy algorithm and incorrectly saying that it's the exact solution.
2. Present a naive solution for the problem
  - This will likely run in exponential time 
3. Present a polynomial approximate solution
  - This solution will run in poly time, but will not be an exact solution. Sometimes they ask for how good the approximation is.

## How to Approach Different Types of Coding Questions

[Please check out this article I wrote about this topic.](https://github.com/mikinty/ace-the-code-interview)