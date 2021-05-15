# Jenkins Documentation

## Introduction 

Continuous Integration is a software development practice in which developers are required to frequently commit changes to the source code in a shared repository. Each commit is then continuously pulled & built. Jenkins is an open source, Continuous Integration (CI) tool, written in Java. It continuously pulls, builds and tests any code commits made by a developer with the help of plugins.

## Installation
First we need an operating system ,mostly preferred linux based UBUNTU 20.04 and then <br>
Let’s start by installing Jenkins. This installation is specific to systems operating on Ubuntu. Follow the below steps:

<details><summary><b>STEPS</b></summary>

Step 1: Install Java
```
$ sudo apt update
$ sudo apt install openjdk-8-jdk
```

Step 2: Add Jenkins Repository
```
$ wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add –
```

Step 3: Add Jenkins repo to the system
```
$ sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
```

Step 4: Install Jenkins
```
$ sudo apt update
$ sudo apt install Jenkins
```

Step 5: Verify installation
``` 
$ systemctl status Jenkins
 ```

Step 6: Once Jenkins is up and running, access it from the link:
http://localhost:8080

Step 7: Then it asks for the installation of the resources and packages and set your admin credentials and then you are good to go

</details>


## Dashboard 

<p align="center">
<img src="https://1.bp.blogspot.com/-tV7SdU8H9wg/XrPX8DeO3KI/AAAAAAAADL8/A6S-gX6_DSU5DPgrVNSd-Zv4q25K7mTywCLcBGAsYHQ/s640/DevOpsArt-jenkins-plugin.PNG" width="350px" height=auto>
</p>
<!-- <details><summary><b>STEPS</b></summary>
</details> -->
<!--
<p align="center">
<img src="" width="350px" height=auto>
</p> -->

## Creating a New Job 
The freestyle build job is a highly flexible and easy-to-use option. You can use it for any type of project; it is easy to set up, and many of its options appear in other build jobs. Below is a step by step process to create job in Jenkin.

<details><summary><b>STEPS</b></summary>
1. Create New Item.

Click on "New Item" at the top left-hand side of your dashboard.
<p align="center">
<img src="https://www.guru99.com/images/1/091318_0458_HowtoCreate3.png" width="350px" height=auto>
</p>

2. Enter Item details

      In the next screen,
* Enter the name of the item you want to create. We shall use the "Hello world" for this demo.
* Select Freestyle project
* Click Okay
<p align="center">
<img src="https://www.guru99.com/images/1/091318_0458_HowtoCreate4.png" width="350px" height=auto>
</p>

3.  Enter Project details

      Enter the details of the project you want to test.
<p align="center">
<img src="https://www.guru99.com/images/1/091318_0458_HowtoCreate5.png" width="350px" height=auto>
</p>

4. Enter repository URL
<p align="center">
<img src="https://www.guru99.com/images/1/091318_0458_HowtoCreate6.png" width="350px" height=auto>
</p> 

5. Click Apply and Save Project and Build Source Code.
</details>

## Sonar Cloud & SonarQube Scanner 

1. Install the SonarScanner for Jenkins via the Jenkins Update Center.
2. Configure your SonarQube server(s):

      1. Log into Jenkins as an administrator and go to Manage Jenkins > Configure System.
      2. Scroll down to the SonarQube configuration section, click Add SonarQube, and add the values you're prompted for.
      3. The server authentication token should be created as a 'Secret Text' credential.

### Configuring a webhook secret
If you want to verify the webhook payload that is sent to Jenkins, you can add a secret to your webhook on SonarQube.

To set the secret:

1. In Jenkins, navigate to Manage Jenkins > Configure System > SonarQube Server > Advanced > Webhook Secret and click the Add button.
2. Select Secret text and give the secret an ID.
3. Select the secret from the dropdown menu.




