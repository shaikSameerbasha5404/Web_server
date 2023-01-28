# Developing a Simple Webserver

# AIM:

Name: Shaik Sameer Basha
Reff no:22004926

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```python
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<hl>Welcome</hl>
<h1>SHAIK SAMEER BASHA</h1>
<h1>22004926</h1>
</body>
<html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address=('',80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()        
```

# OUTPUT:
![Screenshot (74)](https://user-images.githubusercontent.com/118707756/215249056-c09d360b-f127-4288-969b-58e526cf2fd6.png)
# RESULT:

The program is executed succesfully
