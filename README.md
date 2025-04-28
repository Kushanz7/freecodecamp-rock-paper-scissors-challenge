# Rock Paper Scissors

This is the boilerplate for the Rock Paper Scissors project. Instructions for building your project can be found at https://www.freecodecamp.org/learn/machine-learning-with-python/machine-learning-with-python-projects/rock-paper-scissors

This repository contains the code for an AI player designed to play the game Rock Paper Scissors. The goal of this project was to create an AI that can learn and adapt its strategy to win against different opponent bots.

## Project Goal

The primary objective was to develop a `player` function (within `RPS.py`) that can consistently win at least 60% of games against four distinct opponent bots with varying strategies.

## Files in this Repository

* **`RPS.py`**: This file contains the core logic of the AI player, including the `player` function that determines the AI's next move based on the opponent's previous plays.
* **`RPS_game.py`**: This file (which should **not** be modified) defines the game environment, the opponent bots (`quincy`, `abbey`, `kris`, `mrugesh`), and the `play` function used to run matches between players.
* **`main.py`**: This file is provided for development and testing. You can use it to play games between your AI player and the built-in bots.
* **`test_module.py`**: This file contains the unit tests used to evaluate the performance of your `player` function against the challenge requirements.
* **`README.md`**: (This file) Provides an overview of the project.

## How to Use

1.  **Clone the repository:**
    ```bash
    git clone <repository_url>
    cd <repository_name>
    ```

2.  **Develop your AI player:**
    - Modify the `player` function in `RPS.py` to implement your winning strategy.
    - You can use the provided example code as a starting point.
    - The `player` function receives the opponent's last move as input and should return the AI's next move ('R', 'P', or 'S').
    - You can maintain state between games using the optional `opponent_history` argument (or by managing your own state within the function's scope).

3.  **Test your AI:**
    - Use the `main.py` file to test your `player` function against the different bots. For example:
      ```bash
      python main.py
      ```
    - You can modify `main.py` to run specific matches with a desired number of games and verbosity.
      ```python
      from RPS_game import play, quincy, abbey, kris, mrugesh
      from RPS import player

      # Example: Play 1000 games against quincy with verbose output
      play(player, quincy, 1000, verbose=True)

      # Uncomment the last line in main.py to run the automated tests
      # from test_module import *
      # unittest.main('test_module', exit=False)
      ```

4.  **Run the tests:**
    - To check if your AI meets the challenge requirements, uncomment the last lines in `main.py` to run the unit tests.
      ```python
      from test_module import *
      import unittest

      unittest.main('test_module', exit=False)
      ```
    - Your AI must achieve a win rate of at least 60% against each of the four bots to pass the challenge.

## Hints and Strategies

* Observe the behavior of each opponent bot. They have different strategies!
* Your `player` function might need to implement different counter-strategies depending on the opponent.
* Keeping track of the opponent's history is crucial for identifying patterns.
* Consider implementing frequency analysis, pattern recognition, or more advanced game theory concepts.
