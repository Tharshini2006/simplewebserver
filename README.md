# EX01 Developing a Simple Webserver
## Date:08.04.2025

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.


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
               '''
              from http.server import HTTPServer, BaseHTTPRequestHandler
              content = """
              <html>
              <head>
              <h2 style="font-family: Arial, sans-serif; color: blue; text-align: center;"><b>LIST OF PROTOCOLS</b></h1>
              <h1>NAME:THARSHINI.M <br> 
              REF NO:212224230287</h2>

             <title>TCP/IP Protocol Suite</title>
            </head>
            <body>
    <h1>TCP/IP Protocol Suite</h1>
    <ul>
        <li>HTTP</li>
        <li>FTP</li>
        <li>SMTP</li>
        <li>DNS</li>
        <li>Telnet</li>
        <li>SNMP</li>
    </ul>
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
        server_address = ('',8000)
        httpd = HTTPServer(server_address,myhandler)
        print("my webserver is running...")
        httpd.serve_forever()
        '''

## OUTPUT:
![alt text](<WhatsApp Image 2025-04-08 at 21.48.26_e07a1992.jpg>)

![alt text](<WhatsApp Image 2025-04-08 at 21.48.53_34f7b4b3.jpg>)



## RESULT:
The program for implementing simple webserver is executed successfully.
