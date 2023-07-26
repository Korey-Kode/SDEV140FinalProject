from tkinter import*
from tkinter import ttk
import random
import time
import datetime
import tkinter.messagebox

root = Tk()
root.geometry("1350x650+0+0")
root.title("King's Pizza Ordering System")
root.configure(background='black')

def Exit():
  qExit = tkinter.messagebox.askyesno("Ordering System", "Do you want to exit the system")
  if qExit > 0:
      root.destroy()
      return

def Reset():
  CustomerRef.set("")
  Tax.set("")
  SubTotal.set("")
  TotalCost.set("")
  CustomerName.set("")
  CustomerPhone.set("")
  CustomerEmail.set("")

def OrderRef():
  Refpay = random.randint(10300, 709467)
  Refpaid = ("OS" + str(Refpay))
  CustomerRef.set(Refpaid)

def CostofOrder() :
  Qty1=float(QtySausage.get())
  Qty2=float(QtyPepperoni.get())
  Qty3=float(QtyCheese.get())

  UnitPrice1 = float(UnitPriceSausage.get())
  UnitPrice2 = float(UnitPricePepperoni.get())
  UnitPrice3 = float(UnitPriceCheese.get())

  CostofPizza1 = "$", str('%.07f'%(Qty1 * UnitPrice1))
  CostofPizza2 = "$", str('%.07f'%(Qty2 * UnitPrice2))
  CostofPizza3 = "$", str('%.07f'%(Qty3 * UnitPrice3))

  CostofSausage.set(CostofPizza1)
  CostofPepperoni.set(CostofPizza2)
  CostofCheese.set(CostofPizza3)

  CostPizza1 = (Qty1 * UnitPrice1)
  CostPizza2 = (Qty2 * UnitPrice2)
  CostPizza3 = (Qty3 * UnitPrice3)

  AllCost = ( (Qty1 * UnitPrice1) + (Qty2 * UnitPrice2) + (Qty3 * UnitPrice3))
  TaxAll ="$", str('%.07f'%((AllCost) * 0.07))
  Tax.set(TaxAll)    
  SubTotalp ="$", str('%.07f'%(AllCost))
  SubTotal.set(SetTotalp)
  TotalCostp = "$", str('%.07f'%((AllCost + (AllCost) * 0.07)))
  TotalCost.set(TotalCostp)
  return

 
#=====================Variables=================================
CustomerRef=StringVar()
Tax =StringVar()
SubTotal=StringVar()
TotalCost=StringVar()
CostofPepperoni=StringVar()
CostofSausage=StringVar()
CostofCheese=StringVar()
CostofDelivery=StringVar()
CustomerName=StringVar()
CustomerPhone=StringVar()
CustomerEmail=StringVar()
TimeOfOrder=StringVar()
DateOfOrder=StringVar()
Discount=StringVar()
CostofCheese=StringVar()
CostofPepperoni=StringVar()
CostofSausage=StringVar()
UnitPriceCheese=StringVar()
UnitPricePepperoni=StringVar()
UnitPriceSausage=StringVar()
QtyCheese=StringVar()
QtyPepperoni=StringVar()
QtySausage=StringVar()
#============================================
CostofSausage.set(0)
CostofPepperoni.set(0)
CostofCheese.set(0)
UnitPriceCheese.set(0)
UnitPricePepperoni.set(0)
UnitPriceSausage.set(0)
QtyCheese.set(0)
QtyPepperoni.set(0)
QtySausage.set(0)
Discount.set(0)
TimeOfOrder.set(time.strftime("%H:%M:%S")) #Time
DateOfOrder.set(time.strftime("%m/%d/%Y"))  #Date
#===================================================================
Tops=Frame(root, width=1350, height=50,bd=16, relief="raise")
Tops.pack(side=TOP)
LF=Frame(root, width=700, height=650,bd=16, relief="raise")
LF.pack(side=LEFT)
RF=Frame(root, width=600, height=650, bd=16, relief="raise")
RF.pack(side=RIGHT)

Tops.configure(background='black')
LF.configure(background='black')
RF.configure(background='black')

LeftInsideLF=Frame(LF, width=700, height=100, bd=8, relief='raise')
LeftInsideLF.pack(side=TOP)
LeftInsideLFLF=Frame(LF, width=700, height=400, bd=8, relief='raise')
LeftInsideLFLF.pack(side=LEFT)

RightInsideLF=Frame(RF, width=604, height=200, bd=8, relief='raise')
RightInsideLF.pack(side=TOP)
RightInsideLFLF=Frame(RF, width=306, height=400,bd=8, relief="raise")
RightInsideLFLF.pack(side=LEFT)
RightInsideRFRF=Frame(RF, width=300, height=400,bd=8, relief="raise")
RightInsideRFRF.pack(side=RIGHT)
#=======================Title======================
lblInfo = Label(Tops, font=('arial',50, 'bold'),text="Kings Pizza Ordering System", bd=10, anchor='w')
lblInfo.grid(row=0, column=0)

#============================Top Left Frame=========================

lblCustomerName = Label (LeftInsideLF,font=('arial',14,'bold'), text="CustomerName",
                      fg="black", bd=10, anchor="w")
lblCustomerName.grid(row=0, column=0)
txtCustomerName= Entry(LeftInsideLF,font=('arial',14,'bold'), bd=20, width=43,
                     bg="white", justify='left', textvariable=CustomerName)
txtCustomerName.grid(row=0, column=1)

lblCustomerPhone = Label (LeftInsideLF,font=('arial',14,'bold'), text="CustomerPhone",
                      fg="black", bd=10, anchor="w")
lblCustomerPhone.grid(row=1, column=0)
txtCustomerPhone = Entry(LeftInsideLF,font=('arial',14,'bold'), bd=20, width=43,
                     bg="white", justify='left', textvariable=CustomerPhone)
txtCustomerPhone.grid(row=1, column=1)

lblCustomerEmail = Label (LeftInsideLF,font=('arial',14,'bold'), text="CustomerEmail",
                      fg="black", bd=10, anchor="w")
lblCustomerEmail.grid(row=2, column=0)
txtCustomerEmail = Entry(LeftInsideLF,font=('arial',14,'bold'), bd=20, width=43,
                     bg="white", justify='left', textvariable=CustomerEmail)
txtCustomerEmail.grid(row=2, column=1)
#================================Top Right Frame==========================================
lblDateofOrder = Label(RightInsideLF,font=('arial',14,'bold'), text="DateOfOrder",
                      fg="black", bd=10, anchor="w")
lblDateofOrder.grid(row=0, column=0)
txtDateofOrder= Entry(RightInsideLF,font=('arial',14,'bold'), bd=20, width=43,
                     bg="white", justify='left', textvariable=DateOfOrder)
txtDateofOrder.grid(row=0, column=1)

lblTimeofOrder = Label(RightInsideLF,font=('arial',12,'bold'), text="TimeOfOrder",
                      fg="black", bd=10, anchor="w")
lblTimeofOrder.grid(row=1, column=0)
txtTimeofOrder= Entry(RightInsideLF,font=('arial',12,'bold'), bd=20, width=43,
                     bg="white", justify='left', textvariable=TimeOfOrder)
txtTimeofOrder.grid(row=1, column=1)

lblCustomerRef = Label(RightInsideLF,font=('arial',12,'bold'), text="Customer Ref",
                      fg="black", bd=10, anchor="w")
lblCustomerRef.grid(row=2, column=0)
txtCustomerRef= Entry(RightInsideLF,font=('arial',12,'bold'), bd=20, width=43,
                     bg="white", justify='left', textvariable=CustomerRef)
txtCustomerRef.grid(row=2, column=1)

#==========================Bottom Frame======================================
lblMethodOfPayment=Label (RightInsideLFLF, font=('arial',12,'bold'), text="Method of Payment",
                          fg="black", bd=16, anchor="w")
lblMethodOfPayment.grid(row=0, column=0)
cmdMethodOfPayment=ttk.Combobox(RightInsideLFLF, font=('arial',10,'bold'))
cmdMethodOfPayment['value']=('','Cash','Debit Card','Visa Card','MasterCard',)
cmdMethodOfPayment.grid(row=0, column=1)
lblDiscount= Label(RightInsideLFLF, font=('arial',12,'bold'),text="Discount",
                        fg="black", bd=16, anchor='w')
lblDiscount.grid(row=1, column=0)
txtDiscount = Entry(RightInsideLFLF,font=('arial', 12,'bold'), bd=16, width=18, bg="white",
                          justify = 'left',textvariable=Discount)
txtDiscount.grid(row=1, column=1)

lblTax = Label(RightInsideLFLF, font=('arial',12, 'bold'), text="Tax",
                    fg="black", bd=16, anchor='w')
lblTax.grid(row=2, column=0)
txtTax = Entry(RightInsideLFLF, font=('arial',12,'bold'), bd=16, width=18,
                    bg="white", justify = 'left', textvariable=Tax)
txtTax.grid(row=2,column=1)

lblSubTotal = Label(RightInsideLFLF, font=('arial',12,'bold'), text="Sub Total",
                          fg="black", bd=16, anchor='w')
lblSubTotal.grid(row=3, column=0)
txtSubTotal = Entry(RightInsideLFLF, font=('arial',12, 'bold'), bd=16, width=18,
                          bg="white", justify = 'left', textvariable=SubTotal)
txtSubTotal.grid(row=3, column=1)

lblTotalCost = Label(RightInsideLFLF, font=('arial',12, 'bold'),text="Total Cost",
                          fg="black", bd=16, anchor='w')
lblTotalCost.grid(row=4, column=0)
txtTotalCost = Entry(RightInsideLFLF, font=('arial',12,'bold'), bd=16, width=18,
                          bg="white", justify='left',textvariable=TotalCost)
txtTotalCost.grid(row=4, column=1)

#===============

lblSausage = Label(LeftInsideLFLF, font=('arial',14,'bold'),text="Sausage",fg="black",bd=20)
lblSausage.grid(row=1, column=0)
lblPepperoni = Label(LeftInsideLFLF, font=('arial',14,'bold'),text="Pepperoni",fg="black",bd=20)
lblPepperoni.grid(row=2, column=0)
lblCheese = Label(LeftInsideLFLF, font=('arial',14,'bold'),text="Cheese",fg="black",bd=20)
lblCheese.grid(row=3, column=0)

#=====

txtQtySausage = Entry(LeftInsideLFLF, font=('arial', 12,'bold'),bd=20, width=16,
                          bg="white", justify='left',textvariable=QtySausage)
txtQtySausage.grid(row=1, column=1)
txtQtyPepperoni = Entry(LeftInsideLFLF, font=('arial', 12,'bold'),bd=20, width=16,
                          bg="white", justify='left',textvariable=QtyPepperoni)
txtQtyPepperoni.grid(row=2, column=1)
txtQtyCheese = Entry(LeftInsideLFLF, font=('arial', 12,'bold'),bd=20, width=16,
                          bg="white", justify='left',textvariable=QtyCheese)
txtQtyCheese.grid(row=3, column=1)

#====

txtUnitPriceSausage = Entry(LeftInsideLFLF,font=('arial', 12, 'bold'), bd=20, width=16,
                              bg="white", justify= 'left', textvariable=UnitPriceSausage)
txtUnitPriceSausage.grid(row=1, column=2)
txtUnitPricePepperoni = Entry(LeftInsideLFLF,font=('arial', 12, 'bold'), bd=20, width=16,
                              bg="white", justify= 'left', textvariable=UnitPricePepperoni)
txtUnitPricePepperoni.grid(row=2, column=2)
txtUnitPriceCheese = Entry(LeftInsideLFLF,font=('arial', 12, 'bold'), bd=20, width=16,
                              bg="white", justify= 'left', textvariable=UnitPriceCheese)
txtUnitPriceCheese.grid(row=3, column=2)

#====

txtCostofSausage = Entry(LeftInsideLFLF, font=('arial', 12, 'bold'), bd=20, width=16,
                         bg="white", justify='left',textvariable=CostofSausage)
txtCostofSausage.grid(row=1, column=3)
txtCostofPepperoni = Entry(LeftInsideLFLF, font=('arial', 12, 'bold'), bd=20, width=16,
                         bg="white", justify='left',textvariable=CostofPepperoni)
txtCostofPepperoni.grid(row=2, column=3)

txtCostofCheese = Entry(LeftInsideLFLF, font=('arial', 12, 'bold'), bd=20, width=16,
                         bg="white", justify='left',textvariable=CostofCheese)
txtCostofCheese.grid(row=3, column=3)

#Bottom Left Frame
lblItemOrder = Label (LeftInsideLFLF, font=('arial',14, 'bold'), text="Item Order", fg="black",bd=20)
lblItemOrder.grid(row=0, column=0)
lblQty = Label (LeftInsideLFLF, font=('arial',14, 'bold'), text="Qty", fg="black",bd=20)
lblQty.grid(row=0, column=1)
lblUnitPrice = Label (LeftInsideLFLF, font=('arial',14, 'bold'), text="Unit Price", fg="black",bd=20)
lblUnitPrice.grid(row=0, column=2)
lblCostofItem = Label (LeftInsideLFLF, font=('arial',14, 'bold'), text="Cost of Item", fg="black",bd=20)
lblCostofItem.grid(row=0, column=3)
           
#Buttons Right Frame
btnTotalCost=Button(RightInsideRFRF, pady=8, bd=8, fg="black", font=('arial',16,'bold'), width=11,
                    text="Total Cost", bg="white", command=CostofOrder).grid(row=0, column=0)
btnReset=Button(RightInsideRFRF, pady=8, bd=8, fg="black", font=('arial',16,'bold'), width=11,
                    text="Reset", bg="white", command=Reset).grid(row=1, column=0)
btnOrderRef=Button(RightInsideRFRF, pady=8, bd=8, fg="black", font=('arial',16,'bold'), width=11,
                    text="Order Ref", bg="white", command=OrderRef).grid(row=2, column=0)
btnClose=Button(RightInsideRFRF, pady=8, bd=8, fg="black", font=('arial',16,'bold'), width=11,
                    text="Close", bg="white", command=Exit).grid(row=3, column=0)
root.mainloop()
