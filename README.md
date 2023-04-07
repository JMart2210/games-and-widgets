# Games & Widgets
# Tic-Tac-Toe
**Live version here**: https://jmart2210.github.io/top-tic-tac-toe/<br/>
A classic tic-tac-toe game built with modularity, separation of concerns, and event-driven programming in mind. <br />
The interface has been designed with responsive design principles and supports both desktop and mobile devices.<br />
The code includes a gamePlayModule that handles the game logic, including player turns, checking for win conditions, and updating the game board. The module uses an object-oriented approach and encapsulation to manage game state and track player information.<br />
**Optimizations**: I made the cpu move selection to first return if there is a winning move, second if your opponent has a "losing" move so you can block it, and lastly the next best moved based on how useful it appears to be. It determines usefulness by brute force, comparing how many times a given move shows up in the remaining winning combos. Currently the cpu is unbeatable. I think it would be fun to implement another difficulty setting where the cpu selection has a chance to be randomized when there is no obvious move (nothing that wins or loses the game). This would allow potential blunders that the user may be able to take advantage of.<br/>
<img src="./tic-tac-toe/tic-tac-toe-example.gif" alt="Tic-Tac-Toe example">
# Calculator
A fully functional calculator built with HTML, CSS, and Javascript, supporting both mouse and key-stroke input. The basic functionality was fairly simple. The trickiest parts were the details of the edge cases. <br/>
For example: when someone completes an operation, let's say 5+3. They might hit the equals key to display the result (8), or they might continue their operation, hitting the plus key and the next number to make 5+3+2. The specs of the project were to only allow one operation at a time, so we couldn't just keep a record of all operations and compute at the end, it needed to compute at every step. <br/>
The tricky part was they could also hit the equals key to get the result. The user inputs 5+3+2=(10) They may want to continue operating from the (10), hitting one of the operation buttons next. Or they may want to move on to another problem. They could always hit the clear button, but I wanted it to be intuitive, and it's very likely they would expect that just hitting the next number would start the next operation. <br/>
I resolved this by storing a temporary result, the next operand, and a boolean variable "first". I then implemented some conditional logic with those variables to make the program function intuitively. I heavily commented the code to explain my thought process at each step.<br/>
**Live version here**: https://jmart2210.github.io/calculator/ <br/>
<img src="./calculator/calculator.gif" alt="Calculator Example Gif">
# This is War
Simple implementation of the classic card game War.

**Live version here**: https://jmart2210.github.io/this-is-war/

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, & Deck of Cards API

The Deck of Cards API request happens at page load. The deck is distributed evenly between each player as an array. Each round the top card is drawn from the hands and compared. The player with the higher card takes the pot. If the initial cards are equal, a "war" ensues, increasing the stakes. Instead of just pushing the pot to the back of the winning player's hand, I chose to give each player a "wins" pile separate from their hand. Currently there is no benefit to doing it this way, but there are a number of optimizations I could make that would make use of the additional architecture. 