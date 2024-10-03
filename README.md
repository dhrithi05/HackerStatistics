# HackerStatistics
#program to simulate dice rolls 

#Randomness has many uses in science, art, statistics, cryptography, gaming, gambling, and other fields. You're going to use randomness to simulate a game.

#All the functionality you need is contained in the random package, a sub-package of numpy. In this exercise, you'll be using two functions from this package:

#seed(): sets the random seed, so that your results are reproducible between simulations. As an argument, it takes an integer of your choosing. If you call the function, no output will be generated.
#rand(): if you don't specify any arguments, it generates a random float between zero and one.

**Roll the dice
**
you can just as well use randint(), also a function of the random package, to generate integers randomly. The following call generates the integer 4, 5, 6 or 7 randomly. 8 is not included.

**import numpy as np
np.random.randint(4, 8)**

In the Empire State Building bet, your next move depends on the number you get after throwing the dice. We can perfectly code this with an if-elif-else construct!
