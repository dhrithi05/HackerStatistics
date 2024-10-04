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

Additional understanding
all_walks is a list of lists: every sub-list represents a single random walk. If you convert this list of lists to a NumPy array, you can start making interesting plots! matplotlib.pyplot is already imported as plt.

Use np.array() to convert all_walks to a NumPy array, np_aw.
Try to use plt.plot() on np_aw. Also include plt.show(). Does it work out of the box?
Transpose np_aw by calling np.transpose() on np_aw. Call the result np_aw_t. Now every row in np_all_walks represents the position after 1 throw for the five random walks.
Use plt.plot() to plot np_aw_t; also include a plt.show(). Does it look better this time?


Taking clumsiness into consideration. ie, the chances of falling down
You're a bit clumsy and you have a 0.5% chance of falling down. That calls for another random number generation. Basically, you can generate a random float between 0 and 1. If this value is less than or equal to 0.005, you should reset step to 0. use np.random.rand()

To make sure we've got enough simulations, go crazy. Simulate the random walk 500 times.
From np_aw_t, select the last row. This contains the endpoint of all 500 random walks you've simulated. Store this NumPy array as ends.
Use plt.hist() to build a histogram of ends. Don't forget plt.show() to display the plot.


The histogram of the previous exercise was created from a NumPy array ends, that contains 500 integers. Each integer represents the end point of a random walk. To calculate the chance that this end point is greater than or equal to 60, you can count the number of integers in ends that are greater than or equal to 60 and divide that number by 500, the total number of simulations.

Well then, what's the estimated chance that you'll reach at least 60 steps high if you play this Empire State Building game? 
