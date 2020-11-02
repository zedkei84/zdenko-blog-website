---
date: 2020-11-02 15:00:00
title: Install Jenkins on Ubuntu 20.04
categories:
  - jenkins
description: How to install Jenkins on Ubuntu 20.04
type: Document
---
## What is Jenkins?

Jenkins is a self-contained, open source automation server which can be used to automate all sorts of tasks related to building, testing, and delivering or deploying software.

Jenkins can be installed through native system packages, Docker, or even run standalone by any machine with a Java Runtime Environment (JRE) installed.

### Prerequisites

 - Minimum hardware requirements:
   
    256 MB of RAM
    
    1 GB of drive space (although 10 GB is a recommended minimum if running Jenkins as a Docker container)

 - Recommended hardware configuration for a small team:
  
    1 GB+ of RAM

    50 GB+ of drive space

 - JAVA installed

Check with:
~~~ bash
java -version
~~~

If JAVA is not installed, install it:
~~~ bash
sudo apt install openjdk-11-jre-headless -y
~~~

## How to install Jenkins via its official repository

~~~ bash
# import Jenkins GPG key
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -

# update APT sources.list with the Jenkins repository
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'

# update package list
sudo apt-get update -y

# install Jenkins
sudo apt-get install jenkins -y

# check Jenkins status
sudo systemctl status jenkins

# start Jenkins, if not running
sudo systemctl start jenkins
~~~
