# Challenge-1-Intro-to-Python
import random

range_1 = None
range_2 = None
guess = None
numCount = 0 

print ('Welcome to the Number Guessing Game!')

while type(range_1) is not int:
    range_1 = (input("Choose your starting range: "))
    if range_1.isdigit():
        range_1 = int(range_1)
    else:
        print ("Input is not valid, please enter an integer")
        
while type(range_2) is not int:       
    range_2 = (input("Choose your ending range: "))
    if range_2.isdigit():
        range_2 = int(range_2)
    else:
        print ("Input is not valid, please enter an integer")

while range_1 >= range_2: 
    print ("Ending range is too low.")
    range_2 = int(input("Choose a new ending range: "))
    
random = random.randint(range_1,range_2)

while type(guess) is not int:       
    guess = (input("Guess a number between your range: "))
    if guess.isdigit():
        guess = int(guess)
    else:
        print ("Input is not valid, please enter an integer")

while guess != random:
    if guess > random:
        print ('Incorrect. The number is lower')
        numCount = numCount + 1
        guess = input("Guess a number between your range: ")
        while type(guess) is not int:       
            if guess.isdigit():
                guess = int(guess)
            else:
                print ("Input is not valid, please enter an integer")
                guess = input("Guess a number between your range: ")

    elif guess < random:
        print ('Incorrect. The number is higher')
        numCount = numCount + 1
        guess = (input("Guess a number between your range: "))
        while type(guess) is not int:       
            if guess.isdigit():
                guess = int(guess)
            else:
                print ("Input is not valid, please enter an integer")
                guess = input("Guess a number between your range: ")

    else:
        print ("Error. Only integers are allowed")
        numCount = numCount + 1
        guess = (input("Guess a number between your range: "))
        while type(guess) is not int:       
            if guess.isdigit():
                guess = int(guess)
            else:
                print ("Input is not valid, please enter an integer")
                guess = input("Guess a number between your range: ")


if guess == random:
    numCount = numCount + 1
    print ('Congratulations! You guessed the number and it took you',numCount,'attempts')
    print ("Thanks for playing!")
