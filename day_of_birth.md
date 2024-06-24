## Pyhton Program to know the day of the week you were born

**Project description:** This is a starting program that I wrote while practicing my knowledge in Python and the use of different libraries. In this case the project is based on the libraries datetime & calendar. Both are useful in order to manipulate time modules and work directly in days, months and years in order to get different information. 

### 1. Import both libraries 



```javascript
import datetime as dt
import calendar as cal
```

### 2. Main Function: your_birthday() 

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
