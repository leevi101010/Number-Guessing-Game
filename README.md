# Number-Guessing-Game
Simple Number Guessing Game in Python

import random

number = random.randint(1, 100)
guess = None

while guess != number:
    try:
        guess = int(input("Guess a number between 1 and 100: "))
    except ValueError:
        print("Please type an integer!")
        continue           # palaa silmukan alkuun

    if guess < number:
        print("Too low")
    elif guess > number:
        print("Too high")
    else:
        print("Correct! The number was", number)
