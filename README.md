# Brute-Force Sorting

We talked about the complexity of the sorting problem, and used an argument over
all permutations of a list to be sorted to determine its complexity. Implement
a function to sort a list by systematically trying all permutations of the input
list, using the template in `code.js`. Test your new function; I've provided
some basic testing code that uses [jsverify](https://jsverify.github.io/) in
`code.test.js`.

The return value should be the number of permutations that were tried until the
sorted list was "discovered". The unsorted list passed as an argument should be
sorted, i.e. do not copy the list and sort the copy.

## Runtime Analysis

What is the runtime complexity of the algorithm that you implemented? What does
a best case input for your implementation look like, what does a worst case
input look like? How would this complexity change if you generated permutations
randomly without memory instead of systematically trying them?

Describe your reasoning and the conclusion you've come to. Your reasoning is the
most important part. Add your answer to this markdown file.

## Plagarism Statement

All exercises must contain the following statement:
“I certify that I have listed all sources used to complete this exercise, including the use
of any Large Language Models. All of the work is my own, except where stated
otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is
suspected, charges may be filed against me without prior notice.”

## Note
I am attempting this from scratch, I will compare it to my last semesters repository and make any corrections needed based on that code and response.

## Answer

The best case would be if innitial list was already in order, then the algorithm would just have to check once to confirm the order, which has a runtime complexity of $\Theta(n)$. On the otherhand the worst case depends on the implementation of the algorithm, with the difference being whether or not you keep track of the permutations that occur. In order to ensure the brute force will eventually find the sorted list, keeping trtack of the previously generated permutations is key, the complexity for this is $\Theta(n*n!)$, because $n!$ is the maximum number of possible permutations for a list of a given size, and $n$ comes from checking the prior permutations. Another way of brute forcing is randomly generating permutations but without keeping track of them as they are generate, with this algorithm, there is not garuntee that the correctly ordered list will ever be found, so the runtime complexity is infinity in that case.
