import tkinter as tk
import random
import string

def generate_password():
    length = 15
    characters = string.ascii_lowercase

    if uppercase_var.get():
        characters += string.ascii_uppercase
    if digits_var.get():
        characters += string.digits
    if special_var.get():
        characters += string.punctuation

    password = ''.join(random.choice(characters) for _ in range(length))
    password_label.config(text=password)

root = tk.Tk()
root.title("Генератор паролей")


uppercase_var = tk.BooleanVar()
digits_var = tk.BooleanVar()
special_var = tk.BooleanVar()


uppercase_checkbox = tk.Checkbutton(root, text="Включить алфавит нижнего регистра", variable=uppercase_var)
digits_checkbox = tk.Checkbutton(root, text="Включать цифры", variable=digits_var)
special_checkbox = tk.Checkbutton(root, text="Включить спецсимволы", variable=special_var)

generate_button = tk.Button(root, text="Сгенерировать пароль", command=generate_password)

password_label = tk.Label(root, text="", font=("Helvetica", 16))

uppercase_checkbox.pack()
digits_checkbox.pack()
special_checkbox.pack()
generate_button.pack()
password_label.pack()

root.mainloop()
