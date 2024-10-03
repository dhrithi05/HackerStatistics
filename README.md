# HackerStatistics
Task:

Let's imagine that we are planning to walk up the stairs of the Empire State Building with a friend who proposes a bet that is to roll a regular 6-sided die 100 times and move up or down the stairs based on the numbers rolled, as follows:

If it's 1 or 2, we'll go one step down.
If it's 3, 4, or 5, we'll go one step up.
If we throw a 6, we'll throw the die again and will walk up the resulting number of steps.
We can not go lower than step number 0. We admit that we're a bit clumsy and have a chance of 0.1% falling down the stairs when we make a move. Falling means that we have to start again from step 0.

With all of this in mind, we bet with our friend that we'll reach 60 steps high.

program to simulate dice rolls 

Randomness has many uses in science, art, statistics, cryptography, gaming, gambling, and other fields. You're going to use randomness to simulate a game.

All the functionality you need is contained in the random package, a sub-package of numpy. In this exercise, you'll be using two functions from this package:

seed(): sets the random seed, so that your results are reproducible between simulations. As an argument, it takes an integer of your choosing. If you call the function, no output will be generated.
rand(): if you don't specify any arguments, it generates a random float between zero and one.

**Roll the dice
**
you can just as well use randint(), also a function of the random package, to generate integers randomly. The following call generates the integer 4, 5, 6 or 7 randomly. 8 is not included.

**import numpy as np
np.random.randint(4, 8)**

In the Empire State Building bet, your next move depends on the number you get after throwing the dice. We can perfectly code this with an if-elif-else construct!
