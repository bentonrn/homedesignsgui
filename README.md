from tkinter import *
import tkinter as tk
from tkinter import messagebox
from PIL import Image, ImageTk 

root = tk.Tk()
root.title("Add Image Example")
root.geometry("400x400")  # Set the window size

# Load the image
# Replace 'path/to/your/image.jpg' with the path to your image file
image_path = "path/to/your/image.jpg"  # Change this to your image file path
img = Image.open("C:\\Users\\regin\\OneDrive\\Documents\\IVY TECH\\SDEV14\\logo.png")  # Open the image file
img_resized = img.resize((300, 300), Image.ANTIALIAS)  # Resize the image if needed
image = ImageTk.PhotoImage(img_resized)  # Create a PhotoImage object

# Create a Label widget to display the image
img_label = tk.Label(root, image=image)
img_label.pack(pady=20)  # Pack the label with some vertical padding

# Function for registration
def register():
    username = username_entry.get()
    email = email_entry.get()
    password = password_entry.get()
    confirm_password = confirm_password_entry.get()
    
    if not username or not email or not password or not confirm_password:
        messagebox.showerror("Error", "Please check to make sure all fields are filled.")
        return
    
    if password != confirm_password:
        messagebox.showerror("Error", "Passwords do not match!")
        return

    # Information is printed
    print(f"Username: {username}\nEmail: {email}\nPassword: {password}")
    messagebox.showinfo("Successful")
    clear_form()

# Restart the Function once input is successful
def clear_form():
    username_entry.delete(0, tk.END)
    email_entry.delete(0, tk.END)
    password_entry.delete(0, tk.END)
    confirm_password_entry.delete(0, tk.END)

# Create the main window (root)
import tkinter as tk
root = tk.Tk()
root.title("DESIGNated Dream Space Login")
root.geometry("500x500")

# Create a Label for Username
username_label = tk.Label(root, text="Username:")
username_label.grid(row=0, column=0, padx=10, pady=10)

# Create an Entry widget for Username
username_entry = tk.Entry(root)
username_entry.grid(row=0, column=1, padx=10, pady=10)

# Create a Label for Email
email_label = tk.Label(root, text="Email:")
email_label.grid(row=1, column=0, padx=10, pady=10)

# Create an Entry widget for Email
email_entry = tk.Entry(root)
email_entry.grid(row=1, column=1, padx=10, pady=10)

# Create a Label for Password
password_label = tk.Label(root, text="Password:")
password_label.grid(row=2, column=0, padx=10, pady=10)

# Create an Entry widget for Password
password_entry = tk.Entry(root, show="*")
password_entry.grid(row=2, column=1, padx=10, pady=10)

# Create a Label for Confirm Password
confirm_password_label = tk.Label(root, text="Confirm Password:")
confirm_password_label.grid(row=3, column=0, padx=10, pady=10)

# Create an Entry widget for Confirm Password
confirm_password_entry = tk.Entry(root, show="*")
confirm_password_entry.grid(row=3, column=1, padx=10, pady=10)

# Create a register button to enter into app
register_button = tk.Button(root, text="Get Started", command=register, width= 10, bg="#ED1C24",fg="#FFFFFF", font=("Arial",12))
register_button.grid(row=5, column=1, columnspan=1, pady=20, sticky = "NSEW")

#Create a login Button to enter into the interface
exit_button = tk.Button(root, text="Leave", command=register, width = 10, bg="#ED1C24",fg="#FFFFFF", font=("Arial",12))
exit_button.grid(row=6, column=1, columnspan=2, pady=20, sticky = "NSEW")

# Create the main window (root)
root = tk.Tk()
root.title("Get Started Form")
root.geometry("500x500")

# Start the event loop
root.mainloop()
