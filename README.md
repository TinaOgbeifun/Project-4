# Project-4
# Documentation for Project-4

MEAN STACK DEPLOYMENT TO UBUNTU IN AWS

implementing a simple Book Register web form using MEAN stack

Step 1 - Run sudo apt update

![updating ubuntu](./images/sudo-apt-update.png)

Upgrade ubuntu

sudo apt upgrade

![running sudo apt upgrade](./images/sudo-apt-upgrade.png)

Next, Install NodeJS

sudo apt install -y nodejs

![installing nodejs](./images/install-nodejs.png)

Step 2: Install MongoDB
MongoDB stores data in flexible, JSON-like documents. Fields in a database can vary from document to document and data structure can be changed over time

Install MongoDB

sudo apt install -y mongodb

![Installing Mongodb](./images/Installing-Mongo-db.pngimage.jpg)

Start The server

sudo service mongodb start
Verify that the service is up and running

sudo systemctl status mongodb


![Verifying the status of mongodb](./images/sudo-system-status-mongodb.png)

Install npm – Node package manager.

sudo apt install -y npm

![Installing npm](./images/installing-npm.png)

Install body-parser package

We need ‘body-parser’ package to help us process JSON files passed in requests to the server.

sudo npm install body-parser

![installing body parser](./images/Body-parser.png)

Create a folder named ‘Books’

mkdir Books && cd Books

In the Books directory, Initialize npm project

npm init

![running npm init](./images/npm-init.png)

Add a file to it named server.js

![Initializing npm project](./images/npm-project.png)

Run vi server.js in Books directory

Copy and paste the web server code below into the server.js file


![Pasting the web server code in the sever.js file](./images/web-code.png)
# Install Express and set up routes to the server

Express is a minimal and flexible Node.js web application framework that provides features for web and mobile applications

sudo npm install express mongoose

![npm install express mongoose](./images/npm%20install%20express%20mongoose.png)

In ‘Books’ folder, create a folder named apps

mkdir apps && cd apps

![creating apps directory and cd into apps](./images/apps-directory-cd-into-apps.pngimage.jpg)

Create a file named routes.js

![creating routes file](./images/routes-js.png)

vi routes.js

Copy and paste the code below into routes.js

![pasting code in the routes.js file](./images/routes-js-file.png)

In the ‘apps’ folder, create a folder named models

mkdir models && cd models


Create a file named book.js

vi book.js

![making models directory and cd models](./images/models-directory-and-cd-models.png)

Copy and paste the code below into ‘book.js’

![pasting code into book.js file](./images/book-js-file.png)

# Access the routes with AngularJS

AngularJS provides a web framework for creating dynamic views in your web applications. In this tutorial, we use AngularJS to connect our web page with Express and perform actions on our book register.

Change the directory back to ‘Books’

cd ../..

Create a folder named public

mkdir public && cd public

![changing to book directory and creating public folder](./images/book-directory-public-folder.png)

Add a file named script.js

vi script.js
Copy and paste the Code below (controller configuration defined) into the script.js file

![pasting code into the script.js file](./images/script-js.png)

In public folder, create a file named index.html;

vi index.html

![creating index.html file in the public folder](./images/vi-index-html.png)

Cpoy and paste the code below into index.html file

![Pasting the code in the index.html file](./images/html-file.png)

Change the directory back up to Books

cd ..
Start the server by running this command:

node server.js

![starting the server](./images/node-server-js.png)

The server is now up and running, we can connect it via port 3300. You can launch a separate Putty or SSH console to test what curl command returns locally.

curl -s http://localhost:3300

![![Testing what curl command will return locally](./images/testing-curl-command.png)

It shall return an HTML page, it is hardly readable in the CLI, but we can also try and access it from the Internet.

For this – you need to open TCP port 3300 in your AWS Web Console for your EC2 Instance

![Adding 3300 rule](./images/adding-3300-rule.png)

To access our Book Register web application from the Internet with a browser using Public IP address or Public DNS name

Run curl -s http://169.254.169.254/latest/meta-data/public-ipv4 for Public IP address or curl -s http://169.254.169.254/latest/meta-data/public-hostname for Public DNS name.
This is how your Web Book Register Application will look like in browser

![ Accessing our Book Register web application from the Internet with a browser using Public IP address or Public DNS name](./images/curl-command.png)

Book Register Application on the internet

![Testing our book register application on the web browser with our IP address on port 3300](./images/Book-Register-Application.png)




