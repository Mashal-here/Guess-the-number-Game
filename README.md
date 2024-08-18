# Guess-the-number-Game
import random

# Generate a random number between 1 and 20
target = random.randint(1, 20)

# Set the number of chances
chances = 3

# Game loop, giving the user 3 chances
while chances > 0:
    # Prompt the user to guess the number
    user_choice = int(input("Guess the target number (between 1 and 20): "))

    # Check if the user's guess is correct
    if user_choice == target:
        print("The answer is right! You win!")
        break
    elif user_choice > target:
        print("The number is too big.")
    else:
        print("The number is too small.")

    # Decrement the number of chances
    chances -= 1

    # If no chances left, end the game
    if chances == 0:
        print("Game over! The correct number was:", target)
    else:
        print(f"You have {chances} chance(s) left.")
