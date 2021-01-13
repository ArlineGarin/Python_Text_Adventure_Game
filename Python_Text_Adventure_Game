## Doc-String ##
"""

    A - Introduction: 
    It is finally here, the ultimate Harry Potter Experience! 
    This game consists in 3 stages. 
    Stage 1: Discover which House you belong to by answering 1 question, simple
    Stage 2: Coin toss in 3 rounds with your bunk-bed mate. The winner gets 
    the top bed. 
    Stage 3: Defence Against the Dark Arts class, where you will have to, 
    well, survive by succeeding a potion, one ingredient after the other. 
    
    
    B - Known Bugs and/or Errors:
    None
    
"""

## INTRODUCTION ##
from sys import exit
import time
import random
def game_start():
    
# Input user's name
    global user_name
    user_name = input(prompt = "Before the fun begins, state your name\t")
    user_name = user_name.capitalize()
    print("\n")
    stage_1()

## STAGE 1 ##
def stage_1():
# Put context to the game through storytelling
    print("\U0001F31F" * 40)

    print(f"""
The day has finally come: Your first day at Hogwarts School of Witchcraft and Wizardy.\n
Quick after your arrival, you are taken to the Great Hall with all of the first-year\v
students and here comes the moment of the Sorting Hat!

You see each student coming after another for the Sorting Hat to determine which one of\v
the four school Houses they belong to. \v
It is now your turn {user_name}, the Sorting Hat is placed on your head. Are you ready?
    """)

    print("\U0001F31F" * 40)
    
# Pausing the game for user experience
    input("\n<Press Enter to find out which House you belong to> \t")
    
# Introduction of stage 1    
    print(f"""
\U0001F3A9: Well hello there {user_name}! I have been expecting you. You seem stressed about\v 
discovering your House! But do not worry, I've never made one mistake in centuries!\v
All you have to do, is to answer 1 question truthfully.
    """)
    
# Pausing the game for user experience
    input("<Press Enter to release the question> \t")
    
    print("\n\U0001F3A9: What is the most important quality for you?\n") 
    time.sleep(.5)
    print("1 - Bravery\v")
    time.sleep(.5)
    print("2 - Loyalty\v")
    time.sleep(.5)
    print("3 - Wisdom\v")
    time.sleep(.5)
    print("4 - Persistence\v")
    time.sleep(.5)

# Set up house list
    house_list = ["Gryffindor", "Hufflepuff", "Ravenclaw", "Slytherin"]

# Set up input variable
    quality = input(prompt = "> \t")
    quality = quality.lower()

# While loop to output user's answer

    while True:
    
        if "1" in quality or "one" in quality or "bravery" in quality:
        
            global house
            house = house_list[0]
            print("\n\U0001F3A9: \U0001F534 " + house_list[0] + "! \U0001F7E1\n")
            stage_2()
            break
    
        elif "2" in quality or "two" in quality or "loyalty" in quality: 
        
            house = house_list[1]
            print("\n\U0001F3A9: \U0001F7E1 " + house_list[1] + "! \U0001F3F4\n")
            stage_2()
            break
    
        elif "3" in quality or "three" in quality or "wisdom" in quality: 
        
            house = house_list[2]
            print("\n\U0001F3A9: \U0001F535 " + house_list[2] + "! \U0001F7E4\n")
            stage_2()
            break
    
        elif "4" in quality or "four" in quality or "persistence" in quality: 
        
            house = house_list[3]
            print("\n\U0001F3A9: \U0001F7E2 " + house_list[3] + "! \U0001F3F3\n")
            stage_2()
            break
    
        else:
            print("\n\U0001F3A9: Sorry dear, I didn't understand this! Please give me a proper answer")
            quality = input(prompt = "> \v\v")
        
## STAGE 2 ##        
def stage_2():
    time.sleep(1)
    print(f"""
{user_name}, now you know. You belong to {house}! Excited or not, that is your destiny.\v
It's time for you to discover your new room.\n
    """)
    
    print("\U0001F31F" * 40)

# Pausing the game for user experience
    input("\n<Press Enter to teleport yourself to your common area> \t")

# If statement to determine name of friend based on the House from stage_1

# If Gryffindor, friend is Ron Weasley
    if 'Gryffindor' in house:
        global friend
        friend = 'Ron Weasley'
        
# If Hufflepuff, friend is Cedric Diggory       
    elif 'Hufflepuff' in house:
        friend = 'Cedric Diggory'
        
# If Ravenclaw, friend is Cho Chang        
    elif 'Ravenclaw' in house:
        friend = 'Cho Chang'
        
# If Slytherin, friend is Draco Malfoy       
    elif 'Slytherin' in house:
        friend = 'Draco Malfoy'
        
# Else statement to reduce risk for bugs       
    else:
        print('Something went wrong')

# Introduction of coin toss
    print(f"""
As you enter the common area of {house}, you go straight to the 1st-year bedroom\v 
and you meet {friend}, your new bunk-bed mate.\v
The issue here is you both want to sleep in the top-bed, so you both decide to rely\v
on faith by playing heads or tails.\n
    """)
    
# User's input heads or tails    
    user_coin = input(prompt = "Which one do you choose? Heads or tails?\t")
    user_coin = user_coin.lower()

# While loop to ensure user's input is understood and assign 1 variable for user experience
    while True:
        
# If user = head, then friend coin variable = tails
        if "heads" in user_coin:
            ron_coin = 'tails'
            break
            
        elif "tails" in user_coin: 
            ron_coin = 'heads'
            break

# Else statement to reduce risk for bugs  
        else:
            print("\nPlease, say again")
            user_coin = input(prompt = "Which one do you choose? Heads or tails?\t")

# Explaining coin toss rules - 3 rounds, the one who wins 2 out of 3 wins
    print(f"""
{friend}: Okay {user_name}. Guess I'm choosing {ron_coin}. We play it in 3 rounds, the one\v
who wins 2 out of the 3 wins.\n
    """)

# Declairing number of rounds and an empty list to hold results
    tours = 3
    bed_choice = []
    
# While loop to run the 3 rounds of coin toss 
    while tours > 0: 
        
# 1 is heads, else is tails - Generating random numbers 3 times
        coin_toss = random.randint(0, 1)
        coin = input("<Press Enter to play the round> \t")
        
        if (coin_toss == 1):
            print('\033[1m' + "\t\t\t\t Heads" + '\033[0m')
            bed_choice.append(0)
            tours -= 1
            
        else:
            print('\033[1m' + "\t\t\t\t Tails" + '\033[0m')
            bed_choice.append(1)
            tours -= 1

# Determine if user has won - Nested Conditionals 
    if "heads" in user_coin:
        if (bed_choice[0]+bed_choice[1]+bed_choice[2]) > 1:
            print(f"""
{friend}: Haaaaaaha! I beat you, {user_name}! We can switch next semester ... Or not!            
            """)
            
        else: 
             print(f"""
{friend}: WHAT?! You are lucky {user_name}... You can have the top-bed.
            """)
            
    elif "tails" in user_coin:
        if (bed_choice[0]+bed_choice[1]+bed_choice[2]) > 1:
            print(f"""
{friend}: WHAT?! You are lucky {user_name}... You can have the top-bed.
            """)
            
        else:
            print(f"""
{friend}: Haaaaaaha! I beat you, {user_name}! We can switch next semester ... Or not!           
            """)

# Else statement to reduce risk for bugs 
    else: 
        print("Something went wrong.")
        
    stage_3()        

## STAGE 3 ##
def stage_3():
    time.sleep(1)
    print(f"""
{friend}: Come on {user_name}, we have our first class of Defense Against the Dark Arts with\v
Professor Snape and I really don't want to be late!\v
Follow me, I know a quicker way.
    """)
    
    print("\U0001F31F" * 40)

# Pausing game for user experience
    input(f"\n<Press Enter and follow {friend} to class.> \t")

# Introduction of stage 3
    print(f"""
Professor Snape: Hello young humans ... You are very far from being called a wizard yet.\v
Oh! Have you all noticed the privilege we have for {user_name} to be one of us? ...\v
You may be already famous {user_name} in this world, but to me you are no one.\n
However, I want to see what you can do. \v
So let's make the very defensive INVISIBILITY POTION!\n
Make sure to add the ingredients in the right order... \v
\t\t\t\t\t\t\tOtherwise...\v 
\t\t\t\t\t\t\t\t\tYou don't want to know.\n
{friend}: Ok I know the first ingredient is unicorn horn. I know the other two are\v 
juice and cherry but I don't know the right order ... so ... you do it! 
    """)

# Declaring list of potion ingredients for the right order
    potion = ['unicorn horn', 'cherry', 'juice']
    print("Which ingredient do you choose to put first?\n")
    
# User's input to choose the first ingredient 
    ingredient_1 = input(prompt = "\nJuice or cherry?\t")
    ingredient_1 = ingredient_1.lower()
    
# While loop to ensure user's input is understood and assign 1 variable for user experience
    while True:
    
# If statement to determine 2nd ingredient based on the first one
        if "juice" in ingredient_1:
            print(f"\n{friend}: Okay so " + potion[1] + " goes second")
        
# If user does not find the right order, he fails
            time.sleep(1)
            print("...")
            time.sleep(1)
            fail()

# If user finds the right order, he/she wins
        elif "cherry" in ingredient_1:
            ingredient_2 = 'Juice'
            print(f"\n{friend}: Okay so " + potion[2] + " goes second")
            time.sleep(1)
            print("...")
            time.sleep(1)
            win()
        
# Else statement to reduce risk for bugs 
        else:
            print("Please restate your first ingredient.\n")
            ingredient_1 = input(prompt = "Juice or cherry?\t")

## WIN ##
# The user has won the game, the game stops
def win():
    print("\n\U0001F44F\n")
    print(f"""
You're safe {user_name}
CONGRATULATIONS! You made it through your first day of class!
Hope you enjoy the game! \U0001F44B\n
    """)
    print("\U0001F31F" * 40)
    exit(0)

## FAIL ##
def fail():
    print("\n\U0001F480\n")
    print(f"""
Oh no {user_name}...! You mixed up the ingredients and did not survive the explosion..\v
And in case you're wondering, {friend} did not survive either...\n
    """)
    
# Ask for user's input to replay the game
    print(f"{user_name}, do you want to restart the story? (yes or no)")
    replay = input("> \t")
    replay = replay.lower()

# If statement, user's answer yes so game go back to stage_1
    if replay == 'yes':
        print("\n")
        stage_1()

# If statement, user's answer no so game stops. 
    elif replay == 'no':
        print(f"\nHope you enjoy the game! Thanks for playing {user_name}!\n")
        print("\U0001F31F" * 40)
        exit(0)
        
# Else statement to reduce risk for bugs 
    else: 
        print(f"\n I'm sorry, can you repeat this?")
        print(f"{user_name}, do you want to restart the story? (yes or no)")
        replay = input("> \t")

## GAME START ##
game_start()
