# DarkGUI
from tkinter import *
import tkinter.messagebox as tmsg

root = Tk()
root.title('currency convertor-USD to INR')


def result():
    import math
    a = float(eval('74.94 * currencyvalue.get()'))
    # tmsg.askokcancel('result',eval('74.90*currencyvalue.get()'))
    tmsg.askokcancel('result', eval('a'))
    print(f'value of {currencyvalue.get()} dollars is {a} rupees.')
    exit()


currencyvalue = IntVar()
Label(text='want to convert your currency? ', font='a 14 italic').grid()  # pack(anchor=NW)
Label(text='Enter the amount in dollar:', font='a 23').grid()  # pack(side='left',anchor=NW)
Entry(textvariable=currencyvalue, relief=SUNKEN, bd=1.3, font='a 23').grid()  # pack(side='left',anchor=NW)
Button(text='Submit', command=result, font='a 23').grid()  # pack()
mainloop()
