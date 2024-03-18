# Deploying a Node.js Application on AWS EC2

## Testing the Project Locally

1. **Clone this project:**
    ```bash
    git clone https://github.com/hassanhah/AWS-Session-.git
    ```

2. **Set up the following environment variables in a `.env` file:**
    ```plaintext
    DOMAIN=""
    PORT=3000
    STATIC_DIR="./client"
    PUBLISHABLE_KEY=""
    SECRET_KEY=""
    ```

3. **Initialize and start the project:**
    ```bash
    npm install
    npm run start
    ```

## Setting Up an AWS EC2 Instance

1. **Create an IAM user and log in to your AWS Console:**
    - Access Type: Password
    - Permissions: Admin

2. **Create an EC2 instance:**
    - Select an OS image: Ubuntu
    - Create a new key pair and download the `.pem` file
    - Instance type: t2.micro

3. **Connect to the instance using SSH:**
    ```bash
    ssh -i instance.pem ubuntu@<IP_ADDRESS>
    ```

## Configuring Ubuntu on Remote VM

1. **Update the outdated packages and dependencies:**
    ```bash
    sudo apt update
    ```

2. **Install Git -** [Guide by DigitalOcean]

3. **Configure Node.js and npm**

## Deploying the Project on AWS

1. **Clone this project in the remote VM:**
    ```bash
    git clone https://github.com/hassanhah/AWS-Session-.git
    ```

2. **Set up the following environment variables in a `.env` file:**
    ```plaintext
    DOMAIN="http://18.232.138.141"
    PORT=8000
    STATIC_DIR="./client"
    PUBLISHABLE_KEY=""
    SECRET_KEY=""
    ```
    For this project, we'll need to set up an Elastic IP Address for our EC2, and that will be our DOMAIN.

3. **Initialize and start the project:**
    ```bash
    npm install
    npm run start
    ```

   **NOTE:** We need to edit the inbound rules in the security group of our EC2 to allow traffic from our particular port.

### Project is Deployed on AWS 🎉
