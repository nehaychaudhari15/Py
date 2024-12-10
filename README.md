Practical No: 01

Practical Name: Implement a python program to writing text files, appending to a text file, reading text file





def write_to_file(filename, text):

    """Writes text to a file. If the file exists, it overwrites it."""

    with open(filename, 'w') as file:

        file.write(text)

    print(f"Text written to {filename}.")



def append_to_file(filename, text):

    """Appends text to a file. If the file doesn't exist, it creates one."""

    with open(filename, 'a') as file:

        file.write(text)

    print(f"Text appended to {filename}.")



def read_from_file(filename):

    """Reads and returns the contents of a file."""

    try:

        with open(filename, 'r') as file:

            content = file.read()

        return content

    except FileNotFoundError:

        return f"The file {filename} does not exist."



if __name__ == "__main__":

    # Specify the filename

    filename = "example.txt"



    # Writing to the file

    write_to_file(filename, "Hello, World!\n")



    # Appending to the file

    append_to_file(filename, "This is an appended line.\n")



    # Reading from the file

    content = read_from_file(filename)

    print("Contents of the file:")

    print(content)



Output:

Text written to example.txt.

Text appended to example.txt.

Contents of the file:

Hello, World!

This is an appended line. 

Practical No: 02

Practical Name: Implement a python program based on simple statement using variables, built in data types, arithmetic operations, etc.





# Define variables for length and width

length = 5.0  # float for length in units

width = 3.0   # float for width in units



# Calculate the area

area = length * width



# Prepare a message

message = f"The area of the rectangle with length {length} and width {width} is {area}."



# Print the message

print(message)



Output: 

The area of the rectangle with length 5.0 and width 3.0 is 15.0.

 

Practical No: 3.1

Practical Name: Write a python program to calculate factorial of given number. 





def factorial(n):

    """Calculate the factorial of a given number n."""

    if n < 0:

        return "Factorial is not defined for negative numbers."

    elif n == 0:

        return 1

    else:

        result = 1

        for i in range(1, n + 1):

            result *= i

        return result



# Input number

number = 5  # Change this value to test with other numbers



# Calculate factorial

fact = factorial(number)



# Print the result

print(f"The factorial of {number} is {fact}.")





Output: 

The factorial of 5 is 120.

 

Practical No: 3.2

Practical Name: Write a python program to print Fibonacci series upto given range.





def fibonacci_series(n):

    """Print Fibonacci series up to n."""

    fib_sequence = []

    a, b = 0, 1

    while a <= n:

        fib_sequence.append(a)

        a, b = b, a + b

    return fib_sequence



# Input range

range_limit = 50  # Change this value to set the upper limit



# Get Fibonacci series

fibonacci_numbers = fibonacci_series(range_limit)



# Print the result

print(f"Fibonacci series up to {range_limit}: {fibonacci_numbers}")





Output:

Fibonacci series up to 50: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55]

 

Practical No: 3.3

Practical Name: Write a python program to check whether the given number is prime or not.





def is_prime(n):

    """Check if the number n is prime."""

    if n <= 1:

        return False

    for i in range(2, int(n**0.5) + 1):

        if n % i == 0:

            return False

    return True



# Input number

number = 29  # Change this value to test with other numbers



# Check if the number is prime

if is_prime(number):

    print(f"{number} is a prime number.")

else:

    print(f"{number} is not a prime number.")



Output: 

29 is a prime number.

 

Practical No: 3.4

Practical Name: Write a python program to check whether the given number is Armstrong number or not.





def is_armstrong_number(n):

    """Check if the number n is an Armstrong number."""

    # Convert the number to string to easily iterate over digits

    digits = str(n)

    power = len(digits)  # Number of digits

    sum_of_powers = sum(int(digit) ** power for digit in digits)  # Calculate the sum of powers



    return sum_of_powers == n  # Check if the sum equals the original number



# Input number

number = 153  # Change this value to test with other numbers



# Check if the number is an Armstrong number

if is_armstrong_number(number):

    print(f"{number} is an Armstrong number.")

else:

    print(f"{number} is not an Armstrong number.")



Output: 

153 is an Armstrong number.

 

Practical No: 4.1

Practical Name: Implement a python program based on using tuples.





def display_person_info(person):

    """Display information about a person."""

    name, age, city = person

    print(f"Name: {name}")

    print(f"Age: {age}")

    print(f"City: {city}")



# Create a tuple to store person information

person_info = ("Alice", 30, "New York")



# Display the person's information

display_person_info(person_info)



Output: 

Name: Alice 

Age: 30 

City: New York

 

Practical No: 4.2

Practical Name: Implement a python program based on using list.





def calculate_sum_and_average(numbers):

    """Calculate the sum and average of a list of numbers."""

    total = sum(numbers)

    average = total / len(numbers) if numbers else 0  # Handle empty list case

    return total, average



# Create a list of numbers

numbers_list = [10, 20, 30, 40, 50]



# Calculate sum and average

total_sum, average = calculate_sum_and_average(numbers_list)



# Display the results

print(f"Numbers: {numbers_list}")

print(f"Sum: {total_sum}")

print(f"Average: {average}")





Output: 

Numbers: [10, 20, 30, 40, 50]

Sum: 150

Average: 30.0

 

Practical No: 4.3

Practical Name: Implement a python program based on using dictionary.





def display_student_info(student):

    """Display information about a student."""

    print(f"Name: {student['name']}")

    print(f"Age: {student['age']}")

    print(f"Grades: {student['grades']}")

    print(f"Average Grade: {sum(student['grades']) / len(student['grades'])}")



# Create a dictionary to store student information

student_info = {

    "name": "John Doe",

    "age": 21,

    "grades": [88, 92, 79, 85, 90]

}



# Display the student's information

display_student_info(student_info)



Output:

Name: John Doe

Age: 21

Grades: [88, 92, 79, 85, 90]

Average Grade: 86.4

 

Practical No: 4.4

Practical Name: Implement a python program based on using set.





def set_operations(set_a, set_b):

    """Perform various set operations."""

    union = set_a.union(set_b)

    intersection = set_a.intersection(set_b)

    difference = set_a.difference(set_b)

    symmetric_difference = set_a.symmetric_difference(set_b)



    return union, intersection, difference, symmetric_difference



# Create two sets of numbers

set_a = {1, 2, 3, 4, 5}

set_b = {4, 5, 6, 7, 8}



# Perform set operations

union, intersection, difference, symmetric_difference = set_operations(set_a, set_b)



# Display the results

print(f"Set A: {set_a}")

print(f"Set B: {set_b}")

print(f"Union: {union}")

print(f"Intersection: {intersection}")

print(f"Difference (A - B): {difference}")

print(f"Symmetric Difference: {symmetric_difference}")



Output:

Set A: {1, 2, 3, 4, 5}

Set B: {4, 5, 6, 7, 8}

Union: {1, 2, 3, 4, 5, 6, 7, 8}

Intersection: {4, 5}

Difference (A - B): {1, 2, 3}

Symmetric Difference: {1, 2, 3, 6, 7, 8}

 

Practical No: 5.1

Practical Name: Implement a python program for calculating factorial using functions.





def factorial(n):

    """Calculate the factorial of a given number n."""

    if n < 0:

        return "Factorial is not defined for negative numbers."

    elif n == 0:

        return 1

    else:

        result = 1

        for i in range(1, n + 1):

            result *= i

        return result



# Input number

number = 5  # Change this value to test with other numbers



# Calculate factorial

fact = factorial(number)



# Print the result

print(f"The factorial of {number} is {fact}.")



Output: 

The factorial of 5 is 120.

 

Practical No: 5.2

Practical Name: Implement a python program based on functions inside a function to print multiplication table.





def print_multiplication_table(number):

    """Print the multiplication table for the given number."""

    

    def multiply(n, i):

        """Return the product of n and i."""

        return n * i

    

    print(f"Multiplication Table for {number}:")

    for i in range(1, 11):  # Multiplication from 1 to 10

        product = multiply(number, i)

        print(f"{number} x {i} = {product}")



# Input number

num = 7  # Change this value to print the multiplication table for a different number



# Call the function to print the multiplication table

print_multiplication_table(num)



Output:

Multiplication Table for 7:

7 x 1 = 7

7 x 2 = 14

7 x 3 = 21

7 x 4 = 28

7 x 5 = 35

7 x 6 = 42

7 x 7 = 49

7 x 8 = 56

7 x 9 = 63

7 x 10 = 70

 

Practical No: 5.3

Practical Name: Implement a python program based on built in functions.





def process_numbers(numbers):

    """Process a list of numbers to calculate sum, max, min, and sort."""

    

    # Calculate the sum

    total = sum(numbers)

    

    # Find the maximum and minimum

    maximum = max(numbers)

    minimum = min(numbers)

    

    # Sort the list

    sorted_numbers = sorted(numbers)



    return total, maximum, minimum, sorted_numbers



# Input list of numbers

numbers_list = [12, 5, 8, 21, 3, 17]



# Process the numbers

total_sum, max_value, min_value, sorted_list = process_numbers(numbers_list)



# Display the results

print(f"Numbers: {numbers_list}")

print(f"Sum: {total_sum}")

print(f"Maximum: {max_value}")

print(f"Minimum: {min_value}")

print(f"Sorted List: {sorted_list}")



Output:

Numbers: [12, 5, 8, 21, 3, 17]

Sum: 66

Maximum: 21

Minimum: 3

Sorted List: [3, 5, 8, 12, 17, 21]

 

Practical No: 5.4

Practical Name: Implement a python program to demonstrate the working of single inheritance.





# Base class

class Animal:

    def __init__(self, name):

        self.name = name



    def speak(self):

        return "Animal makes a sound"



# Derived class

class Dog(Animal):

    def speak(self):

        return "Woof! Woof!"



# Creating an instance of the Dog class

my_dog = Dog("Buddy")



# Displaying information

print(f"Dog's Name: {my_dog.name}")

print(f"{my_dog.name} says: {my_dog.speak()}")



Output: 

Dog's Name: Buddy

Buddy says: Woof! Woof!

 

Practical No: 6.1

Practical Name: Implement a python program to calculate area of class and object.





import math



# Base class for shapes

class Shape:

    def area(self):

        pass



# Derived class for Rectangle

class Rectangle(Shape):

    def __init__(self, width, height):

        self.width = width

        self.height = height



    def area(self):

        return self.width * self.height



# Derived class for Circle

class Circle(Shape):

    def __init__(self, radius):

        self.radius = radius



    def area(self):

        return math.pi * (self.radius ** 2)



# Create instances of Rectangle and Circle

rectangle = Rectangle(5, 10)  # Width: 5, Height: 10

circle = Circle(7)             # Radius: 7



# Calculate and display the areas

print(f"Area of the Rectangle: {rectangle.area()}")  # Outputs: 50

print(f"Area of the Circle: {circle.area():.2f}")   # Outputs: 153.94



Output:

Area of the Rectangle: 50

Area of the Circle: 153.94

 

Practical No: 6.2

Practical Name: Implement a python program based on function inside a function to print multiplication table.





def print_multiplication_table(number):

    """Print the multiplication table for the given number."""

    

    def multiply(n, i):

        """Return the product of n and i."""

        return n * i

    

    print(f"Multiplication Table for {number}:")

    for i in range(1, 11):  # Multiplication from 1 to 10

        product = multiply(number, i)

        print(f"{number} x {i} = {product}")



# Input number

num = 6  # Change this value to print the multiplication table for a different number



# Call the function to print the multiplication table

print_multiplication_table(num)



Output:

Multiplication Table for 6:

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

 

Practical No: 07

Practical Name: Implement a python program to create import and use package and modules.





Step 1: Create a directory structure like this:

my_package/

    __init__.py

    math_operations.py

main.py



Step 2: In the my_package directory, create a file named math_operations.py and add the following code:

def square(n):

    """Return the square of a number."""

    return n * n



Step 3: In the same my_package directory, you can leave __init__.py empty or add initialization code. For simplicity, we will leave it empty.



Step 4: In the root directory (where my_package is located), create a file named main.py and add the following code:

# Importing the square function from the math_operations module in my_package

from my_package.math_operations import square



# Using the imported function

number = 5

result = square(number)



# Display the result

print(f"The square of {number} is {result}.")



Output: 

The square of 5 is 25.

 

Practical No: 8.1

Practical Name: Implement a python program to write text file appending text to a file reading text file.





# Function to write initial text to a file

def write_to_file(filename, text):

    with open(filename, 'w') as file:

        file.write(text)



# Function to append text to a file

def append_to_file(filename, text):

    with open(filename, 'a') as file:

        file.write(text)



# Function to read and display contents of the file

def read_file(filename):

    with open(filename, 'r') as file:

        contents = file.read()

    return contents



# Define the filename

filename = 'sample.txt'



# Write initial text to the file

write_to_file(filename, 'Hello, World!\n')



# Append more text to the file

append_to_file(filename, 'This is the second line.\n')

append_to_file(filename, 'Appending another line.\n')



# Read the contents of the file

file_contents = read_file(filename)



# Display the contents of the file

print("Contents of the file:")

print(file_contents)



Output:

Contents of the file:

Hello, World!

This is the second line.

Appending another line.

 

Practical No: 8.2

Practical Name: Implement a python program to demonstrate paths and directories, file information, renaming, moving, copying and removing files.





import os

import shutil



# Define paths

source_file = 'source_file.txt'

destination_dir = 'destination_dir'

moved_file = os.path.join(destination_dir, 'moved_file.txt')

copied_file = os.path.join(destination_dir, 'copied_file.txt')



# Create a source file

with open(source_file, 'w') as file:

    file.write('This is a source file.\n')



# Create a destination directory

os.makedirs(destination_dir, exist_ok=True)



# Display initial file information

print("Initial file information:")

print(f"Source File Exists: {os.path.exists(source_file)}")

print(f"Destination Directory Exists: {os.path.exists(destination_dir)}")



# Move the file

shutil.move(source_file, moved_file)

print(f"\nMoved '{source_file}' to '{moved_file}'.")



# Display information after moving

print("\nFile information after moving:")

print(f"Source File Exists: {os.path.exists(source_file)}")

print(f"Moved File Exists: {os.path.exists(moved_file)}")



# Create a new file to copy

with open(moved_file, 'a') as file:

    file.write('This file has been moved.\n')



# Copy the moved file

shutil.copy(moved_file, copied_file)

print(f"\nCopied '{moved_file}' to '{copied_file}'.")



# Display information after copying

print("\nFile information after copying:")

print(f"Moved File Exists: {os.path.exists(moved_file)}")

print(f"Copied File Exists: {os.path.exists(copied_file)}")



# Remove the copied file

os.remove(copied_file)

print(f"\nRemoved '{copied_file}'.")



# Final file information

print("\nFinal file information:")

print(f"Moved File Exists: {os.path.exists(moved_file)}")

print(f"Copied File Exists: {os.path.exists(copied_file)}")



Output:

Initial file information:

Source File Exists: True

Destination Directory Exists: True



Moved 'source_file.txt' to 'destination_dir/moved_file.txt'.



File information after moving:

Source File Exists: False

Moved File Exists: True



Copied 'destination_dir/moved_file.txt' to 'destination_dir/copied_file.txt'.



File information after copying:

Moved File Exists: True

Copied File Exists: True



Removed 'destination_dir/copied_file.txt'.



Final file information:

Moved File Exists: True

Copied File Exists: False

 

Practical No: 9.1

Practical Name: Python program using anonymous functions lambda and filter.





# Sample list of numbers

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]



# Using filter with a lambda function to get even numbers

even_numbers = list(filter(lambda x: x % 2 == 0, numbers))



# Display the results

print("Original List:", numbers)

print("Even Numbers:", even_numbers)



Output:

Original List: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

Even Numbers: [2, 4, 6, 8, 10]

 

Practical No: 9.2

Practical Name: Python program using maps, list comprehension, directories.





import os



# Define the directory

directory = '.'  # Current directory



# Get the list of files in the specified directory

file_names = os.listdir(directory)



# Use map to convert file names to uppercase

uppercase_files_map = list(map(lambda name: name.upper(), file_names))



# Use list comprehension to get uppercase file names

uppercase_files_list_comprehension = [name.upper() for name in file_names]



# Display the results

print("Original File Names:", file_names)

print("Uppercase File Names using map():", uppercase_files_map)

print("Uppercase File Names using List Comprehension:", uppercase_files_list_comprehension)



Output:  

Original File Names: ['file1.txt', 'file2.txt', 'image.png', 'script.py']

Uppercase File Names using map(): ['FILE1.TXT', 'FILE2.TXT', 'IMAGE.PNG', 'SCRIPT.PY']

Uppercase File Names using List Comprehension: ['FILE1.TXT', 'FILE2.TXT', 'IMAGE.PNG', 'SCRIPT.PY']

 

Practical No: 9.3

Practical Name: Python program using command line and getting options from the command line - Get opt.





import sys

import getopt



def main(argv):

    operation = ''

    num1 = 0

    num2 = 0

    

    # Parse command line options

    try:

        opts, args = getopt.getopt(argv, "o:n:m:", ["operation=", "num1=", "num2="])

    except getopt.GetoptError:

        print('Usage: script.py -o <operation> -n <num1> -m <num2>')

        sys.exit(2)



    for opt, arg in opts:

        if opt in ("-o", "--operation"):

            operation = arg

        elif opt in ("-n", "--num1"):

            num1 = float(arg)

        elif opt in ("-m", "--num2"):

            num2 = float(arg)



    # Perform the operation

    if operation == 'add':

        result = num1 + num2

        print(f'The result of adding {num1} and {num2} is: {result}')

    elif operation == 'multiply':

        result = num1 * num2

        print(f'The result of multiplying {num1} and {num2} is: {result}')

    else:

        print('Unknown operation. Please use "add" or "multiply".')



if __name__ == "__main__":

    main(sys.argv[1:])



Output:

The result of adding 5.0 and 3.0 is: 8.0

 

Practical No: 9.4

Practical Name: Python program based on using threads.





import threading

import time



# Function to count numbers

def count_numbers(thread_name, count):

    for i in range(1, count + 1):

        print(f"{thread
