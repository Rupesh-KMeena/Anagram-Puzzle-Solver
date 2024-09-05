# Anagram Game

This is a simple word-based game where the player finds anagrams for given words. The game starts easy and gradually becomes more difficult as longer words are introduced.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Game Rules](#game-rules)
- [Files](#files)
- [How It Works](#how-it-works)

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/anagram-game.git
    cd anagram-game
    ```

2. **Install Dependencies**:
   This game doesn't require any external dependencies, so you're good to go with Python 3 installed.

3. **Prepare Word Files**:
   Place two word files in the `resources/` directory:
   - `many-words.txt`: A large list of around 50,000 words used to generate the anagrams.
   - `common-words.txt`: A smaller list of around 3,000 common words used as prompts in the game.
   
   Ensure that each file contains one word per line, and lines starting with `#` will be ignored.

## Usage

1. **Run the game**:
    ```bash
    python anagram_game.py
    ```

2. **Gameplay**:
   - You will be prompted with a word, and your task is to provide an anagram (another word formed by rearranging the letters of the original word).
   - The game will start with shorter words and progressively use longer words as you answer correctly.

## Game Rules

- You must provide an anagram from the list of accepted words. 
- For each correct answer, the difficulty increases.
- The game will end only when you provide an incorrect answer, at which point you will be shown the correct answer.

## Files

- `anagram_game.py`: Main game script that runs the anagram game.
- `anagrams.py`: Logic for finding and grouping anagrams.
- `words.py`: Utility functions for reading word lists and processing words by length.
- `resources/many-words.txt`: The large word list for generating anagrams.
- `resources/common-words.txt`: The smaller list of common words used in the game.

## How It Works

- The game reads two word files:
  - **Common Words**: Used as prompts in the game.
  - **Many Words**: A larger list used to find all possible anagrams for the prompts.
  
- It groups words into sets of anagrams and randomly selects a word for you to provide an anagram for. If you guess correctly, the word length increases after every few correct answers, making the game more challenging.
