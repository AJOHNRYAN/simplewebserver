# EX01 Developing a Simple Webserver
## Date:29.10.2026

## AIM:
To develop a simple webserver to serve html pages and display the Windows Specifications of your Laptop.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
web.py
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<head>
    <title>localhost:8000</title>
</head>
<body>

<h2>A JOHN RYAN A (26008446)</h2>
<h3>Laptop Configuration</h3>

<table border="1" width="700" height="350" cellpadding="12" cellspacing="0">

    <tr bgcolor="#1E3A5F">
        <th><font color="white">Specification</font></th>
        <th><font color="white">Details</font></th>
    </tr>

    <tr bgcolor="#E6F2FF">
        <td>Device Name</td>
        <td>A JOHN RYAN</td>
    </tr>

    <tr bgcolor="#F0F8FF">
        <td>Processor</td>
        <td>Intel Core 5 210H (2.20 GHz)</td>
    </tr>

    <tr bgcolor="#E6F2FF">
        <td>RAM</td>
        <td>16 GB (15.7 GB usable)</td>
    </tr>

    <tr bgcolor="#F0F8FF">
        <td>Graphics Card</td>
        <td>Intel Graphics (128 MB)</td>
    </tr>

    <tr bgcolor="#E6F2FF">
        <td>Storage</td>
        <td>112 GB of 477 GB used</td>
    </tr>

    <tr bgcolor="#F0F8FF">
        <td>System Type</td>
        <td>64-bit OS, x64-based processor</td>
    </tr>

    <tr bgcolor="#E6F2FF">
        <td>Pen & Touch</td>
        <td>No pen or touch input</td>
    </tr>

</table>

</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Client request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my own webserver is running successfully...")
httpd.serve_forever()
```
## OUTPUT:
<img width="1916" height="1078" alt="Screenshot 2026-11-04 193851" src="https://github.com/user-attachments/assets/b12e2773-922a-4d34-9e74-b0df5b32a682" />
<img width="1600" height="900" alt="WhatsApp Image 2026-11-04 at 7 46 35 PM" src="https://github.com/user-attachments/assets/63465c8f-919d-439d-8f83-3fc1ad8bf32f" />


## RESULT:
The program for implementing simple webserver is executed successfully.
