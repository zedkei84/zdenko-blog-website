---
date: 2020-10-15 00:00:00
title: Install kubelogin on WSL
categories:
  - kubernetes
description: Jekyll template for digital agencies
type: Video
---
## What is Jenkins?

Jenkins is a self-contained, open source automation server which can be used to automate all sorts of tasks related to building, testing, and delivering or deploying software.

Jenkins can be installed through native system packages, Docker, or even run standalone by any machine with a Java Runtime Environment (JRE) installed.

### Prerequisites

JAVA installed.

Check with:

~~~ bash
java -version
~~~

If JAVA not installed, install it:

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
sudo apt update -y

# install Jenkins
sudo apt install jenkins -y

# check Jenkins status
sudo systemctl status jenkins

# start Jenkins, if not running
sudo systemctl start jenkins
~~~
