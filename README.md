# ROCK-PAPER-SCISSOR-GAME-OOP
Coursework Report: Rock Paper Scissors Game Application
Object-Oriented Programming - Python App

1. Introduction
1.1 Purpose and Objectives of the Application
The primary purpose of this coursework is to design and implement a classic Rock Paper Scissors game using the principles of Object-Oriented Programming (OOP) in Python. The objectives of this application are to:

Demonstrate understanding and application of core OOP concepts such as classes, objects, encapsulation, inheritance (if applicable), and polymorphism.
Develop a functional and interactive game that allows a user to play against a computer opponent.
Implement clear and modular code through the use of classes and methods.
Provide a user-friendly text-based interface for gameplay.
Incorporate basic game logic, including handling user input, generating computer choices, determining the winner, and keeping track of scores.
1.2 Brief Overview of Chosen Project
The chosen project is a text-based implementation of the popular game Rock Paper Scissors. This game involves two players simultaneously choosing one of three options: rock, paper, or scissors. The winner is determined by a set of rules: rock beats scissors, scissors beats paper, and paper beats rock. 1  If both players choose the same option, it's a tie. This project was selected due to its relatively simple ruleset, which allows for a focused application of OOP principles without being overly complex, while still providing opportunities for logical implementation and user interaction.   


2. Problem Definition and Requirements
2.1 Description of the Problem Your Application Solves
The application addresses the problem of providing a simple and engaging way for a user to play the Rock Paper Scissors game against a computer. It offers a digital version of the traditional game, eliminating the need for physical interaction and providing immediate feedback on the outcome of each round. The application aims to be a straightforward demonstration of game logic and user interaction within a Python environment, structured using object-oriented principles.

2.2 Functional and Non-Functional Requirements
Functional Requirements:

User Input: The application must allow the user to input their choice (rock, paper, or scissors) in each round.
Computer Choice Generation: The application must generate a random choice (rock, paper, or scissors) for the computer opponent in each round.
Winner Determination: The application must correctly determine the winner of each round based on the rules of Rock Paper Scissors.
Result Display: The application must display the user's choice, the computer's choice, and the outcome of each round (user wins, computer wins, or tie).
Score Tracking: The application must keep track of the user's score and the computer's score across multiple rounds.
Multiple Rounds: The application should allow the user to play multiple rounds of the game.
Game Termination: The application should provide a mechanism for the user to end the game.
Input Validation: The application should handle invalid user input gracefully and prompt the user to enter a valid choice.
Non-Functional Requirements:

Usability: The application should have a clear and easy-to-understand text-based interface.
Maintainability: The codebase should be well-structured and adhere to OOP principles to facilitate future modifications and enhancements.
Readability: The code should be well-commented and use meaningful variable and method names to enhance readability.
Efficiency: The application should execute efficiently without significant delays in processing or displaying results.
Robustness: The application should handle unexpected user input without crashing.
3. Design and Implementation
3.1 Object-Oriented Design Principles Used
The application's design leverages several key object-oriented programming principles:

Encapsulation: Data (attributes) and the methods that operate on that data are bundled together within classes. For instance, the Game class encapsulates the game state (scores, choices) and the logic (determining winner, updating scores).
Abstraction: Complex logic is hidden behind simple interfaces. The user interacts with the Game object through methods like play_round() without needing to know the intricate details of how the winner is determined or scores are updated.
Class and Object: The core of the application revolves around the creation of classes (Game, potentially Player if expanded) and their instances (objects). The Game class serves as a blueprint for the game logic, and an object of this class manages the game flow.
3.2 Class Diagrams and Structure
A simplified class diagram for the application is as follows:

Code snippet

classDiagram
    class Game {
        -user_score: int
        -computer_score: int
        -choices: list
        +__init__()
        +get_user_choice(): str
        +get_computer_choice(): str
        +determine_winner(user_choice: str, computer_choice: str): str
        +update_score(winner: str)
        +play_round(): void
        +display_score(): void
        +play_again(): bool
        +run_game(): void
    }
Class Structure:

Game Class:
Attributes:
user_score: An integer to store the user's current score.
computer_score: An integer to store the computer's current score.
choices: A list containing the possible choices: "rock", "paper", "scissors".
Methods:
__init__(): Constructor to initialize the game state (scores to 0, define choices).
get_user_choice(): Prompts the user for their choice and validates the input.
get_computer_choice(): Randomly selects a choice for the computer.
determine_winner(user_choice, computer_choice): Compares the choices and returns the winner ("user", "computer", or "tie").
update_score(winner): Increments the score of the winner.
play_round(): Orchestrates a single round of the game, including getting choices, determining the winner, and updating the score.
display_score(): Prints the current scores of the user and the computer.
play_again(): Asks the user if they want to play another round and returns a boolean.
run_game(): Contains the main game loop, controlling the flow of multiple rounds.
3.3 Key Algorithms and Data Structures Implemented
Random Choice Generation: The random.choice() function from the random module is used to implement the get_computer_choice() method, ensuring the computer makes a random selection from the available choices.
Winner Determination Logic: The determine_winner() method implements the core game rules using conditional statements (if, elif, else) to compare the user's and computer's choices and determine the winner based on the defined rules (rock beats scissors, etc.).
Data Structures:
List (choices): Used to store the possible choices in the game, making it easy to randomly select the computer's move and validate user input.
Integer Variables (user_score, computer_score): Used to keep track of the scores for both players.
4. Development Process
4.1 Tools and Environment
Operating System: [Your Operating System, e.g., Windows 10, macOS Big Sur, Linux Ubuntu]
Programming Language: Python 3.x
Integrated Development Environment (IDE) / Text Editor: [Your IDE/Text Editor, e.g., PyCharm, VS Code, Sublime Text]
Version Control System (Optional but Recommended): Git with a repository on [e.g., GitHub, GitLab, Bitbucket] was [or was not] used for version control.
4.2 Steps Followed During Development
Planning and Design:

Defined the project scope and objectives.
Identified the functional and non-functional requirements.
Conceptualized the object-oriented design, identifying the necessary classes and their responsibilities.
Sketched a basic class diagram to visualize the structure.
Implementation:

Created the Game class with its attributes (user_score, computer_score, choices).
Implemented the constructor (__init__) to initialize the game state.
Developed the get_user_choice() method to handle user input and validation.
Implemented the get_computer_choice() method using the random module.
Created the core logic in the determine_winner() method to apply the Rock Paper Scissors rules.
Implemented the update_score() method to increment the scores based on the round winner.
Developed the play_round() method to orchestrate a single round of the game.
Implemented the display_score() method to show the current scores.
Created the play_again() method to ask the user if they want to continue playing.
Developed the run_game() method containing the main game loop to manage multiple rounds.
Testing and Debugging:

Conducted informal testing after implementing each method to ensure it functioned as expected.
Ran multiple game sessions to test the overall game flow and winner determination logic.
Debugged any identified issues, such as incorrect winner determination or input validation errors.
Documentation:

Added comments to the code to explain the logic and purpose of different sections.
Prepared this coursework report to document the design, implementation, and testing process.
5. Results and Demonstration
5.1 Application Features
The implemented Rock Paper Scissors game application features:

An interactive text-based interface.
Clear prompts for user input (choosing rock, paper, or scissors).
Random selection of the computer's choice.
Accurate determination of the round winner based on the game rules.
Display of both the user's and the computer's choices for each round.
Real-time tracking and display of the user's and computer's scores.
The ability to play multiple rounds.
Input validation to handle incorrect user input.
A clear indication of the game outcome (win, lose, or tie) for each round.
A prompt to play another round at the end of each round.
5.2 Screenshots or Relevant Visuals
As this is a text-based application, screenshots of the terminal output during a game session are the most relevant visuals.

CASE 1: Start of the Game

Welcome to Rock Paper Scissors!

Enter your choice (rock, paper, scissors):
CASE 2: A Round Played (User Wins)

Enter your choice (rock, paper, scissors): rock
You chose: rock
Computer chose: scissors
You win this round!
Your score: 1, Computer score: 0
Do you want to play again? (yes/no):
CASE 3: A Round Played (Computer Wins)

Enter your choice (rock, paper, scissors): paper
You chose: paper
Computer chose: scissors
Computer wins this round!
Your score: 1, Computer score: 1
Do you want to play again? (yes/no):
CASE 4: Game Over

Enter your choice (rock, paper, scissors): no
Thanks for playing!
Final Score: User - 2, Computer - 1
6. Testing and Validation
6.1 Description of Testing Procedures
The testing process involved both manual testing and focused testing of specific functionalities:

Input Validation Testing: Tested the application's response to invalid user input (e.g., typing something other than "rock", "paper", or "scissors"). Ensured the application prompts the user to enter a valid choice again.
Winner Determination Logic Testing: Played multiple rounds covering all possible combinations of user and computer choices to verify that the winner is determined correctly according to the game rules. This included scenarios where the user wins, the computer wins, and it's a tie.
Score Tracking Testing: Monitored the score after each round to ensure that the scores are updated correctly based on the round winner.
Game Flow Testing: Played several complete game sessions, including choosing to play multiple rounds and then ending the game, to ensure the application flows as expected.
Play Again Functionality Testing: Verified that the "play again" prompt works correctly, allowing the user to continue playing or terminate the game.
6.2 Test Results and Issues Resolved

No significant issues were identified during the final testing phase. The application met all the functional requirements and demonstrated reasonable robustness in handling invalid input.

7. Conclusion and Future Work
7.1 Summary of Achievements
This coursework successfully implemented a text-based Rock Paper Scissors game using object-oriented programming principles in Python. The application effectively demonstrates the concepts of classes, objects, encapsulation, and abstraction. It provides a functional and interactive gaming experience, allowing users to play multiple rounds against a computer opponent, with accurate winner determination and score tracking. The code is structured logically within the Game class, enhancing readability and maintainability.

7.2 Recommendations for Future Improvements
While the current implementation fulfills the basic requirements, several enhancements could be considered for future development:

Graphical User Interface (GUI): Developing a GUI using libraries like Tkinter or Pygame would significantly improve the user experience, making the game more visually appealing and interactive.
Best-of-N Rounds: Implementing an option to play a "best-of-3" or "best-of-5" series of rounds.
More Sophisticated Computer AI: Instead of a purely random choice, the computer's AI could be improved to learn the user's patterns and make more strategic choices.
Player Class: Introducing a Player class to represent both the user and the computer, which could hold their name and score, would further enhance the object-oriented design.
Game History: Storing and displaying the history of moves and outcomes for each round.
Error Handling: Implementing more robust error handling for unexpected input or potential issues.
Configuration Options: Allowing users to configure game settings, such as the number of rounds or the computer's difficulty level (if AI is implemented).
These future improvements would build upon the current object-oriented foundation, further demonstrating more advanced OOP concepts and creating a more engaging and feature-rich game.
