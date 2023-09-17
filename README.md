DEPLOYMENT 3: 
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
![image](https://github.com/DomIvey/Dep_3/assets/140740841/ba20d7a5-2624-4e94-b2b0-1f11704561dd)

 
5.	Created Jenkins server in EC2

6.	Installed the following packages: python3.10-venv", "python-pip", "unzip"

7.	Download Jenkins server using the public IP address from EC2 instance and put into web browser along with :8080
![image](https://github.com/DomIvey/Dep_3/assets/140740841/3efea4e2-3c4c-418a-92ae-ee7eaf5807e7)

 
8.	Created and ran a Jenkins build with a multibranch pipeline 
 ![image](https://github.com/DomIvey/Dep_3/assets/140740841/3126591c-b10e-4b2d-9abe-b12884a97926)


9.	Installed AWS EB CLI and AWS CLI

10.	Created EB url shortener: url-shortener-dev222222.us-east-1.elasticbeanstalk.com

11.	Added the following stage to Jenkins build: stage ('Deploy') { steps { sh '/var/lib/jenkins/.local/bin/eb deploy' } } 

12.	Reran Jenkins build

13.	Successfully configured a Webhook within Jenkins
 ![image](https://github.com/DomIvey/Dep_3/assets/140740841/a0850e6f-4881-4282-b59f-aaa3c4874fa7)



Issues:
•	I was unable to create the Jenkins server initially. I may have been using incorrect or outdated instructions. I closed out all of my tabs, restarted my computer, created a new instance, and ran the most current commands for creating a Jenkins server.
![image](https://github.com/DomIvey/Dep_3/assets/140740841/ec77bbf5-f117-423b-b175-ca915aca9416)

 

•	My Jenkins log said “Finished: SUCCESS”, however the build was still running. The Scan Repository Log kept spinning, and the Progress was not moving. I waited for about 20 minutes before refreshing and getting a successful message.
![image](https://github.com/DomIvey/Dep_3/assets/140740841/ac87a33f-b2ac-4670-8fd4-808966b46537)

 ![image](https://github.com/DomIvey/Dep_3/assets/140740841/556532eb-b36f-47e3-a2fa-6a944256b8ea)

 

•	Wasn’t able to create a new access key because it was grayed out (there can only be 2 keys at a time). I deleted the one that hadn’t been used and created a new key so that I could proceed to the next step.
![image](https://github.com/DomIvey/Dep_3/assets/140740841/1aba570e-b289-410a-a397-aff1d44217d3)


 
•	Once adding the new line of code to the Jenkins file, Jenkins no longer ran successfully. 
![image](https://github.com/DomIvey/Dep_3/assets/140740841/58c2f58e-10b3-4880-85a8-853847ced5e4)

 

•	The logs did not give a reason for the failure, however the Console Output stated the following:
 ![image](https://github.com/DomIvey/Dep_3/assets/140740841/182457a1-7e6f-48d2-ad92-69cef1f91fb6)


•	I went into the VS Code terminal to try and see if I could get a better understanding and maybe try to fix it from there, but this is not a git repository
 ![image](https://github.com/DomIvey/Dep_3/assets/140740841/8cf56f24-5b73-491c-960c-55911b6557ba)



Optimization (How I would make this deployment more efficient):
•	Have more information in the Jenkins log to stating why the build failed after adding the new stage
•	Better updates to Jenkins Scan Repository Log



System Diagram: 
 ![image](https://github.com/DomIvey/Dep_3/assets/140740841/4268b7bf-1817-4382-b317-78d6fa06d883)




 
 



 
 

