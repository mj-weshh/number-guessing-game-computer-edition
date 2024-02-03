# Number Guessing Game - Computer Edition

This Python script implements a number guessing game where the computer tries to guess a user-specified number within a given range.

## Description

The script utilizes a binary search algorithm to narrow down the possible values and make intelligent guesses. The user provides feedback after each guess, indicating whether the guess is too high (H), too low (L), or correct (C).

## Getting Started

### Prerequisites

- Python 3.x installed on your machine.

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/mj-weshh/number-guessing-game-computer-edition.git
   ```

2. Change into the project directory:

   ```bash
   cd number-guessing-game-computer-edition
   ```

### Usage

Run the script using the following command:

```bash
python guessing_game_user.py
```

Follow the on-screen instructions to specify the upper limit of the range, and the computer will start guessing. Provide feedback after each guess until the computer correctly identifies the chosen number.

## Functionality

The script consists of one main function:

- `computer_guess(x)`: Implements the computer's number guessing algorithm. It takes an upper limit `x` as a parameter and iteratively narrows down the range based on user feedback until the correct number is guessed.

## Example

```python
import random

def computer_guess(x):
    low = 1
    high = x
    feedback = ""
    while feedback != 'c':
        if low != high:
            guess = random.randint(low, high)
        else:
            guess = low
        feedback = input(f"Is {guess} too high (H), too low (L), or correct (C)?: ").lower()
        if feedback == 'h':
            high = guess - 1
        elif feedback == 'l':
            low = guess + 1
    print(f"!!!The computer guessed {guess} correctly!!!")

computer_guess(100)
```

##Customization

You can customize the script by changing the argument passed to `computer_guess(x)` to set the upper limit of the range for the number guessing game.

## Contributions

Contributions are welcome! If you have any ideas for improvements or new features, feel free to open an issue or submit a pull request.
