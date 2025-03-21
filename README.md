# EX01 Developing a Simple Webserver
## Date:21-03-2025

## AIM:
To develop a simple webserver to serve html pages and display the types of headings in TCP/IP Protocol Suite.

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

rom http.server import HTTPServer, BaseHTTPRequestHandler

content = """

<!DOCTYPE html>

<html>

  <body>



<h1>Heading 1</h1>

<h2>Heading 2</h2>

<h3>Heading 3</h3>

<h4>Heading 4</h4>

<h5>Heading 5</h5>

<h6>Heading 6</h6>


</body>

</html>


"""
class myhandler(BaseHTTPRequestHandler):

    def do_GET(self):
    
        print("request received")
        
        self.send_response(200)
        
        self.send_header('content-type', 'text/html; charset=utf-8')
        
        self.end_headers()
        
        self.wfile.write(content.encode())

server_address = ('',80)

httpd = HTTPServer(server_address,myhandler)

print("my webserver is running...")

httpd.serve_forever()



## OUTPUT:
![Screenshot 2025-03-21 184510-1](https://github.com/user-attachments/assets/b840007e-889a-4ce0-9005-d49d36615e43)

![Screenshot 2025-03-21 184447](https://github.com/user-attachments/assets/a317df7a-21db-4a2c-bcc7-891bbe877cde)




## RESULT:
The program for implementing simple webserver is executed successfully.

