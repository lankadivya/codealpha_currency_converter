#import libraries 
import tkinter as tk

from tkinter import *

from tkinter import ttk

from forex_python.converter import CurrencyRates,CurrencyCodes


#creating GUI 
root = tk.Tk()
root.title('Currency Converter')
root.geometry('500x650')
root['bg']='gray81'

 
#creating variable
variable1 = tk.StringVar(root)
variable2 = tk.StringVar(root)


#setting variables 
variable1.set("choose currency")
variable2.set("choose currency")


#Creating Header 
lbl_txt = Label(root,text = 'Currency Converter',font=("Time New Roman",'18','bold'),bg='gray81')
lbl_txt.place(x=135)


#Function for currency conversion
def currencyconversion():
    c= CurrencyRates()

    from_currency = variable1.get()
    to_currency = variable2.get()
    
    convert_amount = c.convert(from_currency,to_currency,float(sor_amount.get()))
    new_amount = float("{:.4f}".format(convert_amount))
    des_amount.insert(0,str(new_amount))
    return des_amount


#Function for clearing all values
def clear_all():
    sor_amount.delete(0,tk.END)
    des_amount.delete(0,tk.END)


#creating label Amount 
lbl_txt = Label(root,text="Amount             :",font=("Helvetica",'15','bold'),bg='gray81')
lbl_txt.place(x=50,y=60)


#Taking value from user
sor_amount = tk.Entry(root,font=('Helvetica','18','bold'),bg='White')
sor_amount.place(x=220,y=65,height= 25,width = 200) 


#list of currencies
list= ["INR", "USD", "CAD", "CNY", "DKK", "EUR"]


#Creating label from currency 
lbl_txt = tk.Label(root,text="From Currency :",font=("Helvetica",'15','bold'),bg='gray81')
lbl_txt.place(x=50,y=100)


#Creating label to currency 
lbl_txt = tk.Label(root,text="To Currency     :",font=("Helvetica",'15','bold'),bg='gray81')
lbl_txt.place(x=50,y=140)


#Creating label Converted amount 
lbl_txt=tk.Label(root,text="Converted Amo:",font=("Helvetica",15,'bold'),bg='Gray81')
lbl_txt.place(x=50,y=240) 
des_amount=Entry(root,font=('Helvetica','15','bold'),bg='white')
des_amount.place(x=220,y=240,height=25,width=200)


FromCurrency_option = tk.OptionMenu(root,variable1, *list)
ToCurrency_option = tk.OptionMenu(root, variable2, *list)
 

FromCurrency_option.place(x=270,y=105,height=25,width=150)
ToCurrency_option.place(x=270,y=140,height=25,width=150)


#Convert button
Btn1 = Button(root,text="Convert",font=("Helvetica",'18','bold'),bg='darkslategray3',command= currencyconversion)
Btn1.place(x=120,y=190,height = 30,width = 120)


#Clear all button 
Btn2 = Button(root,text="Clear All",font=("Helvetica",'18','bold'),bg='darkslategray3',command=clear_all)
Btn2.place(x=120,y=280,height = 30,width = 120)


root.mainloop()