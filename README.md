dicegamepython
==============
import random

print ("Welcome to my Python Dice Game!")

print ("Ready to start? Hit Enter to start rolling the dice or CTRL +C to quit")

input()


def rollDice():
 die1 = random.random()*6 + 1
 die2 = random.random()*6 + 1
 if die1 == 1 or die2 == 1:
  score = 0
 else:

  if die1 == die2:
    score = die1 + die2 * 2
    print ("Doubles!")
  else:
    score = die1 + die2
	
 print ("You have rolled %d and %d" % (die1, die2))
 print ("You scored %d" % score)


rollDice()
while True:
  tryAgain = input("Try again? [y/n]")
  if tryAgain == "y":
    rollDice()
    tryAgain
  else:
    False
    print ("Thank you for playing!")
    break
