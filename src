#subprogram to clear the screen
def clearscreen():
    for widget in Screen.winfo_children():
        widget.destroy()

def clearscreenB():
    for Button in Screen.winfo_children():
        Button.destroy()

#profile button subprogram when the driver is on the driveMode() screen/subprogram
def profileClickedDriveMode():
    #clear the screen
    clearscreen()

    #word 'profile' and its location
    profileLabel = Label(Screen, text="Profile:", font="100", fg="#ffc5d3", bg="#fffff6")
    profileLabel.place(x=40, y=86)

    #the drivers details
    driverForenameLabel = Label(Screen, text="Forename: Eva", font="30", fg="#ffc5d3", bg="#fffff6")
    driverForenameLabel.place(x=40, y=136)
    driverLastnameLabel = Label(Screen, text="Lastname: Rebelo Marques", font="30", fg="#ffc5d3", bg="#fffff6")
    driverLastnameLabel.place(x=40, y=196)
    ratingLabel = Label(Screen, text="Rating: 5.0 ", font="30", fg="#ffc5d3", bg="#fffff6")
    ratingLabel.place(x=40, y=256)
    carTypeLabel = Label(Screen, text="Car Type: PINK Dodge Royal", font="30", fg="#ffc5d3", bg="#fffff6")
    carTypeLabel.place(x=40, y=316)
    licencePlateLabel = Label(Screen, text="Licence Plate: ST47 GRL", font="30", fg="#ffc5d3", bg="#fffff6")
    licencePlateLabel.place(x=40, y=376)
    
    #button that takes driver/user back to the LoadLoginPage() subprogram
    logOff = Button(Screen, text="Log Off", font=1, bg="#ffc5d3", command=lambda: loadLoginPage())
    logOff.place(x=40, y=436)
    
    #button to exit the profile page
    exitButton = Button(Screen, text="X", font=30, bg="#ffc5d3", command=lambda: driveMode())
    exitButton.place(x=280, y=32)

#profile button subprogram when the driver is on the mainScreen() screen/subprogram
def profileClickedMainScreen():
    #clear the screen
    clearscreen()

    #the word profile
    profileLabel = Label(Screen, text="Profile:", font="100", fg="#ffc5d3", bg="#fffff6")
    profileLabel.place(x=40, y=86)

    #the drivers details
    driverForenameLabel = Label(Screen, text="Forename: Eva", font="30", fg="#ffc5d3", bg="#fffff6")
    driverForenameLabel.place(x=40, y=136)
    driverLastnameLabel = Label(Screen, text="Lastname: Rebelo Marques", font="30", fg="#ffc5d3", bg="#fffff6")
    driverLastnameLabel.place(x=40, y=196)
    ratingLabel = Label(Screen, text="Rating: 5.0 ", font="30", fg="#ffc5d3", bg="#fffff6")
    ratingLabel.place(x=40, y=256)
    carTypeLabel = Label(Screen, text="Car Type: PINK Dodge Royal", font="30", fg="#ffc5d3", bg="#fffff6")
    carTypeLabel.place(x=40, y=316)
    licencePlateLabel = Label(Screen, text="Licence Plate: ST47 GRL", font="30", fg="#ffc5d3", bg="#fffff6")
    licencePlateLabel.place(x=40, y=376)

    #button taking user back to the LoadLoginPage() subprogram
    logOff = Button(Screen, text="Log Off", font=1, bg="#ffc5d3", command=lambda: loadLoginPage())
    logOff.place(x=40, y=436)

    #button that allows user to exit the profile screen
    exitButton = Button(Screen, text="X", font=30, bg="#ffc5d3", command=lambda: mainScreen())
    exitButton.place(x=280, y=10)

#subprogram taking the user back to the mainscreen() page
def exitPopUp():
    #button taht takes user to the confirmation
    whiteSquare = Label(Screen, width=21, height=10, bg="#fffff6")
    whiteSquare.place(x=157, y=11)
    exitButton = Button(Screen, text="X", font=30, bg="#ffc5d3", command=lambda: driveMode())
    exitButton.place(x=280, y=10)

    #confirmation that the user would like to go back to the mainscreen
    queryLabel = Label(Screen, text="Are you sure you \n you want to \n  \nexit?", bg="#fffff6", width=12, height=5)
    areyousureLabel.place(x=159, y=40)
    yesButton = Button(Screen, text="yes", bg="#ffc5d3", command=lambda: mainScreen(), width=4)
    yesButton.place(x=250, y=120)

#imports
from tkinter import *
import tkinter as tk
from tkinter import messagebox
import customtkinter as ctk
import tkintermapview
import mysql.connector
import sqlite3
import random

#creating a database
connection = sqlite3.connect("addresses.db")
cursor = connection.cursor()

#creating the table with SE addresses
cursor.execute("create table SEaddresses (pickupLocation text,pickupPostcode text,dropoffLocation text, earning text)")

#values to be inputted
SEaddress_list = [
    ("P:23 Lewisham Way","SE14 6PP", "\nD:67 Coldharbour Lane, SW9 8HW", "\nP:12.60"),
    ("P:89 Forest Hill Road,","SE23 2DD", "\nD:48 Mitcham Lane, SW16 6LG", "\nP:20.00"),
    ("P:5 Nunhead Lane","SE15 3NT", "\nD:40 Lavender Sweep, SW11 1HJ", "\nP:34.20"),
    ("P:3 Blackheath Hill","SE10 8AA", "\nD:18 Marton Road, SW19 2BD", "\nP:6.99"),
    ("P:64 Catford Hill","SE6 4PP", "\nD:11 Balham Park Road, SW12 8HS", "\nP:25.98"),
    ("P:94 Woolwich Road","SE7 8LG", "\nD:5 Tower Bridge Road, SE1 4TT", "\nP:24.80"),
    ("P:61 Eltham High Street","SE9 1DQ", "\nD:36 Bell Green, Sydenham, SE26 4QD", "\nP:37.10"),
    ("P:87 Abbey Wood Road","SE2 9NR", "\nD:50 Ladywell Road, SE13 7XQ", "\nP:18.12"),
    ("P:38 Tulse Hill","SE27 9EP", "\nD:21 Drakefell Road, SE4 2OT", "\nP:13.04"),
    ("P:42 Brockley Road","SE4 2EF", "\nD:114 Clapham High Street, SW4 7UJ", "\nP:27.02"),
    ("P:16 New Cross Road","SE14 5BD", "\nD:29 Southfields Avenue, SW18 5RJ", "\nP:16.34"),
    ("P:23 Lewisham Way","SE14 6PP", "\nD: Helville Court, Greenwich, SE10 8QW", "\nP:24.70"),
    ("P:8 Forest Hill Road","SE23 2DD", "\nD:110 Old Kent Road, SE1 4TY", "\nP:16.45"),
    ("P:95 Nunhead Lane","SE15 9LP", "\nD:14 Kings Avenue, Clapham, SW4 8DQ", "\nP:10.99"),
    ("P:43 Honor Oak Road","SE23 3LG", "\nD:91 Clapham Park Road, SW4 7DP", "\nP:15.99"),
    ("P:12 Lee High Road","SE13 5NS", "\nD:39 Walworth Road, SE17 1YQ", "\nP:19.95"),
    ("P:91 Crystal Palace Road","SE22 9LL", "\nD:13 Brixton Road, SW9 6OS", "\nP:14.70"),
    ("P:83 Peckham High Street","SE15 5RR", "\nD:107 Deptford High Street, SE8 4PS", "\nP:34.80"),
    ("P:47 Archway Road","SE15 3NR", "\nD:17 Clapham Common North Side, SW4 9SG", "\nP:33.99"),
    ("P:48 Penge High Street","SE20 7DS", "\nD:43 Old Kent Road, SE1 5EZ", "\nP:23.09"),
    ("P:67 Grove Park Road","SE12 8QX", "\nD:78 Walworth Road, SE17 1DN", "\nP:12.89"),
    ("P:41 Telegraph Hill","SE14 6TY", "\nD:5 Brixton Road, SW9 6DJ", "\nP:47.81")
]

#making a second table with SW addresses
cursor.execute("create table SWaddresses (pickupLocation text,pickupPostcode text,dropoffLocation text, earning text)")

#values to be inputted
SWaddress_list = [
    ("P:71 Clapham Common North Side","SW4 9RH", "\nD:7 Lavender Grove, SW9 8HA", "\n Price: 27.90"),
    ("P:16 Stockwell Park Road","SW9 0DA", "\nD:25 Kensington Lane, SE11 4HQ", "\n Price: 25.10"),
    ("P:34 Lavender Hill","SW11 5RR", "\nD:33 South Lambeth Road, SW8 1TS", "\n Price: 18.20"),
    ("P:39 Earlsfield Road","SW18 3BE", "\nD:29 Bermondsey Wall East, SE16 4TX", "\n Price: 17.60"),
    ("P:83 South Lambeth Road","SW8 1UG", "\nD:9 Horniman Drive, Forest Hill, SE23 3BQ", "\n Price: 36.55"),
    ("P:12 Colliers Wood High Street","SW19 5BU", "\nD:11 Dartmouth Hill, Blackheath, SE10 8AW", "\n Price: 12.80"),
    ("P:9 Raynes Park Road","SW20 3QO", "\nD:95 Westcombe Hill, SE3 7DT", "\n Price: 45.20")
]

#inserting the values of the tables as a tuple to the database as four seperate columns
cursor.execute("insert into SEaddresses values (?,?,?,?)", SEaddress_list)
cursor.execute("insert into SWaddresses values (?,?,?,?)", SWaddress_list)

#printing all the rows on both tables to make sure the database has all the values in it
for row in cursor.execute("select * from SEaddresses"):
    print(row)

for row in cursor.execute("select * from SWaddresses"):
    print(row)

#creating a window for my code
Screen = Tk()
Screen.geometry("330x620")
Screen.config(bg="#fffff6")


#the login screen
def loadLoginPage():
    #clearing the screen
    clearscreen()

    #button that will make it so the values inputted are correct and takes user to the mainscreen() subprogram
    loginButton = Button(Screen, text="Login", font="5", fg="#ffffff", height=1, width=5, bg="#ffc5d3", command=lambda: loginClicked())
    loginButton.place(x=220, y=296)

    #the username and password labels
    usernameLabel = Label(Screen, text="Username", font="35", fg="#ffc5d3", bg="#fffff6")
    usernameLabel.place(x=40, y=176)
    passwordLabel = Label(Screen, text="Password", font="35", fg="#ffc5d3", bg="#fffff6")
    passwordLabel.place(x=40, y=236)

    #entry boxes for the username and password
    usernameEntry = Entry(Screen, text="Username", font="30", fg="#000000", bg="#fffff6", width=12)
    usernameEntry.place(x=160, y=176)
    passwordEntry = Entry(Screen, text="Password", font="30", fg="#000000", bg="#fffff6", width=12)
    passwordEntry.place(x=160, y=236)
    
    #the values that the user needs to input
    drivercodeA = "3456"
    passwordA = "1234"
    
    #if statement to allow or disallow access to the rest of the program
    def loginClicked():
        if usernameEntry.get() == drivercodeA and passwordEntry.get() == passwordA:
            mainScreen()
        else:
            #error message that opens up when details are incorrect
            messagebox.showerror("Error", "Incorrect username or password.\nTry again.")

# the main screen subprogram
def mainScreen():
    #Clear the Screen
    clearscreen()

    #the interactive map
    map = tkintermapview.TkinterMapView(Screen, width=500, height=800)
    map.place(relx=0.5, rely=0.5, anchor=tk.CENTER)

    #button indicating they're ready to drive and its placement
    whiteBlock = Label(Screen, width = 400, height = 56, bg = "#ffffff")
    whiteBlock.place(x=0, y=400)
    
    #subprogram that will allow the user to input the type of address they're looking for
    readyDrive = Button(Screen, text="Drive", font = 30, width = 10, height = 2, bg="#ffc5d3", command=lambda: locationGet(useDatabase))
    readyDrive.place(x=107, y=460)
    
    #button that takes the driver to their profile
    profileButton = Button(Screen, text = "Profile", font = 30, fg = "#BE9D04", command = lambda: profileClickedMainScreen())
    profileButton.place(x=20, y=30)
    
    #variable that will determine which database the program will fetch the requests from
    useDatabase = 0

#subprogram for driver to specify what address they would like to get clients from
def locationGet(useDatabase):
    whiteBlock = Label(Screen, width=35, height=9, bg="#ffffff")
    whiteBlock.place(x=45, y=200)
    locationLabel = Label(Screen, text="SW on SE", font="35", fg="#000000", bg="#ffffff")
    locationLabel.place(x=46, y=210)

    #entry box for driver to input details
    locationEntry = Entry(Screen, font="30", fg="#000000", bg="#ffffff", width=19)
    locationEntry.place(x=48, y=250)

    #subprogram assigning a value to the useDatabase variable to specify what database the requests will come from
    def updateDatabase():
        global useDatabase
        if locationEntry.get() == "SW":
            useDatabase += 2
        else:
            useDatabase -= 2
        driveMode(useDatabase)

    #button confirming a value is inputted the right postcode
    locationButton = Button(Screen, text="Confirm", font=30, bg="#ffc5d3", command=updateDatabase)
    locationButton.place(x=200, y=290)


#subprogram that will allow requests to come through
def driveMode(useDatabase):
    #clearing the screen
    clearscreen()

    #the map widget
    map = tkintermapview.TkinterMapView(Screen, width=500, height=800)
    map.place(relx=0.5, rely=0.5, anchor=tk.CENTER)

    #the profile button
    profileButton = Button(Screen, text="Profile", font=30, fg="#BE90D4", command=lambda: profileClickedDriveMode())
    profileButton.place(x=20, y=30)

    #the exit button
    exitMainScreenButton = Button(Screen, text="X", font=30, fg="#BE90D4", command=lambda: exitPopUp())
    exitMainScreenButton.place(x=280, y=32)

    #randomising the order of the rows on the table
    random.shuffle(SEAddress_list)
    
    #randomising the order of the rows of the second table
    random.shuffle(SWAddress_list)
    
    #checking the value of the useDatabase variable and retrieving requests from the database the value corresponds to
    if useDatabase >= 2:
        requestSW = tk.Label(Screen, text = SWAddress_list[0], fg="#ffc5d3", bg="#fffff6", width = 30,height = 3)
        requestSW.place(x = 0, y=250)
    else:
        requestSE = tk.Label(Screen, text = SEAddress_list[0], bg="#ffc5d3", bg="#fffff6", width = 30,height = 3)
        requestSE.place(x = 0, y=250)
    
    #array for clients name
    nameArray=["Kanye", "Eren", "Theo", "Grant", "Cornelius", "Saiki", "Roy", "Jasmin"]
    random.shuffle(nameArray)
    
    #array for the client's rating
    ratingArray = ["4.5","3.9","4.2","5.0","4.9","4.7","4.8","2.1","3.7","2.5","4.3"]
    random.shuffle(ratingArray)
    
    #array for the ride details
    detailsArray = ["quiet ride", "electric car", "play music", "heated seats", "N/A"]
    random.shuffle(detailsArray)
    
    nameRating = tk.Label(Screen, text = nameArray[0]+ "      "+ratingArray[0],font=5,fg="#ffc5d3",bg="#fffff6",width=19)
    nameRating.place(x = 0, y=223)
    
    denyRequest = Button(Screen, text="X", bg="#BE90D4", command=lambda: driveMode(useDatabase))
    denyRequest.place(x = 200 , y=223)
    
    details = tk.Label(Screen, text = "Details: "+detailsArray[0],font="1",fg="#ffc5d3",bg="#fffff6",width=19)
    details.place(x = 0, y=300)
    
    buttonBackground = tk.Label(Screen, text = "Details: "+detailsArray[0],font="1",fg="#fffff6",bg="#fffff6",width=19)
    buttonBackground.place(x = 0, y=328)
    
    acceptButton = Button(Screen, text="accept", height=1, width=10,bg="#BE90D4", command= lambda: rideOngoing())
    acceptButton.place(x = 72, y = 328)

def rideOngoing():
    #clearing the screen
    clearscreen()

    #the map widget
    map = tkintermapview.TkinterMapView(Screen, width=500, height=800)
    map.place(relx=0.5, rely=0.5, anchor=tk.CENTER)

    #the profile button
    profileButton = Button(Screen, text="Profile", font=30, bg="#BE90D4", command=lambda: profileClickedDriveMode())
    profileButton.place(x=20, y=30)

    #the exit button
    exitMainScreenButton = Button(Screen, text="X", font=30, bg="#BE90D4", command=lambda: exitPopUp())
    exitMainScreenButton.place(x=280, y=32)
    
    #button indicating theyre ready to drive and its placement
    whiteBlock = Label(Screen, width = 400, height = 56, bg = "#ffffff")
    whiteBlock.place(x=0,y=400)
    
    #checking the value of the useDatabase variable and retrieving requests from the database the value corresponds to
    if useDatabase >= 2:
        requestSW = tk.Label(Screen, text = SWAddress_list[0][0], fg="#ffc5d3", bg="#ffffff", width = 30,height = 3, font = 1)
        requestSW.place(x=0,y=460)
    else:
        requestSE = tk.Label(Screen, text = SEAddress_list[0][0], fg="#ffc5d3", bg="#ffffff", width = 30,height = 3, font = 1)
        requestSE.place(x=0,y=460)

loadLoginPage()
connection.close()
Screen.mainloop()

