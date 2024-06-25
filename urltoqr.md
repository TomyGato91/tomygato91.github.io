## Pyhton Program to short an URL and get their QR code

**Project description:** This is a starting program that I wrote while practicing my knowledge in Python and the use of different libraries. In this case the project is based on the libraries psyshorteners (to handle url shortening) and qrcode (to generate a qr code from that url).

### 1. Install and import both libraries  

First of all we install both libraries directly through the VisualStudio TERMINAL by using pip:

```javascript
pip install qrcode
pip install psyshorteners
pip3 install qrcode
pip3 install psyshorteners
```

Then we import both libraries

```javascript
import qrcode
import psyshorteners
```

### 2. Main Program

```javascript
def your_birthday():                                                                            #we define the function your_birthday 
    try:
        Birthday = input("Enter your Date of Birth in numbers (Day/Month/Year) : ")             #we ask the user to enter his birthday in form of a string     
        Datebirth = dt.datetime.strptime(Birthday, '%d/%m/%Y')                                  #we identify the date from the string insterted before
        Weekday = Datebirth.weekday()                                                           #from the date we now get an int to identify the day of the week: Mon->0 ,Sun->6
    except:
        print("Your Input is wrong!")
        return
    finally:
        Bornday = cal.day_name[Weekday]                                                         #we get the day of the week as a string from the int of Weekday
        print("You were born the " + Birthday + " and that was on a {}." .format(Bornday))      #print the solution by calling the string that gives us the day of the week (Bornday)

your_birthday()                                                                                 #call the function
```

### 3. Results: 

In order to know if the program runs properly I tried with my own birthday first : 01/12/1991
And then with the next day and the day before. As seen on the console my program seems to work!

<img src="images/Captura de pantalla 2024-06-24 a las 19.30.34.png?raw=true"/>
