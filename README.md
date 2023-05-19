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

#### :arrow_right: Project: Band Name Generator

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
#### :arrow_right: Project: Tip Calculator

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

#### :arrow_right: Project: Treasure Island:old_key:
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
