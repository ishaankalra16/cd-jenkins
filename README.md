# Vprofile-project

A demo application integrated, tested and analysed with the tools such as Jenkins, Nexus, SonarQube that send every notification to desired slack regarding every build of the pipeline. 

# Prerequisites
# 
- JDK 1.8 or later
- Maven 3 or later
- MySQL 5.6 or later

# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- MySQL

# Architecture

<img width="676" alt="Screenshot (363)" src="https://user-images.githubusercontent.com/68735863/152752972-c1740664-1491-4510-9ad3-5133381da907.png">

# Flow of Execution

- Login to AWS Console
- Create Login key pair for the EC2 Instances
- Create Security Group
  - Jenkins
  - Nexus
  - Sonarqube
- Create EC2 Instances with the userdata
  - Jenkins
  - Sonarqube
  - Nexus
- Configuring Jenkins and installing the required plugins
- Nexus Repository Setup
  - Release Version repository
  - Central repository for dependencies
  - Snapshot
  - Group repository 
- Sonarqube Post installation
- Jenkins Steps
  - Build Job
  - Setup Slack Notification
  - Checkstyle Code Analysis Job
  - Sonarqube Code Analysis Job
  - Artifact upload Job
- Connect all Jobs together with Build Pipeline
- Set Automatic Build Trigger
- Create Security Groups
  - Windows Server
  - Tomcat Server
 - Setup Tomcat & backup server on ec2 with userdata
- Create Jenkins job and deploy artifact to staging
- Add windows node as slave to Jenkins
- Create Job to run Software Tests(Selenium) from Windows Server
- Deploy artifact to Porduction Server
- Connect all Jobs with Build Pipeline
- 

# Database
Here,we used Mysql DB 
MSQL DB Installation Steps for Linux ubuntu 14.04:
- $ sudo apt-get update
- $ sudo apt-get install mysql-server

Then look for the file :
- /src/main/resources/accountsdb
- accountsdb.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < accountsdb.sql

# Screenshots

![Screenshot (364)](https://user-images.githubusercontent.com/68735863/152753022-26188c53-f3f5-4c22-92ea-ddd9b7e48dab.png)

![Screenshot (365)](https://user-images.githubusercontent.com/68735863/152753041-10989ed0-efd6-48bf-b1b8-3f17abc1f971.png)

![Screenshot (366)](https://user-images.githubusercontent.com/68735863/152753080-34c2ca87-4f3a-479c-acb3-3061e8caa06d.png)

![Screenshot (368)](https://user-images.githubusercontent.com/68735863/152753113-1c58b00b-8e06-4359-8a2f-f91fe3b8bf3e.png)

![Screenshot (369)](https://user-images.githubusercontent.com/68735863/152753156-90a9747b-b8c5-41dc-adbe-f1402a796fa0.png)

![Screenshot (370)](https://user-images.githubusercontent.com/68735863/152753191-07a4f8ab-2da7-4c3d-bd2c-266c32057750.png)

![Screenshot (371)](https://user-images.githubusercontent.com/68735863/152753208-a2fcde65-c8df-41de-9e7c-797ab41d19e5.png)

![Screenshot (372)](https://user-images.githubusercontent.com/68735863/152753233-ec36f2a0-3e62-4328-ba5d-76b318e02c80.png)

![Screenshot (373)](https://user-images.githubusercontent.com/68735863/152753269-fbddb010-c886-407a-a04d-b6fc5ec52a28.png)

![Screenshot (374)](https://user-images.githubusercontent.com/68735863/152753298-28c657f0-cc09-4a14-9faa-fb8785661a6e.png)

![Screenshot (375)](https://user-images.githubusercontent.com/68735863/152753325-5cc26466-6d27-4318-8b0a-a57702b4b986.png)

![Screenshot (376)](https://user-images.githubusercontent.com/68735863/152753353-537428b1-d724-471c-b9d4-5c6b1369d70f.png)

![Screenshot (377)](https://user-images.githubusercontent.com/68735863/152753385-66a5f3bd-d913-4ad0-adc9-782e0a22216a.png)

![Screenshot (378)](https://user-images.githubusercontent.com/68735863/152753407-1e2c2b82-16b2-4f67-b758-5c2a57ee1f28.png)

![Screenshot (379)](https://user-images.githubusercontent.com/68735863/152753428-442494df-ecb6-4f4e-914c-0a8121a18946.png)



