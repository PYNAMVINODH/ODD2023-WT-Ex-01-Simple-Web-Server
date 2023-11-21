# Ex-01-Simple-Web-Server
## Date:

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
<head>
<title>Top Five Web Application Development Frameworks</title>
</head>
<body>
<h1>1.Django</h1>
<h1>2.MEAN Stack</h1>
<h1>3.React<h1>
<h1>4.Ruby on rails<h1>
<h1>5.Angular<h1>
</body>
</html>

"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()
```


## OUTPUT:
 ![WhatsApp Image 2023-11-21 at 15 52 34_561e8d19](https://github.com/PYNAMVINODH/ODD2023-WT-Ex-01-Simple-Web-Server/assets/145742678/bf371f29-9477-4f1b-8470-09af57dd0fe6)


## RESULT:
The program for implementing simple webserver is executed successfully.
