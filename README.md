import random

print("🎲 Welcome to the 'Guess the Number' game!")
print("The computer has chosen a number between 1 and 100. Try to guess it!")

secret_number = random.randint(1, 100)
attempts = 0

while True:
    guess = input("Enter your guess: ")
    if not guess.isdigit():
        print(" Please enter a valid number!")
        continue
    guess = int(guess)
    attempts += 1
    if guess < secret_number:
        print(" The number is higher!")
    elif guess > secret_number:
        print(" The number is lower!")
    else:
        print(f" Congratulations! You guessed {secret_number} in {attempts} attempts!")
        break
