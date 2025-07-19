## **Exercise 3.1: Deploy a New Application**

In this lab we will deploy a very simple **Python** application, test it using **Podman**, ingest it into **Kubernetes** and con-figure **probes** to ensure it continues to run.  This lab requires the completion of the previous lab, the installation and configuration of a **Kubernetes cluster**.Note that **Podman** and **crictl** use the same syntax as **docker**, so the labs should work the same way if you happen to be using Docker instead.

### **Working with A Simple Python Script**
---
- Install python on my cp node. 

Run : `sudo apt-get -y install python3`

- Locate the python binary on my system.

Run : ̃`which python3`

![install python](./Images/install%20python.PNG)

- Create and change into a new directory. The **Podman** build process pulls everything from the current directory into the image file by default. Make sure the chosen directory is empty.

Run : `mkdir app1`

Run : `cd app1`

Run :  `ls -l`

![mkdir app1](./Images/mkdir%20app1.PNG)

- Create a simple python script which prints the time and hostname every 5 seconds. There are six commented parts tothis script, which should explain what each part is meant to do.  The script is included with others in the course tar file,you may consider using thefindcommand used before to find and copy over the file.While the command showsvimas an example other text editors such asnanowork just as well.

Run : `vim simple.py`
