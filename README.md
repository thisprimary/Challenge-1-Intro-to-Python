# Challenge-1-Intro-to-Python
import random

range_1 = int(input("Choose your starting range: "))
range_2 = int(input("Choose your ending range: "))

if range_2 > range_1:
    print ("Please choose a number higher for range_2 than range_1")

random = random.randint(range_1,range_2)

print (random)


guess = int(input("Guess a number between your range: "))


while guess != random:
    if guess > random:
        print ('Incorrect. The number is lower')
        guess = int(input("Guess the number between your range: "))
    elif guess < random:
        print ('Incorrect. The number is higher')
        guess = int(input("Guess the number between your range: "))
    else:
        print ("Error. Only integers are allowed")
        guess = int(input("Guess the number between your range: "))
        
if guess == random:
    print ('Congratulations! You guessed the number')
