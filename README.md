# Tugas-python-istri
#Tugas Istri with Python


from tkinter import *


class Windowku:
    def __init__(self, win):
        self.lbl1 = Label(win, text='masukan nilai 1')
        self.lbl2 = Label(win, text='Masukan Nilai 2')
        self.lbl3 = Label(win, text='Masukan Nilai 3')
        self.lbl4 = Label(win, text='Masukan Nilai 4')
        self.lbl5 = Label(win, text='yang terbesar adalah')
        self.lbl1.place(x=60, y=50)
        self.lbl2.place(x=60, y=100)
        self.lbl3.place(x=60, y=200)
        self.lbl4.place(x=60, y=250)
        self.lbl5.place(x=60, y=301)
        self.t1 = Entry(bd=3)
        self.t2 = Entry()
        self.t3 = Entry()
        self.t4 = Entry()
        self.t5 = Entry()
        self.t1.place(x=200, y=50)
        self.t2.place(x=200, y=100)
        self.t3.place(x=200, y=200)
        self.t4.place(x=200, y=250)
        self.t5.place(x=200, y=300)
        self.b1 = Button(win, text='Cari terbesar', command=self.cari)
        self.b1.place(x=60, y=150)

    def cari(self):
        self.t5.delete(0, 'end')
        a = int(self.t1.get())
        b = int(self.t2.get())
        c = int(self.t3.get())
        d = int(self.t4.get())
        if a > b and a > c and a > d:
            hasil = (self.t1.get())
        elif b > a and b > c:
            hasil = (self.t2.get())
        elif c > a and c > b and c > d:
            hasil = (self.t3.get())
        else:
            hasil = (self.t4.get())
        self.t5.insert(END, str(hasil))


form1 = Tk()
mywin = Windowku(form1)
form1.title('Program Pertemuan 3 BSI')
form1.geometry("500x400+10+10")
form1.mainloop()
