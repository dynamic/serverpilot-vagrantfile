#ServerPilot Vagrantfile

This repo contains a sample Vagrantfile to get up and running with a local development environment, managed by [ServerPilot](https://serverpilot.io).

##Requirements

* Install [VirtualBox](https://www.virtualbox.org)
* Install [Vagrant](http://www.vagrantup.com)

##Getting Started

Clone this repo:

`git clone git@github.com:dynamic/serverpilot-vagrantfile.git serverpilot`

Navigate to new directory:

`cd serverpilot`

Fire up Vagrant:

`vagrant up`

Connect via SSH:

`vagrant ssh`

##Install ServerPilot

* [Log in](https://manage.serverpilot.io/#login) to ServerPilot
* Go to the *Servers* page and click **+ Connect Server**
* Near the bottom of the screen, click *Install ServerPilot manually*
* Name your server and set a SFTP password
* Copy the command provided

![screen shot](assets/manual-install.png)

* Paste the command into your VM terminal to install ServerPilot

##Create an App



  
