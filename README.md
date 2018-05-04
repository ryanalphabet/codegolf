### Objective: Simulate a game of Snakes and Ladders

## Rules of Snakes and Ladders
The objective of the game is to get the game piece to the end of the game board using a series of moves.
Each move is started with a roll of a die. The game piece is then moved forwards on the game board
as many places as determined by the value of the die. If the resulting position is a snake, the game piece
is moved backwards on the board by 5 places. If the resulting position is a ladder, the game piece is moved
forward on the board by 7 places. Play continues as the game piece progresses to the end of the board.
To complete the game, the game piece must land exactly on the last piece of the board. If the game piece
overshoots the last piece of the board, the die must be rerolled.

Snakes *CAN NOT* be placed so that it would move the player to a negative board position.

Ladders *CAN* be placed so that it would move the player past the end position. If this happens, print "LADDERWINNER!" and end the game.

## Challenge:

Create a function that takes three arguments:
1. The game board array
2. The amount of moves a snake moves the player backwards.
3. The amount of moves a ladder moves the player forwards.

The function should simulate a game of snakes and ladders and outputs the results.
Each move should be printed on a new line in the following format:

`X->Y[,S|L->Z]`

X = Die value

Y = New position

S|L = Landed on a snake or ladder

Z = New position after adjustment

If a reroll is required, the format should be:
`X->Y,Rerolling`

When the game completes, the format should be:
`X->Y,Finished`

Starting position is 1.

Dice rolls should yield an integer value of [1, 2, 3, 4, 5, 6]

# Examples:

(Based on a snake being -5, and a ladder being +7)

Rolling a 4 on from position 1:
`4->5`

Rolling a 3 on from position 20 and landing on a snake:5
`3->23,S->18`

Rolling a 4 on from position 12 and landing on a ladder:
`4->16,L->23`

Rolling a 5 on from position 97 and having to reroll:
`5->102,Rerolling`

Rolling a 4 on from position 96 and finishing the game:
`4->100,Finished`

Rolling a 3 on from position 90, landing on a ladder:
`3->93,LADDERWINNER!`

The board will consist of a one dimensional array containing all board positions, snakes, and ladders.

For example, a 3 x 3 board would be represented as:

`['.', '.', '.', L, '.', S, '.', '.']`

Die rolls should be random.

It should output no errors or warnings.

Only the function body is counted for characters.

An example call to the method would look like:

`snakesAndLadders(['.', '.', '.', L, '.', S, '.', '.'], 5, 7)`
