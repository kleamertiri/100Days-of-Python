# #100DaysOfCode🐍
In this repository, I will show the different Python exercises I will be doing on the 100 Days of Code.

## Two main rules:
1- Code minimum an hour every day for the next 100 days.

2- Show your progress every day on social media.

### :arrow_forward:`Day 1` - Working with Variables in Python to Manage Data
#### :arrow_right: Exercise 1
Write a program that prints the notes using what you have learnt about the Python print function.
```python
#Write your code below this line 👇
print("Day 1 - Python Print Function \nThe function is declared like this: \nprint('what to print')")
```
#### :arrow_right: Exercise 2
Write a program that prints the number of characters in a user's name.

```python
#Write your code below this line 👇
userName = input("What is your name? ")
print(len(userName))
```
#### :arrow_right: Exercise 3
Write a program that switches the values stored in the variables a and b.

```python
a = input("a: ")
b = input("b: ")
c = ""
c = a 
a = b 
b = c
print("a: " + a)
print("b: " + b)
```
Input:

a: 3

b: 5

Output:

a: 5

b: 3

#### :dart: Project: Band Name Generator

```python
#1. Create a greeting for your program.
print("Welcome to the Band Name Generator.")

#2. Ask the user for the city that they grew up in.
userName = input("What's the name of the city you grew up in?\n" )

#3. Ask the user for the name of a pet.
petName = input("What's your pet's name?\n")

#4. Combine the name of their city and pet and show them their band name.
print("Your band name could be " + userName + " " + petName)
```

### :arrow_forward:`Day 2` - Understanding Data types and how to manipulate strings

#### :arrow_right: Exercise 1
Write a program that adds the digits in a 2 digit number. e.g. if the input was 35, then the output should be 3 + 5 = 8

```python
two_digit_number = (input("Type a two digit number: "))
print(int(two_digit_number[0]) + int(two_digit_number[1]))
```

#### :arrow_right: Exercise 2
Write a program that calculates the Body Mass Index (BMI) from a user's weight and height.

```python
height = input("enter your height in m: ")
weight = input("enter your weight in kg: ")
bmi = float(weight) / float(height) ** 2
print(int(bmi))
```

#### :arrow_right: Exercise 3
Create a program using maths and f-Strings that tells us how many days, weeks, months we have left if we live until 90 years old.

***Hint:*** There are 365 days in a year, 52 weeks in a year and 12 months in a year.

```python
age = input("What is your current age? ")

#Calculating the remaining years
remainYears = 90 - int(age)

#Calculating the remaining weeks, days and months
days = remainYears * 365
weeks = remainYears * 52
months = remainYears * 12

print(f"You have {days} days, {weeks} weeks, and {months} months left.")
```
#### :dart: Project: Tip Calculator

```python
print("Welcome to the tip calculator!")
bill = input("What was the total bill? $")
tipPerc = input("How much tip would you like to give? 10, 12, 15? ")
nrPeople = input("How many people to split the bill?")

#Calculate the share
share = (int(bill) * float(tipPerc) / 100 + int(bill)) / int(nrPeople)
print("Each person should pay: $" + str(round(share,2)))
```

### :arrow_forward:`Day 3` - Control Flow and Logical Operators

#### :arrow_right: Exercise 1
Write a program that works out whether if a given number is an odd or even number.
```python
number = int(input("Which number do you want to check? ")

if number % 2 == 0:
    print("This is an even number.")
else:
    print("This is an odd number.")    
```    

#### :arrow_right: Exercise 2
Write a program that interprets the Body Mass Index (BMI) based on a user's weight and height.

It should tell them the interpretation of their BMI based on the BMI value.
- Under 18.5 they are underweight
- Over 18.5 but below 25 they have a normal weight
- Over 25 but below 30 they are slightly overweight
- Over 30 but below 35 they are obese
- Above 35 they are clinically obese.

```python
height = float(input("enter your height in m: "))
weight = float(input("enter your weight in kg: "))

dec_bmi = weight / height ** 2
bmi = round(dec_bmi)

if dec_bmi < 18.5:
    print(f"Your BMI is {bmi}, you are underweight.")
elif dec_bmi > 18.5 and dec_bmi < 25:
    print(f"Your BMI is {bmi}, you have a normal weight.")
elif dec_bmi > 25 and dec_bmi < 30:
    print(f"Your BMI is {bmi}, you are slightly overweight.")
elif dec_bmi > 30 and dec_bmi < 35:
    print(f"Your BMI is {bmi}, you are obese.")
else:
    print(f"Your BMI is {bmi}, you are clinically obese.")
```    
    
#### :arrow_right: Exercise 3
Write a program that works out whether if a given year is a leap year.

This is how you work out whether if a particular year is a leap year:
- on every year that is evenly divisible by 4
- **except** every year that is evenly divisible by 100 
- **unless** the year is also evenly divisible by 400

![image](https://github.com/kleamertiri/100Days-of-Python/assets/105167291/7ec6d1e5-6829-46aa-9a95-f7e9e933f9ef)

```python
year = int(input("Which year do you want to check? "))

if year % 4 == 0:
    if year % 100 == 0:
        if year % 400 == 0:
            print("Leap year.")
        else:
            print("Not leap year.")
    else:
        print("Leap year.")
else:
    print("Not leap year.")
```    

#### :arrow_right: Exercise 4
Congratulations, you've got a job at Python Pizza. Your first job is to build an automatic pizza order program.

Based on a user's order, work out their final bill.

Small Pizza: $15

Medium Pizza: $20

Large Pizza: $25

Pepperoni for Small Pizza: +$2

Pepperoni for Medium or Large Pizza: +$3

Extra cheese for any size pizza: + $1

```python
print("Welcome to Python Pizza Deliveries!")
size = input("What size pizza do you want? S, M, or L ")
add_pepperoni = input("Do you want pepperoni? Y or N ")
extra_cheese = input("Do you want extra cheese? Y or N ")

price = 0
if size == "S":
    price = 15
    if add_pepperoni == "Y":
        price += 2
    if extra_cheese == "Y":
        price += 1
    else:
        price
elif size == "M":
    price = 20
    if add_pepperoni == "Y":
        price += 3
    if extra_cheese == "Y":
        price += 1
    else:
        price
elif size == "L":
    price = 25
    if add_pepperoni == "Y":
        price += 3
    if extra_cheese == "Y":
        price += 1
    else:
        price

print(f"Your final bill is: ${price}.")
```
 
#### :arrow_right: Exercise 5
You are going to write a program that tests the compatibility between two people.

To work out the love score between two people:

Take both people's names and check for the number of times the letters in the word TRUE occurs. 

Then check for the number of times the letters in the word LOVE occurs. 

Then combine these numbers to make a 2 digit number.

```python
print("Welcome to the Love Calculator!")
name1 = input("What is your name? \n")
name2 = input("What is their name? \n")

name = (name1 + name2).lower()
#TRUE
nrT = name.count("t")
nrR = name.count("r")
nrU = name.count("u")
nrE = name.count("e")
nrTrue = nrT + nrR + nrU + nrE

#LOVE
nrL = name.count("l")
nrO = name.count("o")
nrV = name.count("v")
nrLove = nrL + nrO + nrV + nrE

str_totalNr = str(nrTrue) + str(nrLove)
int_totalNr = int(str_totalNr)

#Find the compatibility
if int_totalNr > 40 and int_totalNr < 50:
    print(f"Your score is {str_totalNr}, you are alright together.")
elif int_totalNr <= 10 or int_totalNr >= 90:
    print(f"Your score is {str_totalNr}, you go together like coke and mentos.")
else:
    print(f"Your score is {str_totalNr}")
```    

#### :dart: Project: Treasure Island:old_key:
![image](https://github.com/kleamertiri/100Days-of-Python/assets/105167291/b9924570-7214-468f-812c-3b20e21c7b11)

```python
print('''
*******************************************************************************
          |                   |                  |                     |
 _________|________________.=""_;=.______________|_____________________|_______
|                   |  ,-"_,=""     `"=.|                  |
|___________________|__"=._o`"-._        `"=.______________|___________________
          |                `"=._o`"=._      _`"=._                     |
 _________|_____________________:=._o "=._."_.-="'"=.__________________|_______
|                   |    __.--" , ; `"=._o." ,-"""-._ ".   |
|___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________
          |           |o`"=._` , "` `; .". ,  "-._"-._; ;              |
 _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______
|                   | |o;    `"-.o`"=._``  '` " ,__.--o;   |
|___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________
____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____
/______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_
____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____
/______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_
____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____
/______/______/______/______/______/______/______/______/______/______/_____ /
*******************************************************************************
''')
print("Welcome to Treasure Island.")
print("Your mission is to find the treasure.") 

#Game Logic
left_right = input('You\'re at a cross road. Where do you want to go? Type "left" or "right" \n').lower()
if left_right == "left":
  swim_wait = input('You\'ve come to a lake. There is an island in the middle of the lake. Type "wait" to wait for a boat. Type "swim" to swim across.\n').lower()
  if swim_wait == "wait":
    door = input('You arrive at the island unharmed. There is a house with 3 doors. One red, one yellow and one blue. Which colour do you choose?\n').lower()
    if door == "red":
      print("You get burned by fire. Game Over.")
    elif door == "yellow":
      print("You win!")
    elif door == "blue":
      print("You get eaten by beasts. Game Over.")
    else:
      print("Game Over")
  else:
    print("You get attacked by trout. Game over.")
```    

### :arrow_forward:`Day 4` - Randomisation and Python Lists

#### :arrow_right: Exercise 1
You are going to write a virtual coin toss program. It will randomly tell the user "Heads" or "Tails".

```python
import random

randomInt = random.randint(0,1)
if randomInt == 1:
    print("Heads")
else:
    print("Tails")
```

#### :arrow_right: Exercise 2
You are going to write a program that will select a random name from a list of names. The person selected will have to pay for everybody's food bill.

**Hint:** You might need the help of the `len()` function.

```python
import random
# Split string method
names_string = input("Give me everybody's names, separated by a comma. ")
names = names_string.split(", ")

size = len(names)
random_name = names[random.randint(0, size - 1)]
print(f"{random_name} is going to buy the meal today!")
```

#### :arrow_right: Exercise 3
You are going to write a program that will mark a spot with an X  in the map, based on the user input.

Map:

['⬜️', '⬜️', '⬜️']

['⬜️', '⬜️', '⬜️']

['⬜️', '⬜️', '⬜️']

```python
row1 = ["⬜️","️⬜️","️⬜️"]
row2 = ["⬜️","⬜️","️⬜️"]
row3 = ["⬜️️","⬜️️","⬜️️"]
map = [row1, row2, row3]
print(f"{row1}\n{row2}\n{row3}")
position = input("Where do you want to put the treasure? ")

horizontal = int(position[0])
vertical = int(position[1])
map[vertical -1][horizontal - 1] = "X"

print(f"{row1}\n{row2}\n{row3}")
```

#### :dart:  Project: Rock Paper Scissors

```python
import random
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors. "))
comp_choice = random.randint(0,2)

#User
if user_choice == 0:
  print("Rock:\n" + rock)
elif user_choice == 1:
  print("Paper:\n" + paper)
else:
  print("Scissors:\n" + scissors)

#Computer   
if comp_choice == 0:
  print("Rock:\n" + rock)
elif comp_choice == "1":
  print("Paper:\n" + paper)
else:
  print("Scissors:\n" + scissors)
  
#Game Logic 
if (user_choice == 0 and comp_choice == 2) or (user_choice == 1 and comp_choice == 0) or (user_choice == 2 and comp_choice == 1):
  print("You win!")
elif user_choice == comp_choice:
  print("It's a tie!")
else:
  print("You lose!")
```
**OR**

```python
import random
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

#List of images
image_list = [rock, paper, scissors]
#User
user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors. "))
if user_choice >= 3 or user_choice < 0:
  print("Invalid input. Game Over!")
else:
  print("Your Choice:\n" + image_list[user_choice])

#Computer    
comp_choice = random.randint(0,2)
print("Computer choice:\n" + image_list[comp_choice])

#Game Logic
if user_choice == 0 and comp_choice == 2:
  print("You win!")
elif user_choice == 2 and comp_choice == 0:
  print("You lose!")
elif user_choice > comp_choice:
  print("You win!")
elif user_choice == comp_choice:
  print("It's a tie!")
else:
  print("You lose!")
```

### :arrow_forward:`Day 5` - Python Loops

#### :arrow_right: Exercise 1
You are going to write a program that calculates the average student height from a List of heights.

**Important:** You should not use the `sum()` or `len()` functions in your answer. You should try to replicate their functionality using loops.
```python
student_heights = input("Input a list of student heights ").split()
for n in range(0, len(student_heights)):
  student_heights[n] = int(student_heights[n])

sumHeight = 0 
counter = 0
for height in student_heights:
    sumHeight += height
    counter += 1

averageHeight = round(sumHeight / counter)
print(averageHeight)
```

#### :arrow_right: Exercise 2
You are going to write a program that calculates the highest score from a List of scores.

**Important:** You are not allowed to use the max or min functions. The output words must match the example.

```python
student_scores = input("Input a list of student scores ").split()
for n in range(0, len(student_scores)):
  student_scores[n] = int(student_scores[n])

max_score = 0
for score in student_scores:
    if score > max_score:
        max_score = score
    
print(max_score)
```

#### :arrow_right: Exercise 3
You are going to write a program that calculates the sum of all the even numbers from 1 to 100.

**Important:** There should only be 1 print statement in your console output. It should just print the final total and not every step of the calculation.

```python
sum = 0
for n in range(1, 101):
    if n % 2 == 0:
        sum += n

print(sum)
```

#### :arrow_right: Exercise 4
You are going to write a program that automatically prints the solution to the FizzBuzz game.

- Your program should print each number from 1 to 100 in turn.
- When the number is divisible by 3 then instead of printing the number it should print `"Fizz"`.
- When the number is divisible by 5, then instead of printing the number it should print `"Buzz"`.
- And if the number is divisible by both 3 and 5 e.g. 15 then instead of the number it should print `"FizzBuzz"`.

```python
for n in range(1, 101):
    if n % 5 == 0 and n % 3 == 0:
        print("FizzBuzz")
    elif n % 3 == 0:
        print("Fizz")
    elif n % 5 == 0:
        print("Buzz")
    else:
        print(n)
```

#### :dart:  Project: Create e Password Generator

```python
#Password Generator Project
import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 
't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 
'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters= int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

#Order not randomised:
#e.g. 4 letter, 2 symbol, 2 number = JduE&!91

lettersPass = random.sample(letters, nr_letters)
symbolsPass = random.sample(symbols, nr_symbols)
numberPass = random.sample(numbers, nr_numbers)

#Order not randomised:
#e.g. 4 letter, 2 symbol, 2 number = JduE&!91
print("Here is your password: " + "".join(lettersPass) + "".join(symbolsPass) + "".join(numberPass))

#Order of characters randomised:
#e.g. 4 letter, 2 symbol, 2 number = g^2jk8&P

list1 = [lettersPass, symbolsPass, numberPass]
flat_list = []
for nestList  in list1:
  for item in nestList:
    flat_list.append(item)

shuffle_list = random.sample(flat_list, len(flat_list))
print("Here is your randomised password: " + "".join(shuffle_list))
```

### :arrow_forward:`Day 6` - Python Functions & Karel

#### :arrow_right: Exercise 1 - The Hurdles Loop

![image](https://github.com/kleamertiri/100Days-of-Python/assets/105167291/55ca3a59-5ba9-473f-a798-178ca309e36d)


```python
def turn_right():
    turn_left()
    turn_left()
    turn_left()
def jump():
    move()
    turn_left()
    move()
    turn_right()
    move()
    turn_right()
    move()
    turn_left()

for step in range(6):
    jump()
```

### :arrow_forward:`Day 7` - [Hangman](https://replit.com/@kleamertiri/Hangman?v=1)

`hangman_art.py`
```python
stages = ['''
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========''', '''
  +---+
  |   |
  O   |
  |   |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
      |
      |
      |
=========
''', '''
  +---+
  |   |
      |
      |
      |
      |
=========
''']

logo = ''' 
 _                                             
| |                                            
| |__   __ _ _ __   __ _ _ __ ___   __ _ _ __  
| '_ \ / _` | '_ \ / _` | '_ ` _ \ / _` | '_ \ 
| | | | (_| | | | | (_| | | | | | | (_| | | | |
|_| |_|\__,_|_| |_|\__, |_| |_| |_|\__,_|_| |_|
                    __/ |                      
                   |___/    '''

 ```
 
 `hangman_words.py`
 ```python
 word_list = ['abruptly', 'absurd', 'abyss', 'affix', 'askew','avenue','awkward','axiom','azure','bagpipes','bandwagon','banjo',
 'bayou','beekeeper','bikini','blitz','blizzard','boggle','bookworm','boxcar','boxful','buckaroo', 'buffalo', 'buffoon', 'buxom','buzzard','buzzing','buzzwords','caliph','cobweb','cockiness','croquet','crypt','curacao','cycle',
 'daiquiri','dirndl','disavow','dizzying','duplex','dwarves','embezzle','equip','espionage','euouae','exodus',
 'faking','fishhook', 'fixable','fjord', 'flapjack','flopping', 'fluffiness', 'flyby', 'foxglove', 'frazzled', 
 'frizzled', 'fuchsia', 'funny', 'gabby', 'galaxy', 'galvanize', 'gazebo', 'giaour', 'gizmo']
 ```
 
```python
import random
import hangman_words
import hangman_art
chosen_word = random.choice(hangman_words.word_list)
word_length = len(chosen_word)
end_of_game = False
lives = 6

#Print the Hangman logo
print(hangman_art.logo)

#Create blanks
display = []
for _ in range(word_length):
    display += "_"

while not end_of_game:
    guess = input("Guess a letter: ").lower()

    #If the user has entered a letter they've already guessed, print the letter and let them know.
    if guess in display:
      print(f"You already guessed the letter {guess}. Guess another letter")
      
    #Check guessed letter
    for position in range(word_length):
        letter = chosen_word[position]
        #Replacing the _ with the actual letter
        if letter == guess:
            display[position] = letter

    #Check if the letter is not part of the word
    if guess not in chosen_word:
        print(f"This letter {guess} is not in the word")
        lives -= 1
        if lives == 0:
            end_of_game = True
            print(f"You lose. The word is {chosen_word}.")

    #Join all the elements in the list and turn it into a String.
    print(f"{' '.join(display)}")

    #Check if user has got all letters.
    if "_" not in display:
        end_of_game = True
        print(f"You win. The word is {chosen_word}.")

    # Import the stages from hangman_art.py and make this error go away.
    print(hangman_art.stages[lives])
    
```
 
### :arrow_forward:`Day 8` - Function Parameters & Caesar Cipher

#### :arrow_right: Exercise 1

You are painting a wall. The instructions on the paint can says that 1 can of paint can cover 5 square meters of wall. Given a random height and width of wall, calculate how many cans of paint you'll need to buy.

number of cans = (wall height x wall width) ÷ coverage per can.

```python
def paint_calc(height, width, cover):
    print(height * width / cover)  

test_h = int(input("Height of wall: "))
test_w = int(input("Width of wall: "))
coverage = 5
paint_calc(height=test_h, width=test_w, cover=coverage)
```

#### :arrow_right: Exercise 2

You need to write a function that checks whether if the number passed into it is a prime number or not.

```python
def prime_checker(number):
    check = False
    if number == 1:
        print("It's not a prime number")
    elif number > 1:
        for i  in range(2, number):
            if number % i == 0:
                check = True
        if check:
            print("It's not a prime number")
        else:
            print("It's a prime number")

n = int(input("Check this number: "))
prime_checker(number=n)
```

#### :dart: Project: [Caesar Cipher](https://replit.com/@kleamertiri/Caesar-Cipher?v=1)

`art.py`
```python
logo = """           
 ,adPPYba, ,adPPYYba,  ,adPPYba, ,adPPYba, ,adPPYYba, 8b,dPPYba,  
a8"     "" ""     `Y8 a8P_____88 I8[    "" ""     `Y8 88P'   "Y8  
8b         ,adPPPPP88 8PP"""""""  `"Y8ba,  ,adPPPPP88 88          
"8a,   ,aa 88,    ,88 "8b,   ,aa aa    ]8I 88,    ,88 88          
 `"Ybbd8"' `"8bbdP"Y8  `"Ybbd8"' `"YbbdP"' `"8bbdP"Y8 88   
            88             88                                 
           ""             88                                 
                          88                                 
 ,adPPYba, 88 8b,dPPYba,  88,dPPYba,   ,adPPYba, 8b,dPPYba,  
a8"     "" 88 88P'    "8a 88P'    "8a a8P_____88 88P'   "Y8  
8b         88 88       d8 88       88 8PP""""""" 88          
"8a,   ,aa 88 88b,   ,a8" 88       88 "8b,   ,aa 88          
 `"Ybbd8"' 88 88`YbbdP"'  88       88  `"Ybbd8"' 88          
              88                                             
              88           
"""
```

`main.py`
```python
import art
alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 
'w', 'x', 'y', 'z', 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 
'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']
print(art.logo)
run_again = False

def caesar(plain_text, shiftNr, enc_dec):
  encry_decry_list = []
  #Bug Fix: When the shift number is bigger then the list
  if shiftNr >= len(alphabet):
    shiftNr = shiftNr % len(alphabet)
  
  for letter in plain_text:
    if letter in alphabet:
      index = alphabet.index(letter)
      if enc_dec == "encode" :
        encry_decry_list += alphabet[index + shiftNr]
      else:
        encry_decry_list += alphabet[index - shiftNr]
    else:  
      encry_decry_list += letter
      
  if enc_dec == "encode":
    print("Here's the encoded result: "+ "".join(encry_decry_list))
  else:
    print("Here's the decoded result:"+ "".join(encry_decry_list))

while not run_again:
  direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n").lower()
  text = list(input("Type your message:\n").lower())
  shift = int(input("Type the shift number:\n"))
  caesar(plain_text = text, shiftNr = shift, enc_dec = direction)
  yes_no = input("Type 'yes' if you want to go again. Otherwise type 'no'.\n").lower()
  if yes_no == "no":
    print("Goodbye")
    run_again = True
  ```

### :arrow_forward:`Day 9` - Dictionaries, Nesting and the Secret Auction

#### :arrow_right: Exercise 1

You have access to a database of `student_scores` in the format of a dictionary. The **keys** in `student_scores` are the **names** of the students and the **values** are their exam **scores**.

Write a program that **converts their scores to grades**. By the end of your program, you should have a new dictionary called `student_grades` that should contain student **names** for **keys** and their **grades** for **values**. The **final version** of the `student_grades` dictionary will be checked.

This is the scoring criteria:

Scores 91 - 100: Grade = "Outstanding"

Scores 81 - 90: Grade = "Exceeds Expectations"

Scores 71 - 80: Grade = "Acceptable"

Scores 70 or lower: Grade = "Fail"

```python
student_scores = {
  "Harry": 81,
  "Ron": 78,
  "Hermione": 99, 
  "Draco": 74,
  "Neville": 62,
}

student_grades ={}
for key in student_scores:
    if student_scores[key] > 90:
        student_grades[key] = "Outstanding"
    elif student_scores[key] in [81,90]:
        student_grades[key] = "Exceeds Expectations"
    elif student_scores[key] >= 71 and student_scores[key] <= 81:
        student_grades[key] = "Acceptable"
    elif student_scores[key] <= 70 :
        student_grades[key] = "Fail"
    
print(student_grades)
```

#### :arrow_right: Exercise 2
You are going to write a program that adds to a `travel_log`. You can see a travel_log which is a **List** that contains 2 **Dictionaries**.

Write a function that will work with the following line of code on line 21 to add the entry for Russia to the `travel_log`.

```python
travel_log = [
{
  "country": "France",
  "visits": 12,
  "cities": ["Paris", "Lille", "Dijon"]
},
{
  "country": "Germany",
  "visits": 5,
  "cities": ["Berlin", "Hamburg", "Stuttgart"]
},
]

def add_new_country(country, visits_nr, cities_names):
  new_country = {}
  new_country["country"] = country
  new_country["visits"] = visits_nr
  new_country["cities"] = cities_names 
  travel_log.append(new_country) 

add_new_country("Russia", 2, ["Moscow", "Saint Petersburg"])
print(travel_log)
```

#### :dart: Project: [Blind Auction](https://replit.com/@kleamertiri/Blind-Auction?v=1)
![image](https://github.com/kleamertiri/100Days-of-Python/assets/105167291/61ac0d8c-63c7-474c-ae94-04cfee72f8d8)


`art.py`

```python
logo = '''
                         ___________
                         \         /
                          )_______(
                          |"""""""|_.-._,.---------.,_.-._
                          |       | | |               | | ''-.
                          |       |_| |_             _| |_..-'
                          |_______| '-' `'---------'` '-'
                          )"""""""(
                         /_________\\
                       .-------------.
                      /_______________\\
'''
```



`main.py`

```python
from replit import clear
from art import logo
#HINT: You can call clear() to clear the output in the console.
print(logo)
continue_bid = True
auction_dict = {}

def highest_bidding(bidding_dict):
  high_bid = 0
  winner=""
  for bidder in bidding_dict:
    bid_amount = bidding_dict[bidder]
    if bid_amount > high_bid:
      high_bid = bid_amount
      winner = bidder
  print(f"The winner is {winner} with a bid of ${high_bid}")
      

while continue_bid:
  bid_name = input("What is your name?: ")
  bid_sum = int(input("What is your bid?: $"))
  auction_dict[bid_name] = bid_sum
  yes_no = input("Are there any other bidders? Type 'yes' or 'no'. ").lower()

  if yes_no == 'no':
    continue_bid = False
    highest_bidding(auction_dict) 
  elif yes_no == 'yes':
    clear()
```

### :arrow_forward:`Day 10` - Functions with Outputs

#### :arrow_right: Exercise 1

You are then going to create a function called `days_in_month()` which will take a year and a month as inputs, and it will use 
this information to work out the **number of days in the month**, then return that as the **output**.

```python
def is_leap(year):
  if year % 4 == 0:
    if year % 100 == 0:
      if year % 400 == 0:
        return True
      else:
        return False
    else:
      return True
  else:
    return False

def days_in_month(user_year, user_month):
  month_days = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]  
  if is_leap(user_year) and user_month == 2:
      return 29
  else:
      return month_days[user_month - 1]
  
year = int(input("Enter a year: "))
month = int(input("Enter a month: "))
days = days_in_month(year, month)
print(days)
```

#### :dart: Project: [Calculator](https://replit.com/@kleamertiri/Calculator?v=1)

```python
from replit import clear
from art import logo

#Add
def add(n1, n2):
    return n1 + n2


#Substract
def substract(n1, n2):
    return n1 - n2


#Divide
def divide(n1, n2):
    return n1 / n2


#Multiply
def multiply(n1, n2):
    return n1 * n2


#Dictionary where keys = operation's symbols, values = functions
calc_operations = {
  "+": add, 
  "-": substract, 
  "/": divide, 
  "*": multiply
}
                  

continue_calculation = True
restart_calculation = True

while restart_calculation:
  print(logo)
  num1 = int(input("What's the first number?: "))
  for symbol in calc_operations:
    print(symbol)
  restart_calculation = False
  while continue_calculation:
    operation_symbol = input("Pick an operation: ")
    num2 = int(input("What's the next number?: "))
  
    calculation = calc_operations[operation_symbol]
    answer = calculation(num1, num2)
  
    print(f"{num1} {operation_symbol} {num2} = {answer}")
    yes_no = input(f"Type 'y' to continue calculating with {answer}, or type 'n' to start a new calculation: ")

    if yes_no == 'y':
      num1 = answer
    elif yes_no == 'n':
      clear()
      continue_calculation = False
  restart_calculation = True
  continue_calculation = True
```

### :arrow_forward:`Day 11` - The Blackjack Capstone Project 
[ View the project :black_joker:](https://replit.com/@kleamertiri/The-Blackjack-Capstone?v=1) 

```python
#The Blackjack Capstone 🃏
import random
from replit import clear
from art import logo


#Function to get random cards
def deal_card():
  """Returns a random card from the deck"""
  cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
  card = random.choice(cards)
  return card

#Function to calculate the sum
def calculate_score(list_of_cards):
  """Take a list of cards and calculate the sum of them."""
  #Check for blackjack (ace + 10)
  if sum(list_of_cards) == 21 and len(list_of_cards) == 2:
    return 0
  
  #Check for an ace(11). If the score is > 21, replace 11 with 1 
  if 11 in list_of_cards and sum(list_of_cards) > 21:
    list_of_cards.remove(11)
    list_of_cards.append(1)
  
  return sum(list_of_cards)  

#Function to compare the scores
def compare(user_score, computer_score):
  if user_score == computer_score:
    return "Draw!"
  elif computer_score == 0:
    return "Lose, the opponent has Blackjack"
  elif user_score == 0:
    return "Win with a blackjack"
  elif user_score > 21:
    return "You went over. You lose"
  elif computer_score > 21:
    return "The opponent went over. You win"
  elif user_score > computer_score:
    return "You win"
  else:
    return "You lose"
      
def game():
  print(logo)
  user_cards = []
  computer_cards = []
  #Getting the first two cards for the user and computer
  for _ in range(2):
    user_cards.append(deal_card()) 
    computer_cards.append(deal_card())
  
  #For the user to take more cards
  game_over = False
  while not game_over:
    user_score = calculate_score(user_cards)
    computer_score = calculate_score(computer_cards)
    
    print(f"    Your cards: {user_cards}, current score: {user_score}")
    print(f"    Computer's first card: {computer_cards[0]}")
    
    if user_score == 0 or computer_score == 0 or user_score > 21:
      game_over = True
    else:
      next_deal = input("Type 'y' to get another card, type 'n' to pass: ")
      if next_deal == 'y':
        user_cards.append(deal_card()) 
      else:
        game_over = True
      
  #For the computer to take more cards
  while computer_score != 0 and computer_score < 17:
    computer_cards.append(deal_card())
    computer_score = calculate_score(computer_cards)
  
  print(f"    Your final hand: {user_cards}, final score: {user_score}")
  print(f"    Computer's final hand: {computer_cards}, final score: {computer_score}")
  print(compare(user_score, computer_score))

while input("Do you want to play a game of Blackjack? Type 'y' or 'n': ") == 'y':
  clear()
  game()
```

### :arrow_forward:`Day 12` - Scope & Number Guessing Game

[View the game](https://replit.com/@kleamertiri/Guess-the-number-Game?v=1)

```python
import random

EASY_ATTEMPS = 10
HARD_ATTEMPS = 5


#Function to check the user's guess against the random number
def check_number(guess, answer):
  if guess < answer:
      print("Too low.\n")  
  elif guess > answer:
      print("Too high.\n")
  else:
      print(f"You got it. The answer is {answer}")

#Function to set the difficulty
def set_difficulty():
  level = input("Choose the level of difficulty. Take 'easy' or 'hard' ".lower())
  if level == 'easy':
    return EASY_ATTEMPS
  else:
    return HARD_ATTEMPS
                
def game():
  print("Welcome to the Number Guessing Game!")
  print("I'm thinking of a number between 1 and 100.")
  random_number = random.randint(1,100)
  # print(random_number)
  
  
  turns = set_difficulty()
  guess = 0
  while guess != random_number and turns > 0:
    print(f"You have {turns} attempts remaining.")
    guess = int(input("Make a guess: "))
    check_number(guess, random_number)
    turns -= 1
    if turns == 0:
      print("You are out of attemps. You lose.")
      return
    elif guess != random_number:
      print("Guess again.")

game()
```

### :arrow_forward:`Day 13` - Debugging: How to find and fix errors in your code
**Steps:**

1- Describe the problem

2- Reproduce the Bug

3- Play computer and evaluate each line

4- Fixing errors and watching for Red Lines

5- Squash bugs with a `print()` statement

6- Using a [**Debugger**](https://pythontutor.com/)

### :arrow_forward:`Day 14` - [Higher Lower Game Project](https://replit.com/@kleamertiri/Higher-Lower-Game?v=1)

```python
import random
import art
from game_data import data
from replit import clear
a = random.choice(data)
score = 0
right = True
print(art.logo)


#Checking followers
while right:
  b = random.choice(data)
  print(f"Compare A: {a['name']}, a {a['description']}, from {a['country']}")
  print(art.vs)
  print(f"Against B: {b['name']}, a {b['description']}, from {b['country']}")   

  a_or_b = input("Who has more followers? Type 'A' or 'B': ").lower()
  clear()
  print(art.logo)
  if a_or_b == 'a':
    if a['follower_count'] > b['follower_count']:
      
      score += 1
      print(f"\nYou are right! Current score: {score}")
      a = b
      
    else:
      
      print(f"\nOops! You are wrong. Final score: {score}")
      right = False
  else:
      if a['follower_count'] < b['follower_count']:
        score +=1
        print(f"\nYou are right! Current score: {score}")
        a = b
      else:
        print(f"\nOops! You are wrong. Final score {score}")
        right = False
  
```
**OR**

```python
import art
import random
from game_data import data
from replit import clear

#Functions
def format_data(account):
  '''Format the data into a printable format'''
  name = account['name']
  description = account['description']
  country = account['country']
  return f"{name}, a {description}, from {country}"

def check_answer(guess, a_followers, b_followers):
  '''Take the user guess and follower counts and returns if they got it right'''
  if a_followers > b_followers:
    # if guess == a:
    #   return True
    # else:
    #   return False
    return guess == 'a'
  else:
    return guess == 'b'



#Displaying art
print(art.logo)
score = 0
right = True

#Choosing two(a, b) random data set from game_date.py 
account_a = random.choice(data)

#Make the game repeatebale
while right:
  account_b = random.choice(data)
  if account_a == account_b:
    account_b = random.choice(data)

  a = print("Compare A: " + format_data(account_a))
  print(art.vs)
  b = print("Against B: " + format_data(account_b))
  
  #Getting user's input
  user_guess = input("Who has more followers? Type 'A' or 'B': ").lower()

  #Clear the screen
  clear()
  print(art.logo)
  #Checking the user's input 
  ## Comparing the number of followers
  a_followers = account_a['follower_count']
  b_followers = account_b['follower_count']
  
  is_correct = check_answer(user_guess, a_followers, b_followers)
  
  #Give user feedback and track their score
  if is_correct:
    score += 1
    print(f"\nYou are right! Current score: {score}")
    #Change a = b and generate a new random data set for b, when the user is correct
    account_a = account_b
  else:
    print(f"\nOops! You are wrong. Total score: {score}")
    right = False
 ```

### :arrow_forward:`Day 15` - [The Coffee Machine☕](https://replit.com/@kleamertiri/Coffee-Machine?v=1)

```python
MENU = {
    "espresso": {
        "ingredients": {
            "water": 50,
            "coffee": 18,
        },
        "cost": 1.5,
    },
    "latte": {
        "ingredients": {
            "water": 200,
            "milk": 150,
            "coffee": 24,
        },
        "cost": 2.5,
    },
    "cappuccino": {
        "ingredients": {
            "water": 250,
            "milk": 100,
            "coffee": 24,
        },
        "cost": 3.0,
    }
}

profit = 0
resources = {
    "water": 300,
    "milk": 200,
    "coffee": 100,
}

#4 Function to compare the ingredients
def is_resources_enough(ingredients):
  for item in ingredients:
    if ingredients[item] > resources[item]:
      print(f"Sorry there is not enough {item}.")
      return False
  return True

#5
def process_coins():
  '''Returns the total calculated from coins inserted.'''
  print("Please insert coins. ")
  quarters = int(input("How many quarters?: "))
  dimes = int(input("How many dimes?: "))
  nickels = int(input("How many nickels?: "))
  pennies = int(input("How many pennies?: "))
  total = (quarters * 0.25) + (dimes * 0.1) + (nickels * 0.05) + (pennies * 0.01)
  return total


#6
def is_transaction_successful(user_money, cost_drink):
  '''Return True, when the payment is accepted, or False if money is insufficient'''
  if user_money < cost_drink:
    print("Sorry that's not enough money. Money refunded.")
    return False
  elif user_money >= cost_drink:
    change = user_money - cost_drink
    if change > 0:
      print(f"Here is ${round(change, 2)} dollars in change.")
    global profit
    profit += cost_drink
    return True

#7
def make_coffee(drink_name, order_ingredients):
  '''Deduct the required ingredients from the resources.'''
  for item in order_ingredients:
    resources[item] -= order_ingredients[item]
  print(f"Here is your {drink_name} ☕. Enjoy!")
  
  
choice = True
#1
while choice:
  coffee_choice = input("What would you like? (espresso/latte/cappuccino): ")
  #2
  if coffee_choice == "off":
    choice = False
  #3
  elif coffee_choice == "report":
    for key, value in resources.items():
      print(key.capitalize(), ": ", value)
    print(f"Money: ${float(profit)}")
  else:
    drink = MENU[coffee_choice]
    if is_resources_enough(drink['ingredients']):
      payment = process_coins()
      if is_transaction_successful(payment, drink['cost']):
        make_coffee(coffee_choice, drink['ingredients'])
  ```
  
  ### :arrow_forward:`Day 16` - Object Oriented Programming **(OOP)**
  
  ```python
  from prettytable import PrettyTable
x = PrettyTable()
x.field_names = ["Pokemon Name", "Type"]
x.add_rows(
  [
    ["Pikachu", "Electric"],
    ["Squirtle", "Water"],
    ["Charmander", "Fire"]
  ]
)

x.align = "l"
print(x)
```

![image](https://github.com/kleamertiri/100Days-of-Python/assets/105167291/fb428356-b9b5-4297-bc89-d4bd5b7145d3)

[Solution](https://replit.com/@kleamertiri/Coffee-Maker-in-OOP?v=1)

```python
from menu import Menu, MenuItem
from coffee_maker import CoffeeMaker
from money_machine import MoneyMachine

#Creating the objects
money_machine = MoneyMachine()
coffee_maker = CoffeeMaker()
menu = Menu()
choice = True

while choice:
  coffee_choice = input(f"What would you like? ({menu.get_items()}): ")
  
  if coffee_choice == "off":
    choice = False
  
  elif coffee_choice == "report":
    coffee_maker.report()
    money_machine.report()
  else:
    drink = menu.find_drink(coffee_choice)
    if coffee_maker.is_resource_sufficient(drink):
      if money_machine.make_payment(drink.cost):
        coffee_maker.make_coffee(drink)
```

### :arrow_forward:`Day 17` - The Quiz Project & the benefits of OOP
