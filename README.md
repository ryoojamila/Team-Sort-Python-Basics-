#!/bin/python3 

#Import choice from random to allow us to picl a random item from a list.
from random import choice

#Add a file by clicking the + up to the right and name it players.txt
#Then add several names to the txt file, one name per line.

#Create an empty list to hold the players.
players = []

#We open the file, using 'r' to read out of it.
file = open('players.txt' , 'r')
#Fill our empty list by splitting our file's lines into separate names.
players = file.read().splitlines()
print('Players:' , players)

#Create an empty team list.
teamA = []


#loop through the player list until we have taken them all out.
while len(players) > 0:

    #Choose a random player for team A.
    playerA = choice(players)
    teamA.append(playerA)
    #Remove the player from the players list.
    players.remove(playerA)


#print the teams
print('\nHere are the teams:\n')
print("team A", teamA)

#Now go back through the program and add a Team B. That means:
#Add another empty team list.
#In your loop, select a player for team B after selecting for Team A.
#Finally, print out team B at the end.

#Add an if statement between choosing players to check if players == []
#Make the loop break if it is empty so we don't try picking from an empty list.
