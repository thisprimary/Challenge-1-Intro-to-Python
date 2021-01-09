# Challenge-1-Intro-to-Python

print("Choose a number from 1 to 100")

import random

range_1 = int(input("Choose your starting range: "))
range_2 = int(input("Choose your ending range: "))

random = random.randint(range_1,range_2)

print (random)

guess = int(input("Guess the number between your range: "))

if guess == random:
    print ('Correct')
else:
    print ("Incorrect")
