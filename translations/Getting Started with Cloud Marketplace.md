## LAB Google Cloud Fundamentals: Getting Started with Cloud Marketplace

### OBJECTIVES:
In this lab get started with Cloud Marktplace, deploying

#### 1.Use Cloud Marketplace to deploy a LAMP stack
#### 2.Verify your deployment
***

## Steps
##### 1.Use Cloud marketplace to deply LAMP Stack
- This step is done inside the GCP console, on the Marketplace tab. 
- Using the search result for LAMP, the LAMP stack is shown and must be clicked for its deployment, where Compute Engine API must be initialized before coontinue.
- Remain teh settings by its defaults, after the GCP marketpalce Terms of Service aceepted, it can be deployed.

##### 2.Verify your deployment
- Clicking on the Site Address, you can visit the site and verify its deployment
- On the GCP client  click on SSH, change the  the currrenty directory:

*cd /opt/bitnami*

- copying the php.info script from the installation directory to a publicly accessible location:

*sudo sh -c 'echo "<?php phpinfo(); ?>" > apache2/htdocs/phpinfo.php'*

