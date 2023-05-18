# #100DaysOfCode🐍
In this repository, I will show the different Python exercises I will be doing on the 100 Days of Code.

## Two main rules:
1- Code minimum an hour every day for the next 100 days.

2- Show your progress every day on social media.

### :arrow_forward:`Day 1` - Working with Variables in Python to Manage Data
#### Exercise 1
Write a program that prints the notes using what you have learnt about the Python print function.
```python
#Write your code below this line 👇
print("Day 1 - Python Print Function \nThe function is declared like this: \nprint('what to print')")
```
#### Exercise 2
Write a program that prints the number of characters in a user's name.

```python
#Write your code below this line 👇
userName = input("What is your name? ")
print(len(userName))
```
#### Exercise 3
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

#### Project: Band Name Generator

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

#### Exercise 1
Write a program that adds the digits in a 2 digit number. e.g. if the input was 35, then the output should be 3 + 5 = 8

```python
two_digit_number = (input("Type a two digit number: "))
print(int(two_digit_number[0]) + int(two_digit_number[1]))
```

#### Exercise 2
Write a program that calculates the Body Mass Index (BMI) from a user's weight and height.

```python
height = input("enter your height in m: ")
weight = input("enter your weight in kg: ")
bmi = float(weight) / float(height) ** 2
print(int(bmi))
```

#### Exercise 3
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
#### Project: Tip Calculator

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

#### Exercise 1
Write a program that works out whether if a given number is an odd or even number.
```python
number = int(input("Which number do you want to check? ")

if number % 2 == 0:
    print("This is an even number.")
else:
    print("This is an odd number.")    
```    
