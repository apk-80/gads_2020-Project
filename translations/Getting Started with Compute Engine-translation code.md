## LAB Google Cloud Fundamentals: Getting Started with Compute Engine:


### OBJECTIVES:
In this lab, you learn how to perform the following tasks:

#####1. Create a Compute Engine virtual machine using the Google Cloud Platform (GCP) Console.
#####2. Create a Compute Engine virtual machine using the gcloud command-line interface.
#####3. Connect between the two instances.
***

###1. Create a Compute Engine virtual machine using the Google Cloud Platform (GCP) Console.

gcloud compute instances create my-vm-1 --machine-type=e2-medium --subnet=default --tags=http-server --image=debian-9-stretch-v20200902 --zone=us-central1-a 

gcloud compute firewall-rules create default-allow-http --direction=INGRESS --network=default --action=ALLOW --rules=tcp:80 --source-ranges=0.0.0.0/0 --target-tags=http-server

###2. Create a Compute Engine virtual machine using the gcloud command-line interface.

gcloud compute zones list | grep us-central1-b

gcloud compute instances create "my-vm-2" --machine-type "n1-standard-1" --image-project "debian-cloud" --image "debian-9-stretch-v20190213" --subnet "default"

###3. Connect between the two instances.
