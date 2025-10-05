''' Rock, Paper and Scissor Game (Python)
      Chaitanya Mangla '''

''' Rules of the game:
    1. Rock breaks scissor (rock > scissor)
    2. Scissor cuts paper (scissor > paper)
    3. Paper folds rock  (paper > rock)
    '''


'''1 for rock
   -1 for paper
    0 for scissor
    '''
import random # Import random library to allow computer operating system for making choices

computer =  random.choice([-1,0,1])
youstr = input ("Enter your choice ")
youDict = {"r": 1, "p" : -1, "s" : 0}
reverseDict = {1: "Rock", -1: "Paper" , 0: "Scissor"}
you = youDict[youstr]

# Here, we have 2 number variables, you and computer 

print(f"You chose {reverseDict[you]}\nComputer chose {reverseDict[computer]}")

if (computer == you):
    print("Its a tie")

else:  # This is a perfect example of nested if else statement 
    if(computer == -1 and you == 0):
        print("You Win\nCongratulations!!")
    
    elif(computer == -1 and you == 1):
        print("You Lose\nBetter Luck next time!!")
    
    elif(computer == 1 and you == -1):
        print("You Win\nCongratulations!!")
    
    elif(computer == 1 and you == 0):
        print("You Lose\nBetter Luck next time!!")
    
    elif(computer == 0 and you == 1):
        print("You Win\nCongratulations!!")
    
    elif(computer == 0 and you == -1):
        print("You Lose\nBetter Luck next time!!")

    else:
        print("Something went wrong")


