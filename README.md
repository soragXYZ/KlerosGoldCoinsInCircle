# Gold coins in circle

Consider a game with n players, seated in a circle. Each player begins with one gold coin. Then player 1 gives a gold coin to player 2, who then gives two gold coins to player 3. This continues with each player alternating between giving one gold coin or giving two gold coins to the next player that still has at least one gold coin. Players that at some point have no gold coins are eliminated and leave the circle. Show that there are infinitely values of n for which the game terminates and a single player finishes with all of the gold coins.  

Let us show by recurrence on n belonging to N the following property:  
For a number of players 2^n starting with the same number x of pieces (x belonging to N*), the game always ends with 1 player owning all the other pieces = nx  

For n = 0, the player is alone, so he has won the game with all the pieces  
Initialization for n = 1:  
By denoting J1i the number of pieces of J1 at round i, and J2i the number of pieces of J2 at round i, we therefore have:
J1i+1 = J1i + 1 and J2i+1 = J2i - 1 with J10 = x and J20 = x
J1i and J2i are arithmetic sequences with a ratio of 1 and -1 respectively, which can therefore be rewritten in the form:
J1i = x + i and J2i = x - i  
Since x belongs to N*, there exists i such that i = x, i.e. J1x = 2x and J2x = 0  
Which is to say that J1 won and J2 lost.  

Inheritance: Suppose the property is true at rank n, ie
For a number of players 2^n starting with the same number x of pieces (x belonging to N*), the game always ends with 1 remaining player owning all the other pieces = nX  

Let's start a game with 2^(n+1) players each having x pieces at the start. So there is a total of 2^(n+1)x pieces  
We note Jri the player number r in game turn number i  
An even player receives 2 coins from his neighbour, and gives 1, while it is the opposite for an odd player, so we have Jri = x + i if r is even and Jri = x - i if r is odd  
As before, there exists a rank i such that i = X, so we have:
Jri = 2x if r is even, Jri = O if r is odd  
Which is equivalent to say that out of 2^(n+1) players, half of the players have been eliminated: all the odd players have given all their coins to their neighbor  
There are therefore 2^n players in play, each with 2X tokens.
However, according to the heredity property stated above, the game therefore ends with 1 remaining player owning all the other pieces = 4^nx = 2^(n+1)x  

The inheritance property is therefore kept at rank n+1  

Conclusion: For a number of players 2^n starting with the same number x of pieces (x belonging to N*), the game always ends with 1 player owning all the other pieces = 2^nx  

Thus there are infinitely many values ​​of n for which the game ends with a player having all the pieces