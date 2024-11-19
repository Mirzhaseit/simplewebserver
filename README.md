<<<<<<< HEAD
# EX01 Developing a Simple Webserver

=======

# EX01 Developing a Simple Webserver

>>>>>>> f0cbe0269a40a66316e607b1987dadbeb981f095
## Date:28/10/2024
## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<body><pre>
<h1>Laptop configuration(24901261)</h1>
<ul>
<li>Device name     Mirzha Fathima</li>
<li>Processor       13th Gen Intel(R) Core(TM) i5-1335U   1.30 GHz</li>
<li>Installed ram   16.0 GB (15.7 GB usable)</li>
<li>Device id       15EEA3B2-7EF5-4DEC-903D-577382C3C005</li>
<li>Product id      00342-42709-10432-AAOEM</li>
<li>System type     64-bit operating system, x64-based processor</li>
<li>Pen and touch   no pen or touch input is available for this display</l
</ul>
</pre></body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()


```

## OUTPUT:
![alt text](<Screenshot (67).png>)
![alt text](<Screenshot (68).png>)

## RESULT:
The program for implementing simple webserver is executed successfully.
