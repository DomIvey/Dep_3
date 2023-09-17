<P>DEPLOYMENT 3: 
Demonstrate your ability to create a fully automated Elastic Beanstalk deployment.

Purpose:
To demonstrate my ability to create a fully automated Elastic Beanstalk deployment.

Steps:
1.	Created GitHub repository which included a README.md file for documentation.

2.	Downloaded zip files and uploaded them to my repo:
o	Download zip files
o	Unzip into new folder in File Explorer
o	Go into the folder and select all files
o	Copy and paste, or drag files into GH repo
o	Commit changes (save)

3.	Created instance in AWS

4.	Created public and private SSH keys to log into AWS. Was able to access EC2 from local terminal

 

5.	Created Jenkins server in EC2

6.	Installed the following packages: python3.10-venv", "python-pip", "unzip"

7.	Download Jenkins server using the public IP address from EC2 instance and put into web browser along with :8080

 


8.	Created and ran a Jenkins build with a multibranch pipeline 
 

9.	Installed AWS EB CLI and AWS CLI

10.	Created EB url shortener: url-shortener-dev222222.us-east-1.elasticbeanstalk.com

11.	Added the following stage to Jenkins build: stage ('Deploy') { steps { sh '/var/lib/jenkins/.local/bin/eb deploy' } } 

12.	Reran Jenkins build

13.	Successfully configured a Webhook within Jenkins
 

Issues:
•	I was unable to create the Jenkins server initially. I may have been using incorrect or outdated instructions. I closed out all of my tabs, restarted my computer, created a new instance, and ran the most current commands for creating a Jenkins server.

 

•	My Jenkins log said “Finished: SUCCESS”, however the build was still running. The Scan Repository Log kept spinning, and the Progress was not moving. I waited for about 20 minutes before refreshing and getting a successful message.

 
 


•	Wasn’t able to create a new access key because it was grayed out (there can only be 2 keys at a time). I deleted the one that hadn’t been used and created a new key so that I could proceed to the next step.

 
•	Once adding the new line of code to the Jenkins file, Jenkins no longer ran successfully. 

 

•	The logs did not give a reason for the failure, however the Console Output stated the following:
 

•	I went into the VS Code terminal to try and see if I could get a better understanding and maybe try to fix it from there, but this is not a git repository
 

Optimization (How I would make this deployment more efficient):
•	Have more information in the Jenkins log to stating why the build failed after adding the new stage
•	Better updates to Jenkins Scan Repository Log

System Diagram: 
 



 
 



 
 

