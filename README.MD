# Number Guessing Game

## Overview
The **Number Guessing Game** is a simple interactive application built using Python and the Tkinter library. In this game, the user is prompted to guess a random number between 1 and 100. The program provides feedback if the guess is too high or too low and tracks the number of attempts. The game is designed to be user-friendly with keyboard and mouse input support, full-screen mode, and a colorful interface.

---

## Features
- **Random Number Generation**: A random number between 1 and 100 is generated when the game starts.
- **Interactive Guessing**: The user inputs guesses, and the program provides feedback such as "Too low!" or "Too high!".
- **Guess Count**: The number of attempts is displayed dynamically.
- **Keyboard & Mouse Support**: Users can press Enter or click the "Check Guess" button to submit their guess.
- **Full-Screen Mode**: The application launches in full-screen for an immersive experience.
- **User-Friendly UI**: Aesthetic design with light blue tones and centered content.
- **Exit Option**: A dedicated "Exit Game" button allows users to close the program easily.

---

## How to Play
1. **Start the Game**: Click the "Start Game" button to generate a random number between 1 and 100.
2. **Make a Guess**:
   - Enter your guess in the input field and press **Enter**.
   - Alternatively, you can click the "Check Guess" button to submit your guess.
3. **Receive Feedback**: The program will display whether your guess is too high, too low, or correct.
4. **Track Your Progress**: The number of attempts is displayed under the "Guess Count" label.
5. **Win**: Once the correct number is guessed, a congratulatory message is displayed along with the total number of attempts.
6. **Exit**: Click the "Exit Game" button to close the application.

---

## Installation
1. **Prerequisites**:
   - Python 3.x installed on your system.
   - Tkinter library (included with standard Python installations).
2. **Steps**:
   - Download the `guessing_game.py` file.
   - Open a terminal or command prompt and navigate to the directory containing the file.
   - Run the program using the following command:
     ```bash
     python guessing_game.py
     ```

---

## Code Explanation
### Key Components
1. **Random Number Generation**:
   - A random number between 1 and 100 is generated using Python's `random` module.
     ```python
     random_number = random.randint(1, 100)
     ```
2. **Event Handling**:
   - Mouse clicks are handled via the `command` parameter of buttons.
   - Keyboard input (Enter key) is handled using `bind`:
     ```python
     guess_entry.bind("<Return>", check_guess)
     ```
3. **Feedback**:
   - The program provides immediate feedback based on the guess:
     ```python
     if user_guess < random_number:
         result_label.config(text="Too low! Try again.")
     elif user_guess > random_number:
         result_label.config(text="Too high! Try again.")
     else:
         result_label.config(text="Congratulations! You guessed it!")
     ```
4. **UI Design**:
   - Full-screen mode:
     ```python
     root.attributes("-fullscreen", True)
     ```
   - Color scheme and fonts for a user-friendly interface.

---

## Screenshots
(Include screenshots of the application if possible.)

---

## Future Enhancements
- Add difficulty levels with customizable number ranges.
- Include a timer to measure how quickly the user guesses the number.
- Add a leaderboard to store high scores.

---

## License
This project is open-source and available under the [MIT License](LICENSE).

---

## Acknowledgments
- Built using Python and the Tkinter library.
- Inspired by classic number-guessing games.

---

Enjoy the game! 🎉
