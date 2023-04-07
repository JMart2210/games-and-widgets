# Games & Widgets

# Calculator
A fully functional calculator built with HTML, CSS, and Javascript, supporting both mouse and key-stroke input. The basic functionality was fairly simple. The trickiest parts were the details of the edge cases. <br/>
For example: when someone completes an operation, let's say 5+3. They might hit the equals key to display the result (8), or they might continue their operation, hitting the plus key and the next number to make 5+3+2. The specs of the project were to only allow one operation at a time, so we couldn't just keep a record of all operations and compute at the end, it needed to compute at every step. <br/>
The tricky part was they could also hit the equals key to get the result. The user inputs 5+3+2=(10) They may want to continue operating from the (10), hitting one of the operation buttons next. Or they may want to move on to another problem. They could always hit the clear button, but I wanted it to be intuitive, and it's very likely they would expect that just hitting the next number would start the next operation. <br/>
I resolved this by storing a temporary result, the next operand, and a boolean variable "first". I then implemented some conditional logic with those variables to make the program function intuitively. I heavily commented the code to explain my thought process at each step.<br/>
**Live version here**: https://jmart2210.github.io/calculator/ <br/>
<img src="./calculator/calculator.gif" alt="Calculator Example Gif">