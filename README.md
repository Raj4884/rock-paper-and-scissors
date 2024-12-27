# rock-paper-and-scissors
import random

options = ("rock", "paper", "scissors") player = None

while True: computer = random.choice(options) while player not in options: player = input("rock, paper or scissors: ").lower()
print(f"player: {player}")
print(f"computer: {computer}")

if player == computer:
    print("It is a tie")
elif player == "rock":
    if computer == "scissors":
        print("You win")
    else:
        print("You lose")
elif player == "paper":
    if computer == "rock":
        print("You win")
    else:
        print("You lose")
elif player == "scissors":
    if computer == "paper":
        print("You win")
    else:
        print("You lose")

play_again = input("Play again? (yes/no): ").lower()
if play_again != "yes":
    break
player = None  # Reset player for the next round
