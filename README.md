# Tic-Tac-Toe
1. Project Overview
1.1 Project Title
Tic Tac Toe - A C Programming Mini-Project
1.2 Project Objective
The main objective of this project is to create a simple, text-based Tic Tac Toe game using the C programming language. The game involves two players who take turns to mark their symbols ('X' or 'O') on a 3x3 grid. The game checks for win conditions and declares the winner or a draw if no player wins.
1.3 Scope of the Project
•	Implement a 3x3 Tic Tac Toe game in C.
•	Allow two players to take turns.
•	Check for winning conditions after each move.
•	Display the game board after each turn.
•	Declare the result when the game ends (win or draw).

2. Software and Hardware Requirements
2.1 Software Requirements
•	Operating System: Windows, Linux, or macOS
•	Compiler: GCC (GNU Compiler Collection) or any C compiler
•	IDE/Editor: Code::Blocks, Visual Studio Code, or any standard C programming IDE
•	Libraries Used:
o	<stdio.h>: Standard I/O functions.
o	<conio.h>: Console handling for functions like getch() (Windows-specific).
o	<stdlib.h>: System functions like system("cls") to clear the console.
2.2 Hardware Requirements
•	Processor: Intel Core i3 or higher
•	RAM: Minimum 4GB
•	Disk Space: 50MB for IDE and compiler
•	Display: 800x600 resolution or higher
p
3. Project Design
3.1 Data Structure
The game board is represented by a 1-dimensional character array (arr[10]). The index numbers (1 to 9) correspond to the grid positions on the 3x3 board, making it easy to check for win conditions and update the board.
3.2 Logic Flow
1.	Initialize the Board: Display numbers (1-9) representing available positions.
2.	Input Handling: Players take turns to choose a cell.
3.	Update the Board: Mark the selected cell with the player's symbol ('X' or 'O').
4.	Check Win: After every move, check if there is a winning combination.
5.	End the Game: Declare the result (Win or Draw).
3.3 Functional Modules
•	showBoard(): Function to display the current state of the game board.
•	checkForWin(): Function to check if any player has won or if the game has ended in a draw.
•	main(): The driver function handling game flow and player interaction.

4. Implementation
4.1 Code Explanation
4.1.1 Main Function
The main() function acts as the game controller:
•	Initializes the game.
•	Alternates between Player 1 and Player 2 using a player variable.
•	Displays the game board and prompts the current player for a move.
•	Checks for valid inputs, updates the board, and verifies winning conditions.
•	Declares the result and ends the game if necessary.
4.1.2 showBoard() Function
Displays the current status of the 3x3 game board:
void showBoard() {
    system("cls");  // Clears the screen for a fresh view
    printf("\tTIC TAC TOE\n");
    printf("       |       |      \n");
    printf("   %c   |   %c   |   %c   \n", arr[1], arr[2], arr[3]);
    printf("       |       |      \n");
    printf("-------|-------|-------\n");
    printf("       |       |      \n");
    printf("   %c   |   %c   |   %c   \n", arr[4], arr[5], arr[6]);
    printf("       |       |      \n");
    printf("-------|-------|-------\n");
    printf("       |       |      \n");
    printf("   %c   |   %c   |   %c   \n", arr[7], arr[8], arr[9]);
    printf("       |       |      \n");
}

4.1.3 checkForWin() Function
Checks for any winning conditions based on rows, columns, and diagonals:
int checkForWin() {
    // Win conditions: Rows, Columns, and Diagonals
    if (arr[1] == arr[2] && arr[2] == arr[3]) return 1;
    else if (arr[4] == arr[5] && arr[5] == arr[6]) return 1;
    else if (arr[7] == arr[8] && arr[8] == arr[9]) return 1;
    else if (arr[1] == arr[4] && arr[4] == arr[7]) return 1;
    else if (arr[2] == arr[5] && arr[5] == arr[8]) return 1;
    else if (arr[3] == arr[6] && arr[6] == arr[9]) return 1;
    else if (arr[1] == arr[5] && arr[5] == arr[9]) return 1;
    else if (arr[3] == arr[5] && arr[5] == arr[7]) return 1;
    else if (arr[1] != '1' && arr[2] != '2' && arr[3] != '3' &&
             arr[4] != '4' && arr[5] != '5' && arr[6] != '6' &&
             arr[7] != '7' && arr[8] != '8' && arr[9] != '9') 
	return 0;
    else return -1;
}

4.2 Code Execution
1.	Compile the program using a C compiler.
2.	Run the executable file to start the game.
3.	Follow the on-screen instructions to play the game.

5. Testing and Validation
5.1 Test Cases
Test Case No.	Input	Expected Output	Result
1	Valid move (Player 1)	Board updates with 'X'	Pass
2	Valid move (Player 2)	Board updates with 'O'	Pass
3	Invalid move (occupied)	Error message, ask for new input	Pass
4	Winning row	Declare player win	Pass
5	Winning column	Declare player win	Pass
6	Winning diagonal	Declare player win	Pass
7	Full board, no winner	Declare game draw	Pass
5.2 Observations
The program successfully handles all expected scenarios. It checks for valid inputs, correctly updates the game state, and accurately detects the game's result.

6. Conclusion
6.1 Project Summary
The Tic Tac Toe game project demonstrates how a simple game can be built using fundamental C programming concepts. The project provides a hands-on application of control flow, user input handling, and game logic.
6.2 Learning Outcomes
•	Understanding of basic array operations.
•	Practice with loops, conditionals, and functions.
•	Experience in handling user input validation.
•	Knowledge of game mechanics and logic implementation.

7. Future Enhancements
•	Implement a single-player mode with AI.
•	Add a graphical user interface (GUI) for a more interactive experience.
•	Provide sound effects and animations for visual appeal.
•	Implement an online version for remote play with other users.
