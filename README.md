# R-Server
Install an Run R server
Install and Run R Server
1.	In the AWS Services menu, Click EC2
2.	Click Launch Instance
3.	In the row for Amazon Linux AMI 2017.09.1(HVM), SSD volume type Click Select
4.	Confirm that the t2.micro instance type is selected
5.	Click Configure Instance Details
6.	Scroll down and click the Advanced Details Heading to expand it
7.	Copy the following text and paste it into the user data text box:
#!/bin/bash 
#install R 
yum install -y R 
wget https://download2.rstudio.org/rstudio-server-rhel-1.1.383-x86_64.rpm 
yum install -y --nogpgcheck rstudio-server-rhel-1.1.383-x86_64.rpm
 
8.	Click Add storage
9.	Click Add Tags
 
10.	Click Next: Configure security Group
 
11.	Click Add Rule
In the bottom row in port add 8787(for R server)
12.	Click Review and Launch
 
 
13.	Connected to my instance using putty
sudo useradd username  echo username:password | sudo chpasswd
sudo useradd jyostna echo jyostna:pereira | sudo chpasswd
14.	Then u can connect to your instance by copy pasting  
http://ec2-34-241-42-6.eu-west-1.compute.amazonaws.com:8787/ 
 
Use the user name and password u have created.   

