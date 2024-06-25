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

### 2. URL shortener

We start by asking the user to insert his long URL

```javascript
weblink = input("Please insert your URL to create a QR code: ")
```
Now we use use the Base Factory class of the library pyshorteners -> Shortener() <br>
In order to short our link we choose the API: Da.gd from the library (There are many more) <br>
And with .short we finally get our shorted version of the URL we inserted before. 

```javascript
shorturl = pyshorteners.Shortener() 
url_shorted = shorturl.dagd.short(weblink)

print("Your shortened URL is : ",url_shorted)
```

### 3. QR code generator

From the inserted URL we will now create a QR code for it! We start defining the size of our QR code <br>
With the class QRCode we can suit the size. Version 1 generates a 21x21 Matrix in which we decided a box_size of 10 and a border of 4 <br>
Then with .add_data we add the URL that we asked at the begining and with .make and a True value for fit, it generates the QR code it automatically <br>

```javascript
qr = qrcode.QRCode(version = 1, box_size = 10, border = 5)

qr.add_data(weblink)
qr.make(fit = True)
```

Finally we decide the QR code background and painting color. In this case we choose a generic back and white QR. <br>
And we save our generated QR code with .save in the folder were our program is running.

```javascript
img = qr.make_image(fill='black', back_color = 'white')
img.save('GeneratedQR.png')
```

### 3. Results: 

In order to know if the program runs properly I tried with my own birthday first : 01/12/1991
And then with the next day and the day before. As seen on the console my program seems to work!

<img src="images/Captura de pantalla 2024-06-24 a las 19.30.34.png?raw=true"/>
