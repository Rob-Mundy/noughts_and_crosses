# Noughts and Crosses

[View the live project here](https://noughts-and-crosses-rm.herokuapp.com/)

NOUGHTS & CROSSES is a Python terminal-based version of the classic paper and pencil game also known as "Tic-tac-toe".

Users can try to beat the computer by placing 3 of their marks (x's or o's) in a row.

+ ## How to play

NOUGHTS & CROSSES is a classic strategy game that can trace its roots back to the Romans or even ancient Egyptians!  [See wikipedia for more info](https://en.wikipedia.org/wiki/Tic-tac-toe).

There are 8 possible ways to win by placing 3 of your chosen marks in a row horizontally, vertically or diagonally.

A stalemate will be declared if all of the spaces are populated without either player placing 3 in a row.

In this version the player inputs ther choice of mar (x or o) and the initial board is drawn.

Rather than presenting empty spaces and using coordinates, the available spaces on the board are presented as numbers 1 - 9, arranged as they would be on a keypad.

The game alternates between the user and computer, whose marks are entered onto the board in place of the initial grid numbers.

The winner is the player that places 3 of their marks in a row.

# Features

+ ## Existing Features
    
    + 

    + 

+ ## Future Features

    + Add a play again function to reset the board.

    + Add the option for two-player mode rather than user vs computer.

    + Apply some logic to make the computer more competitive as playing against randomly-generated moves isn't particularly challenging.

# Testing

I have manually tested this project in the following ways: 

+ The program passed through [pythonchecker.com](https://www.pythonchecker.com/) without any hints.

+ I have tested the [README.md](https://github.com/Rob-Mundy/Noughts_and_Crosses#readme) file with the [MD Reader](https://chrome.google.com/webstore/detail/md-reader/medapdbncneneejhbgcjceippjlfkmkg) extension for Chrome.

# Bugs

+ I noticed that the computer's turn was returning the same sequence of numbers despite it being generated via a random function. I found an article on [stackoverflow.com](https://stackoverflow.com/questions/47937813/random-choice-not-acting-random-at-all) that mentioned that lists are only evaluated once, so it was necessary to shuffle the list of available spaces (random.shuffle) before the computer's turn in order to get a truly random outcome.

+ I reached the terminal row limit when testing my initial Heroku deployment which meant the game could not be completed. This was resolved by clearing the terminal each round instead of prining multiple versions of the board.  See function replace_terminal() for details.

+ The computer's turn was printed to the terminal far too quickly for the user to read, so I found a set of libraries and a function that mimics typing so that the information can be properly digested each turn.  See function simulate_typing() for details.

+ There are no outstanding bugs

# Deployment

## Heroku 

The site was deployed to Heroku via the following process:

+ 

# Credits

## Content

+ replace_terminal() - The idea for clearing/replacing the terminal was sourced from [stackoverflow.com](https://stackoverflow.com/questions/2084508/clear-terminal-in-python).

+ simulate_typing() - The code to simulate typing while printing was also sourced from [stackoverflow.com](https://stackoverflow.com/questions/58763136/printing-every-thing-slowly-simulate-typing)