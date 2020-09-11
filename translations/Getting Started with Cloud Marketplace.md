## LAB Google Cloud Fundamentals: Getting Started with Cloud Marketplace

### OBJECTIVES:
In this lab get started with Cloud Marktplace, deploying

#### 1.Use Cloud Marketplace to deploy a LAMP stack
#### 2.Verify your deployment
***

## Steps
#### 1.Use Cloud marketplace to deply LAMP Stack
1. This step is done inside the GCP console UI, on the Marketplace tab. 
2. With the search result for LAMP, the LAMP stack is shown and must be clicked for its deployment, where Compute Engine API must be initialized before continue.
3. Selecting the Zone assign to your qwuiklabs.
4. Remain the settings by its defaults, after the GCP marketpalce Terms of Service aceepted, the LAMP can be deployed.
5. The Welcome to Deployment Manager essage can be closed
6. The status of the LAMP deployment appers on the console
7. After the software deployed, a summary of the details including the address is displayed

#### 2.Verify your deployment
1. Clicking on the Site Address, the vdeployed site can be visited.
2. Closed the congratulation tab
3. On the GCP console, get started with the LAMP clicking on the ssh button
4. On the new windows, a secure login shell appers on the vm
5. The current working directory can be changed with the following commands:

**cd /opt/bitnami**

- copying the *php.info* script from the installation directory to a publicly accessible location under the webserver document root, use the code:

**sudo sh -c 'echo "<?php phpinfo(); ?>" > apache2/htdocs/phpinfo.php'**

- the *phpinfo.php* displays the PHp configuration
- -you can use the command *exit* to close the ssh window
