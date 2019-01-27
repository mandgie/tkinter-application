# tkinter-application
Short description of creating a desktop application with python and its built in library tkinter
```python

from tkinter import *

# from tkinter.ttk import * Extra library for some additional futures

# Create the window of the application
window = Tk()

# Set the window title 
window.title("Welcome to tkinter")

# Set the window size 
window.geometry('500x300')

# Creating a instance from the Label class
lbl = Label(window, text="Hello World", font=("Arial Bold", 50))

#Set the position of the lbl instance
lbl.grid(column=0, row=0)

# Creating an input label
txt = Entry(window, width=10)

#Set position for txt instance
txt.grid(column=1, row=0)

# Set the cursor to be active automatically
txt.focus()

#Write function for button handle
def clicked():
	res = "Welcome to " + txt.get()
	lbl.configure(text=res)

btn = Button(window, text="Click Me", fg="green", command=clicked)

btn.grid(column=2, row=0)

# Ending with the mainloop so the window is always open until user ends session
window.mainloop()
```


The pack() fuction is used to fill the entire window
