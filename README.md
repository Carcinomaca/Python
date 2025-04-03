#String:
#1.] Program to demonstrate string operations in Python
print("Program to demonstrate string operations in Python")

# Creating strings
print("1st string:")
a = "Hello, World!"
print(a)

# Constructor string
print("2nd string:")
b = str('Python Programming')
print(b)

#2.] Accessing string characters
print("Program for accessing characters in a string")
a = "Programming"
print("Accessing the whole string:", a)
print("Accessing the 2nd character of the string:", a[1])
print("Accessing the 3rd to 5th characters of the string:", a[2:5])
print("Accessing the last character of the string:", a[-1])
print("Accessing characters from 2nd to the last:", a[1:])
print("Accessing characters from start to 5th:", a[:5])
print("Accessing characters from last to 3rd in reverse:", a[-1:-8:-1])

#3.] Adding elements to a string (concatenation)
print("Program to add strings:")
a = "Hello"
a = a + " World!"
print(a)

a = a[:5] + " Python" + a[5:]
print(a)

a = a + " Programming is fun!"
print(a)

#4.] Updating characters in a string (modifying string through replacement)
print("Program to update characters in a string:")
a = "Hello Computer"
print(a)
a = a.replace("Computer", "World")  # Changing word in the string
print(a)

#5.] Deleting elements in a string (removal using replace and slicing)
print("Program to delete characters from a string:")
a = "Hello World"
print(a)
a = a.replace("World", "")  # Removing a substring
print(a)
a = a[:-1]  # Removing the last character
print(a)
a = a[:3] + a[4:]  # Removing a character at a specific position
print(a)

#6.] Iterating through a string
print("Program for iterating through a string:")
a = "Python"
for i in a:
    print(i)

for i in a:
    if i == 't':
        print(i)
    else:
        print("error")

#7.] Attempt to change an element in a string
print("Attempting to change an element in a string:")
a = "Immutable"
a[0] = "i"  # This will give an error because strings are immutable in Python
print(a)
#Tuple:
print("Program to create a tuple and check its type")
# 1st method: Creating tuple using round brackets
t = (10, 20, 30)
print("1st method:", t)
print("Type:", type(t))
# 2nd method: Creating tuple without using round brackets
t1 = 10, 20, 30, 40
print("\n2nd method:", t1)
print("Type:", type(t1))
# 3rd method: Creating tuple using constructor
t2 = tuple([10, 20, 30])
print("\n3rd method:", t2)
print("Type:", type(t2))
# 4th method: Creating tuple with a single element
t3 = (7,)
print("\n4th method (single element tuple):", t3)
print("Type:", type(t3))
t4 = (100)  # This is an integer, not a tuple
print("\nIncorrect single element tuple:", t4)
print("Type:", type(t4))
# Tuple Packing
a, b, c = 10, 20, 30
t5 = (a, b, c)
print("\nTuple Packing:", t5)

t6 = (c, a, b)
print("Rearranged Tuple:", t6)
# Accessing elements in a tuple
t7 = (10, 20, 30, 40, 50, 60, 70, 80, 90, 100)
print("\nAccessing elements in a tuple:")
print("Whole tuple:", t7)
print("2nd element:", t7[1])
print("3rd to 5th elements:", t7[2:5])
print("2nd last element:", t7[-2])
# Creating tuple with multiple data types
t8 = (10, True, 7, 20, "Hello")
print("\nTuple with multiple data types:", t8)
# Duplicate values are allowed
t9 = (10, True, 7, 20, "Hello", 7)
print("\nTuple with duplicate values:", t9)
# Traversing tuple using for loop
t11 = (10, 20, 30, 40, 50, 60, 70, 80, 90, 100)
print("\nTraversing tuple using for loop:")
for i in t11:
    print(i)
# Concatenation of tuples
t12 = ("Hello",)
t13 = ("world",)
print("\nConcatenated Tuple:", t12 + t13)
# Deleting tuple
t7 = (10, 20, 30, 40, 50, 60, 70, 80, 90, 100)
del t7
# Converting list to tuple
a = [7, 10, 18]
print("\nList:", a)
print("Type:", type(a))
c = tuple(a)
print("Converted to Tuple:", c)
print("Type:", type(c))
# Nesting of Tuples
tuple1 = (1, 2, 3)
tuple2 = ("A", "B", "C")
nested_tuple = (tuple1, tuple2)
print("\nNested Tuple:", nested_tuple)
#Dictionary:
d1 = {
    1: "Apple",
    2: "Banana",
    3: "Orange"
}
d2 = {
    "a": "Apple",
    "b": "Banana"
}

# Accessing elements in a dictionary.
print(d2['b'])
# Another way of accessing
print(d2.get('a'))

# Adding values in a dictionary.
d1[4] = 'cherry'
print(d1)
d2['c'] = 'cherry'
print(d2)

# Updating values in a dictionary.
d1[3] = 'Kiwi'
print(d1)

# Removing elements by using pop function
v = d1.pop(1)
print(v)
print(d1)


# Using the popitem() function
popped_item = d1.popitem()
print("Popped item:", popped_item)
print(d1)

# Using the del statement.
del d2['b']
print(d2)

# Using the clear function.
d2.clear()
print(d2)

# Iteration in a dictionary
# Method 1: Iterating over keys
for key in d1:
    print(key)

# Method 2: Iterating over values
for value in d1.values():
    print(value)

# Method 3: Iterating over key-value pairs using items()
for key, value in d1.items():
    print(key, value)
Errors:
#1]program 1 
try:
    b = 0
    c = 100/b
except ZeroDivisionError:
    print("Division by zero is not possible!")
except ValueError:
    print("Invalid Number!")
else:
    print("Answer=",c)
finally:
    print("Output displayed!")

#2]program for catching all exceptions.
try:
    b = "10"/20
except ArithmeticError:
    print("Invalid operation")
except:
    print("Error occured!")
#3] program for catching multiple exception.
try:
    b = "10"
    c = 100/b
except(ZeroDivisionError,ValueError,TypeError):
    print("Invalid operation")
else:
    print("Division=",c)
finally:
    print("Output Displayed")
#RegEx
EXAMPLE 1:-Basic Regular Expression Matching
import re


# Define a pattern
pattern = r"\b[A-Z][a-z]+\b" # Matches words that start with a capital letter


# Sample text
text = "Hello, my name is John and I live in New York."


# Find all matches
matches = re.findall(pattern, text)


# Print matches
print("Words starting with a capital letter:", matches)
OUTPUT:-


EXAMPLE 2:- Validating an Email Address
import re


# Email validation function
 
def is_valid_email(email):
pattern = r"^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$" return bool(re.match(pattern, email))

# Test emails
emails = ["test@example.com", "hello@domain", "user@company.co.in", "invalid@.com"]


# Check validity
for email in emails:
print(f"{email}: {'Valid' if is_valid_email(email) else 'Invalid'}") OUTPUT:-


EXAMPLE 3:- Extracting Phone Numbers
import re


# Sample text with phone numbers
text = "Call me at +1-800-555-1234 or 9876543210."


# Regex pattern for phone numbers
pattern = r"\+?\d{1,3}[-.\s]?\d{3}[-.\s]?\d{3}[-.\s]?\d{4}|\d{10}"
 
# Find matches
matches = re.findall(pattern, text)


# Print extracted phone numbers print("Extracted Phone Numbers:", matches) OUTPUT:-


EXAMPLE 4:- Replacing Text Using Regex
import re


# Sample text
text = "Python is great! I love Python."


# Replace 'Python' with 'Java'
new_text = re.sub(r"Python", "Java", text)


print("Modified Text:", new_text) OUTPUT:-
 
EXAMPLE5:- Splitting a String Using Regex

import re


# Sample string
text = "apple,banana;orange|grapes"


# Split using multiple delimiters (comma, semicolon, and pipe) fruits = re.split(r"[;,|]", text)
print("Fruits List:", fruits) OUTPUT:-

#Tkinter:
#1.]PROG 1 :- prog using Button function print("prog 1")
import tkinter as tk def abc():
print("this is function called") root=tk.Tk()
f=tk.Frame(root) f.pack()
b1=tk.Button(f,text="QUIT",fg="red",command="qiut") b1.pack(side=tk.LEFT) b2=tk.Button(f,text="HELLO",command="abc") b2.pack(side=tk.LEFT)
root.mainloop()


#OUTPUT :-



#2.]PROG 2 :- prog of using Labels in tkinter print("prog 2")
import tkinter as tk root=tk.Tk()
w=tk.Label(root,text="SUN",bg="red",fg="white") w.pack() w=tk.Label(root,text="GRASS",bg="green",fg="black") w.pack() w=tk.Label(root,text="SKY",bg="blue",fg="white") w.pack()
root.mainloop() #OUTPUT :-
 
 


#3.]demo check box print("prog 3")
from tkinter import* m=Tk() v1=IntVar()
Checkbutton(m,text="MALE",variable="v1").grid(row=0,sticky=W) v2=IntVar() Checkbutton(m,text="FEMALE",variable="v2").grid(row=1,sticky=W) mainloop()

#OUTPUT :-



#4.]demo list box print("prog 4")
from tkinter import* top=Tk() Lb=Listbox(top) Lb.insert(1,'PYTHON') Lb.insert(2,'JAVA')
Lb.insert(3,'C++')
Lb.insert(4,'HTML') Lb.insert(5,'ANY OTHER') Lb.pack()
top.mainloop()
 
#OUTPUT :-



# 5]demo radio button from tkinter import * root = Tk()
v = IntVar() Radiobutton(root,text="GFG",variable=v,value=1).pack(anchor = W) Radiobutton(root,text="MIT",variable=v,value=2).pack(anchor = W) mainloop()

import tkinter as tk

root = tk.Tk()
var = tk.IntVar()

tk.Checkbutton(root, text="Check me", variable=var).pack()
root.mainloop()

import tkinter as tk

root = tk.Tk()
var = tk.StringVar(value="1")

tk.Radiobutton(root, text="Option 1", variable=var, value="1").pack()
tk.Radiobutton(root, text="Option 2", variable=var, value="2").pack()

root.mainloop()

import tkinter as tk

root = tk.Tk()
listbox = tk.Listbox(root)
listbox.pack()

for item in ["Item 1", "Item 2", "Item 3"]:
    listbox.insert(tk.END, item)

root.mainloop()

import tkinter as tk

root = tk.Tk()
entry = tk.Entry(root)
entry.pack()

root.mainloop()
import tkinter as tk

root = tk.Tk()
tk.Label(root, text="Hello, Tkinter!").pack()

root.mainloop()
import tkinter as tk

root = tk.Tk()
mb = tk.Menubutton(root, text="Menu")
mb.menu = tk.Menu(mb, tearoff=0)
mb["menu"] = mb.menu

mb.menu.add_command(label="COD")
mb.menu.add_command(label="BGMI")

mb.pack()
root.mainloop()


#OUTPUT :-

import os

import pandas as pd

num = int(input("Enter a number:"))
if num % 2 == 0:
    result = "Even"
else:
    result = "Odd"

data = {
    "Number": [num], "result": [result]
}
df = pd.DataFrame(data)

file_name = "result.xlsx"

if os.path.exists(file_name):
    df_existing = pd.read_excel(file_name)
    df_combine = pd.concat([df_existing, df], ignore_index=True)
    df_combine.to_excel(file_name, index=False)

else:
df.to_excel(file_name,index = False)
print("Data saved in Excel")

  

#2.]prog 2

import os

import pandas as pd

def get_student_info():
    name = input("Enter a name: ")
    roll_no = int(input("Enter your roll_no: "))
    marks = int(input("Enter your marks: "))
    result = "Pass" if marks >= 20 else "Fail"
    return {
        "name": name,
        "roll_no": roll_no,
        "marks": marks,
        "result": result
    }
student_data = get_student_info()
df = pd.DataFrame([student_data])  # Wrap in a list to create a proper DataFrame
file_name = "result1.xlsx"
if os.path.exists(file_name):
    df_existing = pd.read_excel(file_name)
    df_combined = pd.concat([df_existing, df], ignore_index=True)
    df_combined.to_excel(file_name, index=False)
else:
    df.to_excel(file_name, index=False)

print("Data saved in Excel")

  

#3.]

import tkinter as tk

from tkinter import messagebox import pandas as pd
import os


root = tk.Tk() root.title("Student Data Entry") root.geometry("400x450")


empno_var = tk.StringVar() empname_var = tk.StringVar() gender_var = tk.StringVar() city_var = tk.StringVar() hobby_reading = tk.IntVar() hobby_travelling = tk.IntVar() hobby_sports = tk.IntVar()


tk.Label(root, text="Employee no").pack() tk.Entry(root, textvariable=empno_var).pack()


tk.Label(root, text="Employee name").pack() tk.Entry(root, textvariable=empname_var).pack()


tk.Label(root, text="Gender").pack()

tk.Radiobutton(root, text="Male", value="Male", variable=gender_var).pack() tk.Radiobutton(root, text="Female", value="Female", variable=gender_var).pack()


tk.Label(root, text="Hobbies").pack()

tk.Checkbutton(root, text="Reading", variable=hobby_reading).pack() tk.Checkbutton(root, text="Travelling", variable=hobby_travelling).pack() tk.Checkbutton(root, text="Sports", variable=hobby_sports).pack()
 
root.mainloop()


#4.]

import tkinter as tk

from tkinter import messagebox


def submit():

empno = empno_var.get() empname = empname_var.get() gender = gender_var.get()
city = city_var.get() hobbies = []


if hobby_reading.get(): hobbies.append("Reading")
if hobby_travelling.get(): hobbies.append("Travelling")
if hobby_sports.get(): hobbies.append("Sports")


messagebox.showinfo("Submitted Data",

f"Employee No: {empno}\nEmployee Name: {empname}\nGender: {gender}\nCity: {city}\nHobbies:
{', '.join(hobbies)}")


root = tk.Tk() root.title("Student Data Entry") root.geometry("400x450")


empno_var = tk.StringVar() empname_var = tk.StringVar() gender_var = tk.StringVar() city_var = tk.StringVar() hobby_reading = tk.IntVar()
 
hobby_travelling = tk.IntVar() hobby_sports = tk.IntVar()


tk.Label(root, text="Employee no").pack() tk.Entry(root, textvariable=empno_var).pack()


tk.Label(root, text="Employee name").pack() tk.Entry(root, textvariable=empname_var).pack()


tk.Label(root, text="Gender").pack()

tk.Radiobutton(root, text="Male", value="Male", variable=gender_var).pack() tk.Radiobutton(root, text="Female", value="Female", variable=gender_var).pack()


tk.Label(root, text="Hobbies").pack()

tk.Checkbutton(root, text="Reading", variable=hobby_reading).pack() tk.Checkbutton(root, text="Travelling", variable=hobby_travelling).pack() tk.Checkbutton(root, text="Sports", variable=hobby_sports).pack()


tk.Label(root, text="City").pack()

city = ["Select city", "Mumbai", "Bangalore", "Rajasthan", "Gujarat"] city_var.set(city[0])
tk.OptionMenu(root, city_var, *city).pack()


tk.Button(root, text="Submit", command=submit).pack()


root.mainloop()






