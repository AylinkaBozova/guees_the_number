import random

RED = "\033[91m"
GREEN = "\033[92m"
YELLOW = "\033[93m"
CYAN = "\033[96m"
RESET = "\033[0m"

print(CYAN + "Welcome to the 'Guess the Number' game!" + RESET)
print(YELLOW + "The computer has chosen a number between 1 and 100. Try to guess it!" + RESET)

secret_number = random.randint(1, 100)
attempts = 0

while True:
    guess = input("Enter your guess: ")
    if not guess.isdigit():
        print(RED + "Please enter a valid number!" + RESET)
        continue
    guess = int(guess)
    attempts += 1
    if guess < secret_number:
        print(YELLOW + "Too low! Try something higher." + RESET)
    elif guess > secret_number:
        print(YELLOW + "Too high! Try something lower." + RESET)
    else:
        print(GREEN + f"Congratulations! You guessed {secret_number} in {attempts} attempts!" + RESET)
        break

