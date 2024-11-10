# python-practice
python practice 
# Practice    
# Enjoy^_^
# 1. Python Flow Control
 1. Write a Python program to find those numbers which are divisible by 7 and multiples of 5, between 1500 and 2700 (both included). 
start = 1500
end = 2700

for i in range(start , end + 1):
    if i % 7 == 0 and i % 5 == 0:
        print(i)
## 2. Write a Python program to guess a number between 1 and 9.
Note : User is prompted to enter a guess. If the user guesses wrong then the prompt appears again until the guess is correct, on successful guess, user will get a "Well guessed!" message, and the program will exit.
import random

number_to_guess = random.randint(1, 9)

while guess != number_to_guess:
    guess = int(input("Guess a number between 1 and 9: "))
    if guess == number_to_guess:
        print("Well guessed!")
    else:
        print("Try again!")

## 3. Write a Python program that prints all the numbers from 0 to 6 except 3 and 6.
Note : Use 'continue' statement.
Expected Output : 0 1 2 4 5 

for i in range(0 , 7):
    if i == 3:
        continue
    elif i == 6:
        continue
    print(i)
print()

## 4. Write a Python program to construct the following pattern, using a nested for loop.
```
* 
* * 
* * * 
* * * * 
* * * * * 
* * * * 
* * * 
* * 
*
```
rows = 5
for i in range(1 , rows + 1):
    print(" *" * i)

for i in range(rows - 1, 0, -1):
    print(" *" * i)

rows = 8
for i in range(1, rows + 1):
    print(" " * (rows - i) + "* " * i)

for i in range(rows - 1, 0, -1):
    print(" " * (rows - i) + "* " * i)

## 5. Write a Python program that accepts a word from the user and reverses it. 


word = str(input("enter word:"))

reversed_word = word[ :: -1]
print(reversed_word)
## 6. Write a Python program to count the number of even and odd numbers in a series of numbers
Sample numbers : numbers = (1, 2, 3, 4, 5, 6, 7, 8, 9) 

Expected Output :

Number of even numbers : 4

Number of odd numbers : 5
numbers = [2,5,6,7,3,6,7,8,12]

for i in numbers:
    if i% 2 == 0:
        print(f"num {i} is even")
    else:
        print(f"num {i} is odd")
## 7. Write a Python program to print the the first alphabet pattern 'A-Z' in your name .
for example  Expected Output:


```
  ***                                                                   
 *   *                                                                  
 *   *                                                                  
 *****                                                                  
 *   *                                                                  
 *   *                                                                  
 *   *
```

## 8.  Write a Python program to construct the following pattern, using a nested loop number.
Expected Output:


``
1
22
333
4444
55555
666666
7777777
88888888
999999999
``
rows = 9

for i in range(1, rows + 1):
    for j in range(i):
        print(i, end="")
    print()                

## 9. Write a Python program to create the multiplication table (from 1 to 10) of a number.
Expected Output:

Input a number: 6                                                       
6 x 1 = 6                                                               
6 x 2 = 12                                                              
6 x 3 = 18                                                              
6 x 4 = 24                                                              
6 x 5 = 30                                                              
6 x 6 = 36                                                              
6 x 7 = 42                                                              
6 x 8 = 48                                                              
6 x 9 = 54                                                              
6 x 10 = 60 

number = int(input("Input a number: "))

for i in range(1, 11):
    print(f"{number} x {i} = {number * i}")

## 10. Write a Python program to calculate the sum and average of n integer numbers (input from the user). Input 0 to finish.
total_sum = 0
count = 0

while True:
    number = int(input("Enter an integer (enter 0 to finish): "))
    
    if number == 0:
        break 
    
    total_sum += number
    count += 1

if count > 0: 
    average = total_sum / count
    print("Sum:", total_sum)
    print("Average:", average)
else:
    print("No numbers were entered.")

# 11-Python Program to Print the Fibonacci sequence

The Fibonacci numbers are the numbers in the following integer sequence. 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, â€¦â€¦.. In mathematical terms, the sequence Fn of Fibonacci numbers is defined by the recurrence relation.


![image.png](attachment:image.png)
# Finding the Maximum Value in a List
numbers = [3, 7, 2, 9, 5, 8, 10, 12]

max_number = numbers[0]

for num in numbers:
    if num > max_number:
        max_number = num

print("The maximum number is:", max_number)

# Counting Vowels in a String
text = input("Enter a word: ")
vowel_count = 0

vowels = "aeiouAEIOU"

for char in text:
    if char in vowels:
        vowel_count += 1  

print("Number of vowels:", vowel_count)

# Finding Prime Numbers within a Range
start = int(input("Enter the starting number: "))
end = int(input("Enter the ending number: "))

for num in range(start, end + 1):
    if num > 1:
        prime = True  
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                prime = False 
                break 
        if prime:
            print(num, end=" ")

# A Program that Simulating a Basic ATM Withdrawal
balance = 1000 

print("Current balance: " + str(balance))

withdraw_amount = float(input("Enter the amount to withdraw: "))

if withdraw_amount > balance:
    print("Insufficient funds!")
else:
    balance = balance - withdraw_amount
    print("Withdrawal successful, New balance: " + str(balance))

print("Current balance: " + str(balance))
# Finding Common Elements in Two Lists
list1 = [2,1,7,8,5,6]
list2 = [1,7,4,5,2,8]

common_elements = []

for element in list1:
    if element in list2:
        common_elements.append(element) 

print("Common elements:", common_elements)

# Calculating Factorial of a Number
number = int(input("Enter a number to calculate its factorial: "))

factorial = 1

for i in range(1, number + 1):
    factorial *= i  
    print(f"The factorial of {number} is {factorial}.")

# Validating User Input with While Loop
min_value = 15
max_value = 35

while True:
    user_input = input(f"Enter a number between {min_value} and {max_value}: ")
    number = int(user_input)
    if min_value <= number <= max_value:
        print("Valid input! You entered:", number)
        break 
    else:
        print(f"Please enter a number between {min_value} and {max_value}.")
    

# Finding the Sum of Digits of a Number

# Checking for Palindrome Strings

# Creating a Dictionary from Two Lists
keys = ['car_name', 'model', 'year']
values = ['tesla', 'x', '2023']

my_dictionary = {}

for i in range(len(keys)):
    my_dictionary[keys[i]] = values[i]

print("Dictionary:", my_dictionary)

# Simulating a Simple Password Check
correct_password = "ehab91"

password = input("Enter the password: ")

if password == correct_password:
    print("correct password, welcome")
else:
    print("Incorrect password, try again")

# Generating a Multiplication Table for a Given Number
number = int(input("Input a number: "))

for i in range(1, 11):
    print(f"{number} x {i} = {number * i}")
