# Project-Linux-Server-Configuration
This is the final project under Udacity Full Stack Nanodegree course. The project composes of deploying a Flask application onto a Linux server with all the essential softwares installed.

## Project Overview
You will take a baseline installation of a Linux server and prepare it to host your web applications. You will secure your server from a number of attack vectors, install and configure a database server, and deploy one of your existing web applications onto it.

## Why this Project?
A deep understanding of exactly what your web applications are doing, how they are hosted, and the interactions between multiple systems are what define you as a Full Stack Web Developer. In this project, you’ll be responsible for turning a brand-new, bare bones, Linux server into the secure and efficient web application host your applications need.

## What will I Learn?
You will learn how to access, secure, and perform the initial configuration of a bare-bones Linux server. You will then learn how to install and configure a web and database server and actually host a web application

## Get started on Ligtsail
We're recommending Amazon Lightsail for this project. If you prefer, you can use any other service that gives you a publicly accessible Ubuntu Linux server. But Lightsail works pretty well and it's what we've tested.

There are a few things you need to do when you create your server instance.

1. Log in
First, log in to Lightsail. If you don't already have an Amazon Web Services account, you'll be prompted to create one. Amazon Web Services login page.

(https://camo.githubusercontent.com/b04c6f013ef9c3426fae8b913c556ed196cb0d58/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343566395f73637265656e2d73686f742d323031372d30322d31302d61742d31342e35392e33352f73637265656e2d73686f742d323031372d30322d31302d61742d31342e35392e33352e706e67)

Amazon Web Services login page.

2. Create an instance
Once you're logged in, Lightsail will give you a friendly message with a robot on it, prompting you to create an instance. A Lightsail instance is a Linux server running on a virtual machine inside an Amazon datacenter. When you have no instances, Lightsail gives you a picture of an orange robot and suggests that you create an instance.

[](https://camo.githubusercontent.com/889eb93426113892bd71cd2a7df6a6b093e9c030/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343561305f73637265656e2d73686f742d323031372d30322d31302d61742d31342e35382e31372f73637265656e2d73686f742d323031372d30322d31302d61742d31342e35382e31372e706e67)

When you have no instances, Lightsail gives you a picture of an orange robot and suggests that you create an instance.

3. Choose an instance image: Ubuntu
Lightsail supports a lot of different instance types. An instance image is a particular software setup, including an operating system and optionally built-in applications.

For this project, you'll want a plain Ubuntu Linux image. There are two settings to make here. First, choose "OS Only" (rather than "Apps + OS"). Second, choose Ubuntu as the operating system. When you create an instance, Lightsail asks what kind you want.For this project, choose an "OS Only" instance with Ubuntu.

(https://camo.githubusercontent.com/89e35431a70e578602b33830af5629f99a48e877/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343363365f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34362e31352f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34362e31352e706e67)

When you create an instance, Lightsail asks what kind you want. For this project, choose an "OS Only" instance with Ubuntu.

4. Choose your instance plan
The instance plan controls how powerful of a server you get. It also controls how much money they want to charge you. For this project, the lowest tier of instance is just fine. And as long as you complete the project within a month and shut your instance down, the price will be zero. Lightsail's options for instance pricing.For this project, pick the lowest one to get free-tier access. Lightsail's options for instance pricing. For this project, pick the lowest one to get free-tier access.

(https://camo.githubusercontent.com/1faac55eeff666e83e14ab80109efb7804204041/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343363615f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34362e33352f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34362e33352e706e67)

5. Give your instance a hostname
Every instance needs a unique hostname. You can use any name you like, as long as it doesn't have spaces or unusual characters in it. Your instance's name will be visible to you and to the project reviewer.

(https://camo.githubusercontent.com/7e46932122ccfbddcf03a015bdf0c715d0728935/68747470733a2f2f64313768323774366835313561352e636c6f756466726f6e742e6e65742f746f706865722f323031372f46656272756172792f35383965343363655f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34372e30382f73637265656e2d73686f742d323031372d30322d31302d61742d31342e34372e30382e706e67)

I've named my instance Udacity_Full_Stack.

6. Wait for it to start up.
It may take a few minutes for your instance to start up. While your instance is starting up, Lightsail shows you a grayed-out display.

While your instance is starting up, Lightsail shows you a grayed-out display.
Once your instance is running, the display gets brighter.

7. It's running; let's use it!
Once your instance has started up, you can log into it with SSH from your browser.

The public IP address of the instance is displayed along with its name. The big orange "Connect using SSH" button is the next step.

Explore the other tabs of this user interface to find the Lightsail firewall and other settings. You'll need to configure the Lightsail firewall as one step of the project.

When you SSH in, you'll be logged as the ubuntu user. When you want to execute commands as root, you'll need to use the sudo command to do it. Review sudo here if you need a refresher!

An SSH window logged into the server instance. From here, it's just like any other Linux server. An SSH window logged into the server instance. From here, it's just like any other Linux server.

8. Project time.
Now that you have a working instance, you can get right into the project.
