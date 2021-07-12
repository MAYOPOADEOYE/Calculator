# Calculator
from tkinter import *

root=Tk()
root.title("Simple Calculator")
root.configure(bg="blue")


e=Entry(root,width=40,borderwidth=5)
e.grid(row=0,column=0,columnspan=3,padx=10, pady=10)

def num_click(number):
	current=e.get()
	e.delete(0,END)
	e.insert(0,str(current)+str(number))

    
def num_clear():
	e.delete(0,END)

def num_add():
	first_number=e.get()
	global first_num
	global math
	math="addition"
	first_num=int(first_number)
	e.delete(0,END)

def num_sub():
	first_number=e.get()
	global first_num
	global math
	math="subtraction"
	first_num=int(first_number)
	e.delete(0,END)

def num_div():
	first_number=e.get()
	global first_num
	global math
	math="division"
	first_num=int(first_number)
	e.delete(0,END)

def num_times():
	first_number=e.get()
	global first_num
	global math
	math="multiplication"
	first_num=int(first_number)
	e.delete(0,END)

def num_power():
	first_number=e.get()
	global first_num
	global math
	math="power"
	first_num=int(first_number)
	e.delete(0,END)

def num_root():
	first_number=e.get()
	global first_num
	global math
	math="root"
	first_num=int(first_number)
	e.delete(0,END)

def num_pie():
	first_number=e.get()
	global first_num
	global math
	math="pie"
	first_num=int(first_number)
	e.delete(0,END)

	

def num_equal():
	second_number=e.get()
	global second_num
	second_num=int(second_number)
	e.delete(0,END)
	if math=="addition":
		e.insert(0,first_num+second_num)
	if math=="subtraction":
		e.insert(0,first_num-second_num)
	if math=="division":
		e.insert(0,first_num/second_num)
	if math=="multiplication":
		e.insert(0,first_num*second_num)
	if math=="power":
		e.insert(0,first_num**second_num)
	if math=="root":
		e.insert(0,second_num**(1/first_num))
	if math=="pie":
		e.insert(0,22/7*first_num*second_num)
		




buttons_9=Button(root,text="9",padx=42,pady=20,command=lambda:num_click(9))
buttons_8=Button(root,text="8",padx=41,pady=20,command=lambda:num_click(8))
buttons_7=Button(root,text="7",padx=41,pady=20,command=lambda:num_click(7))
buttons_6=Button(root,text="6",padx=42,pady=20,command=lambda:num_click(6))
buttons_5=Button(root,text="5",padx=41,pady=20,command=lambda:num_click(5))
buttons_4=Button(root,text="4",padx=41,pady=20,command=lambda:num_click(4))
buttons_3=Button(root,text="3",padx=42,pady=20,command=lambda:num_click(3))
buttons_2=Button(root,text="2",padx=41,pady=20,command=lambda:num_click(2))
buttons_1=Button(root,text="1",padx=41,pady=20,command=lambda:num_click(1))
buttons_0=Button(root,text="0",padx=42,pady=20,command=lambda:num_click(0))
buttons_add=Button(root,text="+",padx=42,pady=20,command=num_add)
buttons_sub=Button(root,text="-",padx=43,pady=20,command=num_sub)
buttons_times=Button(root,text="*",padx=41,pady=20,command=num_times)
buttons_div=Button(root,text="/",padx=41,pady=20,command=num_div)
buttons_power=Button(root,text="^",padx=40,pady=20,command=num_power)
buttons_root=Button(root,text="sqrt",padx=36,pady=20,command=num_root)
buttons_pie=Button(root,text="pi",padx=40,pady=20,command=num_pie)
buttons_equal=Button(root,text="=",padx=90,pady=20,command=num_equal)
buttons_clear=Button(root,text="CLEAR",padx=76,pady=20,command=num_clear)



buttons_9.grid(row=1,column=0)
buttons_8.grid(row=1,column=1)
buttons_7.grid(row=1,column=2)

buttons_6.grid(row=2,column=0)
buttons_5.grid(row=2,column=1)
buttons_4.grid(row=2,column=2)

buttons_3.grid(row=3,column=0)
buttons_2.grid(row=3,column=1)
buttons_1.grid(row=3,column=2)

buttons_0.grid(row=4,column=0)
buttons_times.grid(row=4,column=1)
buttons_div.grid(row=4,column=2)

buttons_pie.grid(row=5,column=0)
buttons_power.grid(row=5,column=1)
buttons_root.grid(row=5,column=2)


buttons_add.grid(row=6,column=0)
buttons_clear.grid(row=6,column=1,columnspan=2)

buttons_sub.grid(row=7,column=0)
buttons_equal.grid(row=7,column=1,columnspan=2)








#buttons_.grid(row=1,column=0)
#buttons_9.grid(row=1,column=0)



#def drip():
	#hello="HELLO"+e.get()
	#m_label=Label(root,text=hello)
	#m_label.pack()

#buttons=Button(text=("ENTER YOUR NAME"),font=('Verdana,16'),command=drip)
#buttons.pack() 

root.mainloop()
