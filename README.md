# Developing a Simple Webserver
NAME:Kiran C REFERENCE NO:22008437


# AIM:

Develop a webserver to display about top five web application development frameworks.

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
from http.server import HTTPServer,BaseHTTPRequestHandler
content="""
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
<h2>Kiran C</h2>
<h3>22008437</h3>
<ul>
<li>DJANGO<img src =
"https://static.djangoproject.com/img/logos/django-logo-negative.1d528e2cb5fb.png"></li>
<li>FLASK<img src =
"https://codersera.com/blog/wp-content/uploads/2019/06/flask-python.png"></li>
</ul>
</body>
</html>
"""
class HelloHandler(BaseHTTPRequestHandler):
def do_GET(self):
self.send_response(200)
self.send_header('Content-type','text/html; charset=utf-8')
self.end_headers()
self.wfile.write(content.encode())
server_address=('',80)
httpd=HTTPServer(server_address,HelloHandler)
httpd.serve_forever()



# OUTPUT:
![Screenshot_20230116_121449_11zon](https://user-images.githubusercontent.com/118668751/212614899-8cf07235-51bf-4e1a-9888-037ca2cce085.jpg)


# RESULT:

The program is executed succesfully
