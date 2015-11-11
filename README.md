#ServerPilot Vagrantfile

This repo contains a sample Vagrantfile to get up and running with a local development environment, managed by [ServerPilot](https://serverpilot.io).

##Requirements

* Install [VirtualBox](https://www.virtualbox.org)
* Install [Vagrant](http://www.vagrantup.com)

##Getting Started

* Clone this repo: `git clone git@github.com:dynamic/serverpilot-vagrantfile.git serverpilot`
* Navigate to new directory: `cd serverpilot`
* Fire up Vagrant: `vagrant up`
* Connect via SSH: `vagrant ssh`

##Install ServerPilot

* [Log in](https://manage.serverpilot.io/#login) to ServerPilot
* Go to the *Servers* page and click **+ Connect Server**
* Near the bottom of the screen, click *Install ServerPilot manually*
* Name your server and set a SFTP password
* Copy the command provided

![screen shot](assets/manual-install.png)

* Paste the command into your VM terminal to install ServerPilot
* Jump back to ServerPilot and watch the install progress

##Create an App

Once install is complete, click **+ Create App**

* Name your app (example)
* Set a domain name (example.dev)
* Choose PHP version
* Choose the server you just created (dynamic)
* Hit ***Create App***

![screen shot](assets/create-app.png)
	
Go to [192.168.33.10](http://192.168.33.10) in a browser and you should see the ServerPilot splash page

![screen shot](assets/splash-screen.png)

##Update Hosts File

*Optional*

To make it easier to host multiple apps on your Vagrant instance, you can update the hosts file with the domain you've set for your app.

In Terminal:

* `exit` if still connected to your Vagrant instance
* `sudo nano /etc/hosts` to open your hosts file
* At the end of your file, add `192.168.33.10	example.dev`
* Hit command-O to write, command-X to exit

In a browser, visit [example.dev](http://example.dev) and you should see the ServerPilot splash screen

##Create and Manage a Database

Since most modern php frameworks utilize databases, you'll want to create one for your project.

In your app, hit the ***Databases*** link and create a database.

![screen shot](assets/create-database.png)

ServerPilot does not provide a database management tool, but you can use any of the following tools for database management:

* [adminer](https://www.adminer.org)
* [phpmyadmin](https://www.phpmyadmin.net)
* [Sequel Pro](http://www.sequelpro.com)

Using Sequel Pro requires you to connect via SSH. Example settings are below:

![screen shot](assets/sequel-pro.png)

##Start Coding

Your Vagrant VM will create an `apps` folder inside of your `serverpilot` directory. Each time your create an app in ServerPilot, a webroot folder will be created here. To start working on your new example app, simply place your code in the following directory:

`serverpilot/apps/example.dev/public`

##Maintainer Contact

 *  Dynamic (<dev@dynamicagency.com>)

##Links

* [ServerPilot](https://serverpilot.io)
* [VirtualBox](https://www.virtualbox.org)
* [Vagrant](http://www.vagrantup.com)
* [Dynamic](http://www.dynamicagency.com)

##License
	Copyright (c) 2015, Dynamic, Inc.
	All rights reserved.

	Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

	Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
	
	Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
	
	THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.