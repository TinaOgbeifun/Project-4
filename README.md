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

vi server.js













![alt text](image.jpg)
![alt text](image.jpg)
![alt text](image.jpg)
