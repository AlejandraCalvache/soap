# SOAP Project - Hello World

This project consists of a web page that interacts with a basic SOAP service to display a greeting using JavaScript. The SOAP service is given a name and responds with a greeting message.

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge).
- SOAP server running at `http://localhost:8000`.

# Installation

## 1. Clone the repository 
git clone <REPOSITORY_URL>
cd <directory_name>

2. SOAP Server Setup
To interact with this SOAP client, you will need a working SOAP server. You can use the Python SOAP service I provided above, or any SOAP server that implements the say_hello operation.

If you are using the Python service with Spyne, follow the steps in the server.py file to configure it and run it at http://localhost:8000.

3. Client Configuration
Open the client.html file in your browser. This file contains the JavaScript code that interacts with the SOAP server.

Usage
Make sure the SOAP server is running at http://localhost:8000.

Open the client.html file in your browser.

Click the "Call SOAP Service" button to send a request to the service and receive the greeting.

The received greeting will be displayed on the web page as "Hello, World!".

Project Structure
client.html: HTML file with the code that makes the call to the SOAP service and displays the response.
server.py: (If you use the Python server) File with the SOAP service implemented in Python using Spyne.
README.md: This file with the project description.
Code Description
client.html
The client.html file contains a SOAP client that interacts with the server using JavaScript:

XMLHttpRequest: Uses the XMLHttpRequest object to send a SOAP request to the server.
SOAP Envelope: The SOAP request is an XML message containing the World name that will be processed by the server.
SOAP Response: The server responds with an XML message, and the client extracts and displays the received greeting.
server.py
The server.py file (if you are using the SOAP server in Python) defines a SOAP service using Spyne. The service has a say_hello method that takes a name and returns a greeting.

python
Copy code
class HelloWorldService(ServiceBase):
@rpc(str, _returns=str)
def say_hello(ctx, name):
return f"Hello, {name}!"
Notes
The project assumes that you have a SOAP server running at http://localhost:8000. If you need help setting up a SOAP server, see the server section in this README.
If you make changes to the client.html file, make sure that the method names and parameters match those defined in the SOAP service.
