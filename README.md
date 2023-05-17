# #100DaysOfCode🐍
In this repository, I will show the different Python exercises I will be doing on the 100 Days of Code.

## Two main rules:
1- Code minimum an hour every day for the next 100 days.

2- Show your progress every day.

### :arrow_forward:Day 1 - Working with Variables in Python to Manage Data
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
