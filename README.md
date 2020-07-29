# Tkinter-PROJECT-1-REGISTRATION-WINDOW-
This project is basically a template for Registration Form. I have used Tk toolkit in tkinter python module.
#==============CONCERT REGISTRATION FORM===========================================
from tkinter import*
from PIL import Image, ImageTk
from tkinter import ttk
#================================defining my window========================================
root=Tk()
root.title("Registration Window")
root.geometry("1350x700+0+0")
root.config(bg="white")
#=======================================Background Image==================================
image=Image.open("C:\\Users\\acer\\Downloads\\anu.jpg")
backgroundimage=ImageTk.PhotoImage(image)
imagelabel=Label(root, image=backgroundimage).place(x=250, y=0, relwidth=1, relheight=1)
#======================================left image=========================================
aboveimage=Image.open("C:\\Users\\acer\\Downloads\\ff.jpg")
abimage=ImageTk.PhotoImage(aboveimage)
imagelabel=Label(root, image=abimage).place(x=200, y=120, width=400, height=500)

#=====================================frame for the form===============================================
formframe=Frame(root, bg="white")
formframe.place(x=600, y=120, width=700, height=500)

#==========================Title in frame==============================================================
title=Label(formframe, text="REGISTER HERE", font=("times new roman",20,"bold"),
            bg="white",fg="green").place(x=50,y=20)
#======================first name label and entry=======================================================
f_name=Label(formframe, text="First Name", font=("times new roman",15,"bold"),
            bg="white",fg="grey").place(x=50,y=100)
entry_fname=Entry(formframe, font=("times new roman",15), bg="lightgray").place(x=50, y=130, width=250)
#==============================contact info=============================================================
contact=Label(formframe, text="Contact Number", font=("times new roman",15,"bold"),
            bg="white",fg="grey").place(x=50,y=180)
entry_contact=Entry(formframe, font=("times new roman",15), bg="lightgray").place(x=50, y=210, width=250)
#=============================Last name Label and Entry===================================================
l_name=Label(formframe, text="Last Name", font=("times new roman",15,"bold"),
            bg="white",fg="grey").place(x=370,y=100)
entry_lname=Entry(formframe, font=("times new roman",15), bg="lightgray").place(x=370, y=130, width=250)
#==============================contact info===============================================================
email=Label(formframe, text="Email Address", font=("times new roman",15,"bold"),
            bg="white",fg="grey").place(x=370,y=180)
entry_email=Entry(formframe, font=("times new roman",15), bg="lightgray").place(x=370, y=210, width=250)
#==============================Security Question===============================================================
security_ques=Label(formframe, text="Security Question", font=("times new roman",15,"bold"),
            bg="white",fg="grey").place(x=50,y=260)
security_ques=ttk.Combobox(formframe, font=("Times new roman", 14), state="readonly", justify=CENTER)
security_ques['values']=("Select", "Your pet name", "Your cousin name", "Your best friends name")
security_ques.place(x=50,y=290)
security_ques.current(0)
#============================== Your Answer===============================================================
your_ans=Label(formframe, text="Your Answer", font=("times new roman",15,"bold"),
            bg="white",fg="grey").place(x=370,y=260)
your_ans=Entry(formframe, font=("times new roman",15), bg="lightgray").place(x=370, y=290, width=250)
#==========================Password label and entry======================================================
password=Label(formframe, text="Password", font=("times new roman",15,"bold"),
            bg="white",fg="grey").place(x=50,y=340)
entry_password=Entry(formframe, font=("times new roman",15), bg="lightgray").place(x=50, y=370, width=250)
#==============================Confirm Password label and entry===========================================
confirm_password=Label(formframe, text="Confirm Password", font=("times new roman",15,"bold"),
            bg="white",fg="grey").place(x=370,y=340)
your_ans=Entry(formframe, font=("times new roman",15), bg="lightgray").place(x=370, y=370, width=250)
#==============================Check Button for Terms & Conditions========================================
terms_chek=Checkbutton(formframe, text="I Agree The Terms & Conditions.", onvalue=1, offvalue=0, bg="white", font=("times new roman", 13, "bold")).place(x=50, y=400)
#===============================Register button===========================================
#btn_image=Image.open("C:\\Users\\acer\\Downloads\\btn.jpg")
#btn=ImageTk.PhotoImage(btn_image)
btn1=Button(formframe, text="Register Now", bg="darkgreen", font=("Times new roman", 15), fg="black", cursor="hand2").place(x=50, y=430, width=250)
login=Button(root, text="LOGIN", bg="white", font=("Times new roman", 15), fg="black", cursor="hand2").place(x=300, y=500, width=150)
title_label=Label( text="Copyright@MeghnaSrivastava 2020, 29th July", background="black", foreground="white",padx=340, pady=4, font="Verdana 10 bold", borderwidth=3, relief=SUNKEN)
title_label.pack(side=BOTTOM,fill="y")
f1=Label(root,text="WELCOME", font=("times new roman", 30,"bold"),fg="white", bg="black", bd=0)
f1.pack(side=TOP, fill="x")
root.mainloop()
