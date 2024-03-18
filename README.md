Deploying a Node.js Application on AWS EC2
Testing the Project Locally
Clone this project:
bash
Copy code
git clone https://github.com/hassanhah/AWS-Session-.git
Set up the following environment variables in a .env file:
plaintext
Copy code
DOMAIN=""
PORT=3000
STATIC_DIR="./client"
PUBLISHABLE_KEY=""
SECRET_KEY=""
Initialize and start the project:
arduino
Copy code
npm install
npm run start
Setting Up an AWS EC2 Instance
Create an IAM user and log in to your AWS Console:

Access Type: Password
Permissions: Admin
Create an EC2 instance:

Select an OS image: Ubuntu
Create a new key pair and download the .pem file
Instance type: t2.micro
Connect to the instance using SSH:

css
Copy code
ssh -i instance.pem ubuntu@<IP_ADDRESS>
Configuring Ubuntu on Remote VM
Update the outdated packages and dependencies:
sql
Copy code
sudo apt update
Install Git - Guide by DigitalOcean

Configure Node.js and npm 

Deploying the Project on AWS
Clone this project in the remote VM:
bash
Copy code
git clone https://github.com/hassanhah/AWS-Session-.git
Set up the following environment variables in a .env file:
plaintext
Copy code
DOMAIN="http://18.232.138.141"
PORT=8000
STATIC_DIR="./client"
PUBLISHABLE_KEY=""
SECRET_KEY=""

For this project, we'll need to set up an Elastic IP Address for our EC2, and that will be our DOMAIN.

Initialize and start the project:
arduino
Copy code
npm install
npm run start
NOTE: We need to edit the inbound rules in the security group of our EC2 to allow traffic from our particular port.

Project is Deployed on AWS 🎉
