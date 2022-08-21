# Calculator
#my first calculator

import tkinter as tk

def Cal():
    Num1 = int(text_input_1.get())
    Op = text_input_Op.get()
    Num2 = int(text_input_2.get())
    output = ""

    if Op == "+" :
        output += str(Num1+Num2)
    elif Op == "-":
        output += str(Num1-Num2)
    elif Op == "/":
        output += str(Num1/Num2)
    elif Op == "*":
        output += str(Num1*Num2)
    else :
        output += "Error"

    output_lable.configure(text=output)


window = tk.Tk()
window.title("calculator")
window.minsize(width=400, height=400)

title_label = tk.Label(text="Calculator")
title_label.pack(pady=20)

text_input_1 = tk.Entry(master=window, width=10)
text_input_1.pack(pady=5)

text_input_Op = tk.Entry(master=window, width=10)
text_input_Op.pack(pady=5)

text_input_2 = tk.Entry(master=window, width=10)
text_input_2.pack(pady=5)


work_button = tk.Button(
    master=window, text="Go", command=Cal, width=15, height=5
                        )
work_button.pack()

output_lable = tk.Label(master=window)
output_lable.pack(pady=20)

window.mainloop()
