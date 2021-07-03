# Overview

This is a simple game of tic-tac-toe developed in Python. It allows two players to play with one another on different command lines through networking. The host starts the game by *first* running `host.py`, waiting for the client to connect by *then* running `client.py`. Once their connected, the game itself starts.

The host starts as "X" and goes first, and the client is "O." The players choose the square they would like to use with coordinates; both "A1" and "1A" would be accepted, for example. The game proceeds, with the players taking turns, until one wins or the game is a draw. The host, then the client, is asked whether they'd like a rematch. If both agree, the game starts anew. 

Example of a turn:

```
       Your turn!

       A   B   C

   1     ║   ║ X
      ═══╬═══╬═══
   2     ║ O ║
      ═══╬═══╬═══
   3     ║   ║

Enter coordinate: 
```

I programmed this primarily to learn the basics of networking and how to send and receive data between two users. I also wanted to continue polishing my skills in the Python language.

Here's a link to a demo of my program: [Software Demo Video](http://youtube.link.goes.here)

# Network Communication

I used a host/client network architecture for this project using TCP (Transmission Control Protocol), and I used port 12783. The messages were sent back and forth between the host and the client thanks to the pickle module, which converts any object (in this case, a string list storing the nine squares of a tic-tac-toe grid) into a byte stream to be sent and back into an object to be read. 

# Development Environment

* Visual Studio Code
* Python (3.9.4) 64-bit
* Git / GitHub
* Python: Socket and Pickle modules

# Useful Websites

Here's a list of websites that I found helpful while working on this program:

* [Real Python: Socket Programming in Python](https://realpython.com/python-sockets/)
* [PythonProgramming.net: Sockets Tutorial with Python, Part 3](https://pythonprogramming.net/pickle-objects-sockets-tutorial-python-3/)
* [The Python Standard Libaray - Socket](https://docs.python.org/3/library/socket.html)
* [The Python Standard Libaray - Pickle](https://docs.python.org/3/library/pickle.html)
* [GitHub Guides: Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

# Future Work

Here's a list of things that I'd like to add or change in the future:

* Use Arcade (or something similar) for an easier UI than the command line
* Reprompt the user if they select an already used square instead of (currently) skipping their turn altogether
* Add a method within tic_tac_toe.py itself to check if either player has won instead of checking and double-checking between the host and client 
* Allow the players to choose their symbol since the game rules still function with other characters than "X" and "O"