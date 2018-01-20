#---Project---#

# Import the libraries
import tkinter as tk
import tkinter.messagebox
from tkinter import ttk
import tkinter.messagebox as msg
from time import sleep as sl

def main_func():

    # Main window
    main=tk.Tk()
    main.title('Hotel Management System v1.0')
    main.attributes('-fullscreen', True)
    #main.geometry("1366x768")
    main.config(bg="#70a6ff")


    # Headings
    tk.Label(main,text='Hotel Management System', fg="#444444", bg='#70a6ff', font="Verdana 50 bold") .place(x=175, y=100)
    tk.Label(main,text='SEMESTER PROJECT', fg="#444444", bg='#70a6ff', font="Verdana 12 underline") .place(x=1025, y=170)
    #tk.Label(main,text='By Hassan',fg="#444444", bg='#70a6ff', font="Verdana 18 bold") .place(x=500, y=200)


    # Function to call admin.py
    def admin():
        root_admin=tk.Tk()
        root_admin.title("ADMIN")
        root_admin.geometry("1366x786")
        root_admin.config(bg="#70a6ff")
        def  admin_exit():
            root_admin.destroy()
            #FOR ADMIN TO SEE WHICH ROOMS ARE RESERVED
        def booked_rooms():
            root_bookedrooms=tk.Tk()
            root_bookedrooms.title("BOOKED ROOMS")
            root_bookedrooms.geometry('1366x786')
            root_bookedrooms.config(bg="#70a6ff")
            def save_1():
                FileHandle=open("database/Guests.TXT","r")
                tk.Label(root_bookedrooms,text=FileHandle.read(),width=30).place(x=550,y=10)
                FileHandle.close()
            tk.Button(root_bookedrooms,text="DISPLAY",width=20,command=save_1).place(x=100,y=50)    
            def booked_roomsexit():
                root_bookedrooms.destroy()
            tk.Button(root_bookedrooms,text="BACK",width=20,command=booked_roomsexit).place(x=100,y=100)    
                
            #FOR ADMIN TO SEE WHICH PARKING SLOTS ARE FILLED
        def booked_slots():
            root_bookedslots=tk.Tk()
            root_bookedslots.title('BOOKED SLOTS')
            root_bookedslots.geometry('1366x786')
            root_bookedslots.config(bg="#70a6ff")
            def save_2():
                FileHandle=open("database/parking/carnumbers.TXT","r")
                tk.Label(root_bookedslots,text=FileHandle.read(),width=30).place(x=550,y=10)
                FileHandle.close()
            tk.Button(root_bookedslots,text="DISPLAY",width=20,command=save_2).place(x=100,y=50)    
            def booked_slotsexit():
                root_bookedslots.destroy()
            tk.Button(root_bookedslots,text="BACK",width=20,command=booked_slotsexit).place(x=100,y=100)    

        #FOR ADMIN TO SEE THE FEEDBACK OF PEOPLE ABOUT HOTEL
                
        def read_comments():
            root_readcomment=tk.Tk()
            root_readcomment.title('FEEDBACK')
            root_readcomment.geometry('1366x786')
            root_readcomment.config(bg="#70a6ff")
            def save_3():
                FileHandle=open("database/comments.TXT","r")
                tk.Label(root_readcomment,text=FileHandle.read(),width=30).place(x=550,y=10)
                FileHandle.close()
            tk.Button(root_readcomment,text="DISPLAY",width=20 ,command=save_3).place(x=100,y=50)   
            def readcomment_exit():
                root_readcomment.destroy()
            tk.Button(root_readcomment,text="BACK",width=20 ,command=readcomment_exit).place(x=100,y=100)

            
        tk.Label(root_admin, text='Admin Area', bg="#70a6ff",font='Verdana 40 bold').place(x=100, y=40)
        tk.Label(root_admin, text='Version 1.0',bg="#70a6ff").place(x=440, y=100)  
        tk.Button(root_admin,text="BOOKED ROOMS",width=35,height=2,command=booked_rooms).place(x=550,y=200)
        tk.Button(root_admin,text="BOOKED SLOTS",width=35,height=2,command=booked_slots).place(x=550,y=250)
        tk.Button(root_admin,text="FEEDBACKS",width=35,height=2,command=read_comments).place(x=550,y=300)
        tk.Button(root_admin,text="BACK",width=35,height=2,command=admin_exit).place(x=550,y=350)
        tk.Label(root_admin, text='© All rights reserved Haosqu',bg="#70a6ff").place(x=580, y=600)  




        
        # Function to call user.py
    def user_func(n):
        if n == 1:
            main.destroy()
        user=tk.Tk()
        user.attributes('-fullscreen', True)
        user.title("USER")
        user.geometry("1366x786")
        user.config(bg="#70a6ff")
        def room_booking():
            user.destroy()
            roombook=tk.Tk()
            roombook.attributes('-fullscreen', True)
            roombook.title("ROOMS RESRVATION")
            roombook.geometry("1366x786")
            roombook.config(bg="#70a6ff")
            def roomnumber():             
                
         # This reads the file for room numbers
                FileHandle = open("database/Room numbers.TXT", "r")
                rooms = int(FileHandle.readline())
                FileHandle.close()
                n = name.get()
                n += "\n"
                ph = phone.get()
                ph += "\n"
                e = email.get()
                e += "\n"

                 # This confirms the reservation of the room
                if name.get() and phone.get() and email.get():
                     confirm=tkinter.messagebox.askyesno('Confirmation of Reservation', 'Are you sure you want to reserve the room?')
                     nameEntry.delete("0", 'end')
                     phoneEntry.delete("0", 'end')
                     emailEntry.delete("0", 'end')
                     if confirm==True:
                          no = ('00' + str(201 - rooms))
                          message = ('Thank you for your reservation. Your room number is ' + no)
                          tk.Label(roombook, text=message, font='Verdana 20', bg='#70a6ff').place(x=460,y=400)
                          rooms -= 1
                          FileHandle = open("database/Room numbers.TXT", "w")
                          FileHandle.write(str(rooms)+"\n")
                          FileHandle.close()
                          FileHandle = open("database/Guests.TXT", "a")
                          FileHandle.write("Room number " + str(no) + "\n")
                          FileHandle.write("Name: " + n)
                          FileHandle.write("Phone: " + ph)
                          FileHandle.write("Email: " + e)
                          FileHandle.close()
                     else:
                          tk.Label(roombook, text='We feel sad to see you go like this.', font='Verdana 20', bg='#70a6ff').place(x=560,y=400)
                          tk.Label(roombook, text='If you want to book the room, please exit and enter into the portal again.', font='Verdana 14', bg='#70a6ff').place(x=480,y=430)
                else:
                     tkinter.messagebox.showerror('Error!', 'Please enter all the details to continue.')
            # Labels
            tk.Label(roombook, text='Room Booking System', fg='#444444', bg='#70a6ff',font='Verdana 40 bold').place(x=500,y=60)
            name=tk.Label(roombook, text='Name:', bg='#70a6ff').place(x=560,y=160)
            pnumber=tk.Label(roombook, text='Phone #', bg='#70a6ff').place(x=560,y=200)
            email=tk.Label(roombook, text='E-Mail:', bg='#70a6ff').place(x=560,y=240)

            name = tk.StringVar()
            phone = tk.StringVar()
            email = tk.StringVar()

            # Entry Boxes
            nameEntry=tk.Entry(roombook, width=20, bg='#e2e2e2', textvariable = name)
            nameEntry.place(x=700,y=160)
            phoneEntry=tk.Entry(roombook, width=20, bg='#e2e2e2', textvariable=phone)
            phoneEntry.place(x=700,y=200)
            emailEntry=tk.Entry(roombook, width=20, bg='#e2e2e2', textvariable = email)
            emailEntry.place(x=700,y=240)
            tk.Button(roombook)


            # Submit and Exit Buttonss
            def resetRoomNumber():
                     FileHandle= open("database/Room numbers.TXT", "w")
                     FileHandle.write("200\n")
                     FileHandle.close
                     FileHandle = open("database/Guests.TXT", "w")
                     FileHandle.close()
            def exit():
                 confirm=tkinter.messagebox.askyesno('Are you sure?', 'Are you sure you want to exit?')
                 if confirm==True:
                     roombook.destroy()
                     user_func(0)
                

            tk.Button(roombook, text='Submit', bg='#70a6ff', command=roomnumber).place(x=680,y=310)
            tk.Button(roombook, text='Exit', bg='#70a6ff', command=exit).place(x=690,y=350)
            tk.Button(roombook, text="Reset", bg='#70a6ff', command=resetRoomNumber).place(x=1, y=1)
            roombook.config(bg='#70a6ff')
                           








            
        def parking():
            parking=tk.Tk()
            parking.title('Parking Lot')
            parking.attributes('-fullscreen', True)
            parking.configure (bg='#70a6ff')

            ### ========= LEFT ========= ###
            tk.Label(parking, text='Parking Slot', font='Verdana 50 bold', bg='#70a6ff').place(x=100, y=40)
            
            tk.Label(parking, text='Park Your Car', font='Verdana 35 underline', bg='#70a6ff').place(x=400, y=160)
            
            parkinst=tk.Label(parking, text="Enter you Car Number and press the 'Submit' button to get a\ntoken for Parking Slot.", bg='#70a6ff', fg='white' ,font='Verdana 18 bold')
            parkinst.place(x=200, y=220)
         
            def my_no():
                # Reads the text file for the total car slots available
                FileHandle=open("database/parking/carslots.TXT",'r')
                slots=int(FileHandle.readline())
                FileHandle.close()
                c=carno.get()
                c +="\n"
                if car_no.get(): # This checks if the entry box is filled or not

                    # This shows a confirmation box to ensure the parking
                    confirm=tkinter.messagebox.askyesno('Confirmation of Reservation', 'Are you sure to want to park your car?')
                    car_no.delete("0",'end')
                    
                    # If the user confirms, this code runs
                    if confirm==True:
                        nop = (str(201-slots))
                        message=('Thank you for your reservation.\n Your slot number is '+nop)
                        tk.Label(parking, text=message, font='Verdana 20', bg='#70a6ff').place(x=360,y=480)
                        slots-=1
                        FileHandle= open('database/parking/carslots.TXT','w')
                        FileHandle.write(str(slots)+"\n")
                        FileHandle.close()
                        FileHandle=open("database/parking/carnumbers.TXT","a")
                        FileHandle.write('Slot Number: '+ str(nop)+'\n')
                        FileHandle.write('Car Number: ' +c )
                        FileHandle.close()
                    
                # If the entry box is empty, then this code runs
                else:
                    tkinter.messagebox.showerror('Error!', 'Please enter your car number to continue.')
                    

            # Main entry widget
            tk.Label(parking, text='Car Number:', font='Verdana 16', bg='#70a6ff').place(x=400, y=310)
            carno = tk.StringVar()
            
            car_no=tk.Entry(parking, width=15, textvariable=carno)
            car_no.place(x=520, y=307)
            
            
            # Submit button for the parking number
            submit_btn=tk.Button(parking, text='Submit', width=10, command=my_no)
            submit_btn.place(x=470, y=370)
            
            # Exit button of the parking window
            def exit_parking():
                confirm=tkinter.messagebox.askyesno('Are you sure?', 'Are you sure you want to exit?')
                if confirm==True:
                    parking.destroy()

            tk.Button(parking, text='Back', width=10, command=exit_parking) .place(x=470, y=420)

            line=tk.Label(parking, text='|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|\n|', bg='#70a6ff', font='Verdana 20 bold')
            line.place(x=1000, y=100)


            ### ========= Right ========= ###
            tk.Label(parking, text='Other Services', font='Verdana 35 underline', bg='#70a6ff').place(x=1100, y=160)

            tk.Button(parking, text='Book A Room', width=10, command=room_booking) .place(x=1180, y=250)
            tk.Button(parking, text='Give Feedback', width=10, command=feedback) .place(x=1180, y=350)
            tk.Button(parking, text='Leave A Query', width=10, command=queries) .place(x=1180, y=450)
            tk.Button(parking, text='Back To Main', width=10, command=user) .place(x=1180, y=550)


            parking.mainloop()



        def queries ():
            qrs = tk.Tk()
            qrs.title('Queries')
            qrs.attributes('-fullscreen', True)
            qrs.config( bg = "#70a6ff" )
                    
            #Scrollbar
            bar = tk.Scrollbar(qrs) .pack( side = 'right', fill = 'y' )

            # Function for design
            def design():
                tk.Label(qrs,text='...',fg="purple", bg = "#70a6ff", font="Times 25 bold") .pack()
                
            #Function for Exit
            def exit_qrs():
                qrs.destroy()

            #Function for Customer Satifaction Dialoguebox
            def satisfaction():
                stf = msg.askyesno("Customer Satisfaction", "Please tell us if you are satisfied or not." )

                if stf == True:
                    thnks = msg.showinfo("CafeCliche", "Thank-you for your trust in us.")
                    sl(0.7)
                    qrs.destroy()

                if stf == False:
                    msg.showinfo("Customer Satisfaction", "Please register your Complaints at the following number:\n                              0303-5220280")
                    sl(1)
                    

            # Email Message box
            def emailbox():
                msg.showinfo("Our Email Address", "Our E-Mail address is \ncafecliche_isb@gmail.com" )

            #Phone Message box
            def phone():
                msg.showinfo("Contact us", "Our Phone number is \n      0303-5220280")
                
            # ***** Start *****

            lbl_hi = tk.Label( qrs, text = 'Hi !', font='Times 28', fg = 'purple', bg = "#70a6ff" ) .pack()

            design()

            lbl1 = tk.Label(qrs, text='We welcome your queries and \nWe are always willing to answer your questions \nAnd resolve your problems \nThank You!', font='Times 20', fg = 'purple', bg = "#70a6ff").pack()

            design()

            lbl1 = tk.Label(qrs, text="Press the button below to show the Email Address for queries", font='Times 20', fg = 'purple', bg = "#70a6ff" ).pack()

            design()

            btn1 = tk.Button(qrs, text ='Our E-Mail Address', bg='#70a6ff', state = 'active' , command = emailbox ) .pack()

            design()

            btn2 = tk.Button(qrs, text ='Our Phone Number', bg='#70a6ff', state = 'active', command = phone ) .pack()

            

            btn3 = tk.Button(qrs, text ='Back', bg='#70a6ff', state = 'active', command = satisfaction ) .place(x=660,y=525)

            design()

            #Last Things

            lbl_end = tk.Label(qrs, text="All rights reserved ©", font='Times 12', fg = 'black', bg = "#70a6ff").pack( padx = 5, pady = 4 , side = 'bottom' )

            #ProgressBar
            pb = ttk.Progressbar(qrs, orient="horizontal", length=200, mode="determinate")
            pb.pack( padx = 5, pady = 5, side = 'bottom' )
            pb.start()
            
            
        def feedback ():
            user.destroy()
            fbk = tk.Tk()
            fbk.title('Feedback')
            fbk.attributes('-fullscreen', True)

            #fbk.geometry('1366x768')

            #Scrollbar
            bar = tk.Scrollbar(fbk) .pack( side = 'right', fill = 'y' )

            # Function for design
            def design():
                tk.Label( fbk, text='...',fg="purple",bg='#70a6ff',font="Times 25 bold") .pack()

            #Function for Exiting Feedback
            def exit_fbk():
                user_func(0)
                fbk.destroy()

            def saveComment():
                    n = name.get()
                    n += "\n"
                    e = email.get()
                    e += "\n"
                    c = comments.get()
                    c += "\n"
                    FileHandle = open("database/comments.TXT", "a")
                    FileHandle.write(n)
                    FileHandle.write(e)
                    FileHandle.write(c)
                    FileHandle.close()
                
            #Function for Rating
            def rate():              
                rt = tk.Tk()
                rt.title("Rate US!")
                rt.geometry('700x500')
                
                #Function for Exiting Rating
                def exit_rt():
                    rt.destroy()
                    

                #rate_var =tk.IntVar()

                rtlbl1 = tk.Label( rt, text = 'Please rate us according to your experience', font='Times 28', fg = 'purple') .pack()
                rtlbl2 = tk.Label( rt, text = 'Thank you!', font='Times 28', fg = 'purple') .pack()

                tk.Radiobutton( rt, text="1",  value=1) .place( x = 270, y = 130 )
                tk.Radiobutton( rt, text="Worst",  value=1) .place( x = 370, y = 130 )

                tk.Radiobutton( rt, text="2",  value=2 ) .place( x = 270, y = 160 )
                tk.Radiobutton( rt, text="Bad",  value=2 ) .place( x = 370, y = 160 )

                tk.Radiobutton( rt, text="3",  value=3 ) .place( x = 270 , y = 190 )
                tk.Radiobutton( rt, text="Satisfactory",  value=3 ) .place( x = 370, y = 190 )

                tk.Radiobutton( rt, text="4",  value=4 ) .place( x = 270, y = 220 )
                tk.Radiobutton( rt, text="Good",  value=4 ) .place( x = 370, y = 220 )
                
                tk.Radiobutton( rt, text="5",  value=5 ) .place( x = 270, y = 250 )
                tk.Radiobutton( rt, text="Excellent",  value=5 ) .place( x = 370, y = 250 )

                tk.Button( rt, text='Back', bg='#70a6ff', state = 'active' , command = exit_rt ) .place( x = 320, y = 300 ) 

            # ***** Start *****

            lbl_hi1 = tk.Label( fbk, text = 'Hi !', font='Times 28',bg='#70a6ff', fg = 'purple') .pack()

            lbl01 = tk.Label(fbk, text='We love to hear feedbacks from our dear customers.',bg='#70a6ff', font='Times 22', fg = 'purple').pack()

            design()

            lbl02 = tk.Label( fbk, text='Please press the button below to rate our Cafe.',bg='#70a6ff', font='Times 20', fg = 'purple').pack()

            btnn1 = tk.Button( fbk, text='Rate Us!', bg='#70a6ff', state = 'active' , command = rate ) .pack()

            design()

            lbl03 = tk.Label( fbk, text='Or Please give us your precious comments', bg='#70a6ff', font='Times 20', fg = 'purple').pack()

            # Name, Comments and Entries

            name = tk.StringVar()
            email = tk.StringVar()
            comments = tk.StringVar()


            name_lbl = tk.Label(fbk, text= "Name: ", font='Times 15', bg='#70a6ff', fg = 'purple') .place( x = 400, y = 350)
            nameEntry=tk.Entry(fbk, width=20, bg='#e2e2e2', textvariable = name )
            nameEntry.place(x=700,y=350)

            email_lbl = tk.Label(fbk, text= "E-Mail: ", font='Times 15', bg='#70a6ff', fg = 'purple') .place( x = 400, y = 450)
            emailEntry=tk.Entry(fbk, width=20, bg='#e2e2e2', textvariable = email )
            emailEntry.place(x=700,y=450)

            comment_lbl = tk.Label(fbk, text= "Comments: ", font='Times 15', bg='#70a6ff', fg = 'purple') .place( x = 400, y = 550)
            commentEntry=tk.Entry(fbk, width=50, bg='#e2e2e2', textvariable = comments)
            commentEntry.place(x=700,y=550)


            btnn2 = tk.Button( fbk, text='Back', bg='#70a6ff', state = 'active' , command = exit_fbk ) .place( x = 700, y = 630 )


            #Last things
            lbl_end1 = tk.Label( fbk, text="All rights reserved ©", font='Times 12', bg='#70a6ff', fg = 'black').pack( padx = 5, pady = 4 , side = 'bottom' )

            #ProgressBar
            pb1 = ttk.Progressbar(fbk, orient="horizontal", length=200, mode="determinate")
            pb1.pack( padx = 5, pady = 5, side = 'bottom' )
            pb1.start()
            tk.Button(fbk, text="Submit", state = 'active', bg='#70a6ff', command=saveComment).place(x = 620 , y = 630 )
            fbk.configure(bg='#70a6ff')
        def about_us():
            about_us = tk.Tk()
            about_us.title('ABOUT US')
            about_us.geometry('1366x786')
            about_us.config(bg="#70a6ff")
            tk.Label(about_us, text='Hi! \nCafe Cliché has established itself as one of the world’s leading hospitality brands \noffering quality accommodation, unique holiday and conference solutions, \ncultural heritage and adventure tourism. \n Its collection of 35 unique hotels, resorts, safari lodges and camps, palaces and forts \nlocated in East Africa (Kenya, Tanzania, Zanzibar, Rwanda, Uganda), Mozambique \nand Southern Asia (Pakistan, Afghanistan and Tajikistan) \nare in some of the world’s most interesting, enchanting, historic and exotic settings.',fg="purple",bg="#70a6ff",font="Times 21 bold") .place(x=175,y=20)
            tk.Label(about_us, text='The common operating philosophy at all Cafe Cliché properties \nis attention to even the smallest details, exceptionally personal service \nand a continuous effort to meet and even foretell customer requirements. \nIn addition, each property celebrates and reflects \nits area’s artistic idioms and cultural expressions \nwith a view to giving clients a unique experience in every Serena. \nThese values are key to Serena’s ethos and are the key elements \nthat contribute to the strength and uniqueness of the brand.',fg="purple",bg="#70a6ff",font="Times 21 bold") .place(x=250,y=300)

                    
            def aboutus_exit():
                 about_us.destroy()
            tk.Button(about_us,text="BACK",width=30,height=2,command=aboutus_exit).place(x= 550, y = 600)   

        
        def user_exit():
            user.destroy()
            main_func()
         #BUTTON OF ABOUT US WINDOW
        tk.Label(user,text="User Area",font="Verdana 50 bold",bg="#70a6ff").place(x=100,y=40)
        #BUUTON FOR ROOMS WINDOW
        tk.Button(user,text="ROOM RESERVATION",width=30,command=room_booking).place(x=550,y=250)
        #BUTTON FOR PARKING WINDOW
        tk.Button(user,text="PARKING",width=30,command=parking).place(x=550,y=300)
        #BUTTON FOR QUERIES WINDOW
        tk.Button(user,text="QUERIES",width=30,command=queries).place(x=550,y=350)
        #BUTTON FOR FEEDBACK
        tk.Button(user,text="FEEDBACK",width=30,command=feedback).place(x=550,y=400)
        #BUTTON FOR ABOUT US
        tk.Button(user,text="ABOUT US",width=30,command=about_us).place(x=550,y=450)
        #BACK BUTTON FOR USER WINDOW
        tk.Button(user,text="BACK",width=30,command=user_exit).place(x=550,y=500)
 

    # Function to close the main window
    def exit():
        exitConfirm = tkinter.messagebox.askyesno('Are you sure?', 'Are you sure you want to exit?')
        if exitConfirm == True:
            main.destroy()

    # Buttons for the main page

    tk.Button(main, text='Admin', width=50,height=2,command=admin).place(x=500,y=375)

    tk.Button(main, text='User', width=50,height=2, command=lambda: user_func(1)).place(x=500,y=425)

    tk.Button(main, text='Exit',width=50,height=2, command=exit).place(x=500,y=475)

    main.mainloop()
main_func()

#---End---#
