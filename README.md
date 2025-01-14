# SOAP Project - Hello World

This project consists of a web page that interacts with a basic SOAP service to display a greeting using JavaScript. The SOAP service is given a name and responds with a greeting message.

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge).
- SOAP server running at `http://localhost:8000`.

## Installation
```bash
1. Clone the repository
git clone <REPOSITORY_URL>
cd <directory_name>

2. SOAP Server Setup (If you're using Python)
```bash
Install the required dependencies:

bash
Copy code
pip install spyne wsgi
Create and run the server.py file:

bash
Copy code
python server.py
This will start the SOAP server at http://localhost:8000.

3. Client Setup
Open the client.html file in your browser and click the "Call SOAP Service" button to interact with the service and view the greeting on the page.
bash

Client Configuration
Once the SOAP server is running, open the client.html file in your browser. This file contains the JavaScript code that interacts with the SOAP server.

If everything is configured correctly, you will be able to click the "Call SOAP Service" button and see the "Hello, World!" greeting on the page.

