## Pyhton Program to short an URL and get their QR code

**Project description:** This is a starting program that I wrote while practicing my knowledge in Python and the use of different libraries. In this case the project is based on the libraries psyshorteners (to handle url shortening) and qrcode (to generate a qr code from that url).

### 1. Install and import both libraries  

First of all we install both libraries directly through the VisualStudio TERMINAL by using pip:

```javascript
pip install qrcode
pip install pyshorteners
pip3 install qrcode
pip3 install pyshorteners
```

Then we import both libraries

```javascript
import qrcode
import pyshorteners
```

### 2. Main Program

We start by asking the user to insert his long URL

```javascript
weblink = input("Please insert your URL to create a QR code: ")
```
Now we use use the Base Factory class of the library pyshorteners -> Shortener()
In order to short our link we choose the API: Da.gd from the library (There are many more)
And with .short we finally get our shorted version of the URL we inserted before. 

```javascript
shorturl = pyshorteners.Shortener() 
url_shorted = shorturl.dagd.short(weblink)

print("Your shortened URL is : ",url_shorted)
```

### 3. Results: 

In order to know if the program runs properly I tried with my own birthday first : 01/12/1991
And then with the next day and the day before. As seen on the console my program seems to work!

<img src="images/Captura de pantalla 2024-06-24 a las 19.30.34.png?raw=true"/>
