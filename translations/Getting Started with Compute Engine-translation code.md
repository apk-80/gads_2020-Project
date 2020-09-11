## LAB Google Cloud Fundamentals: Getting Started with Compute Engine:


### OBJECTIVES:
In this lab, you learn how to perform the following tasks:

#### 1.Create a Compute Engine virtual machine using the Google Cloud Platform (GCP) Console.
#### 2.Create a Compute Engine virtual machine using the gcloud command-line interface.
#### 3.Connect between the two instances.
***

## Steps   
#### 1. Create a Compute Engine virtual machine using the Google Cloud Platform (GCP) Console.

 * gcloud compute instances create my-vm-1 --machine-type=e2-medium --subnet=default --tags=http-server --image=debian-9-stretch-v20200902 --zone=us-central1-a 

 * gcloud compute firewall-rules create default-allow-http --direction=INGRESS --network=default --action=ALLOW --rules=tcp:80 --source-ranges=0.0.0.0/0 --target-tags=http-server

#### 2. Create a Compute Engine virtual machine using the gcloud command-line interface.

 * cloud compute zones list | grep us-central1-b

 * gcloud compute instances create "my-vm-2" --machine-type "n1-standard-1" --image-project "debian-cloud" --image "debian-9-stretch-v20190213" --subnet "default"

####3. Connect between the two instances.
1. Use the ping command on the my-vm-2 instance through ssh, so that can be confirmed if my-vm-2 can reach my-vm-1:
 * **gcloud compute ssh my-vm-1**
 * **ping -c 4 my-vm-1**

2. Access my-vm-1 through ssh, to install the web server
 * **gcloud compute ssh my-vm-1**
 * **sudo apt-get install ngnix-light -y**
 
4. Use the nano text editor to add custm message
 * **sudo nano /var/www/html/index.nginx-debian.html**
 
5. Add text lie this and replace  YOUR_NAME with your name
 * **Hi from YOUR_NAME**
 
6. Confirm that the webserver is running. At command prompt of my-vm-1 run the following code:
 * **curl http://localhost**

7. Exit the command on the my-vm-1 runnign the code **exit** on my-vm-1 commmand prompt

8. To confirm that the my-vm-2 can reach the webserver on the my-vm-1, at the command prompt of my-vm-2, run this code:
 * **curl http://my-vm-1**

9. Copy the external IP from my-vm-1
 * **gcloud compute instances list**

10. Paste the copied IP address of my-vm-1 into the browser tab and click enter.