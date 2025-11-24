# Guessing-Game-Uniqueness-
🔐 A simple Python Password Guessing Game with easy, medium, and hard levels. Randomly selects a secret word, tracks attempts, and gives hints showing correct letters in the right positions. Built using pure Python and the random module, perfect for beginners to practice loops, lists, and string logic.

import random
easy_words = ["apple", "train", "tiger","money", "india", ]
medium_words = ["pyhton", "bottle", "monkey", "planet", "laptop"]
hard_words = ["elephant", "diamond", "umbrella", "computer", "mountain"]

print("Welcome to the password guessing game")
print("Choose a difficulty level: easy, medium or hard")

level = input("Enter difficulty: ").lower()
if level == "easy":
    secret = random.choice(easy_words)
elif level == "medium":
    secret = random.choice(medium_words)
elif level == "hard":
    secret = random.choice(hard_words)
else:
    print("Invalid choice.Defaulting to easy level")
    secret = random.choice(easy_words)

attempts = 0
print("\nGuess the secret password")

while True:
    guess = input("Enter your guess: ").lower()
    attempts += 1

    if guess == secret:
        print(f"congratulation! You guessed it in (attempts) attempts.")
        break
    hint = ""
    for i in range(len(secret)):
        if i< len(guess) and guess(i) == secret(i):
            hint += guess[i]
        else:
            hint += "_"
            print("Hint:", hint)
            print("Game over")
            







