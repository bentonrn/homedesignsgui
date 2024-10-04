# homedesignsgui
Home design program that is customizable and allows 
File: homedesignergui.py
Date Written: 10.3.2024
"This program is a simple home design interface
that asks user to sign and and sign out. 
"""
from tkinter import *
import tkinter as tk
from PIL import ImageTk, Image

root = Tk()
root.title("DESIGNated Dream Space")
root.iconbitmap('C:\\Users\\regin\OneDrive\\Documents\\IVY TECH\\SDEV140\\image_t.png')
my_img = ImageTk.PhotoImage(Image.open("logo.png"))
my_label = Label(image = my_img)
my_label.pack()


e = Entry(root, width =30)
e.pack(padx=10,pady=10)
e.insert(0, "Enter First & Last Name")

#Create a label widget
def myClick():
    greeting = "Welcome Home" + e.get()
myButton = Button(root, text="Design Your Ultimate Space!", fg="#9E2365", bg="white")
myButton.pack()
myButton = Button(root, text="Get Started!", command=myClick, fg="white", bg="red")
myButton.pack()
button_quit = Button(root,text = "Leave", command = root.quit)
button_quit.pack()
myButton2 = Button(root, text="Sign Up!", command=myClick, fg="white", bg="red")
myButton2.pack()
# Wait to see what the first button does before deleting this comment: myButton = Button(root, text="Sign In")

"""
myLabel2 = Label(root, text = "Imagine a place where you can have your own DREAM SPACE!")
MyLabel4 = Label(root, text="Lets Create An Account:")
"""
    
#Placing it onto the screen

#Create the loop

root.mainloop()
