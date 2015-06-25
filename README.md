# Church Management

## Table of Contents
1. <a href="https://github.com/saddlebackdev/church-management#requirements">Requirements</a>
2. <a href="">Recommended Tools</a>
3. <a href="https://github.com/saddlebackdev/church-management#installing-environment">Installing Environment</a>
4. <a href="https://github.com/saddlebackdev/church-management#architecture">Architecture</a>
5. <a href="https://github.com/saddlebackdev/church-management#front-end-development">Front End Development</a>

## Requirements
Please install the following to work on church management:

1. VirtualBox. <a href="https://www.virtualbox.org/">https://www.virtualbox.org/</a>
2. Vagrant. <a href="https://www.vagrantup.com/">https://www.vagrantup.com/</a>
3. Node.js. <a href="https://nodejs.org/">https://nodejs.org/</a>

The first two pieces of software allow you to run a local virtual machine (VM). The third piece of software will allow you to build the front end software.

## Recommended Tools

1. Sublime Text. <a href="http://www.sublimetext.com/">http://www.sublimetext.com/</a>. Great editor for Javascript codebases.

## Installing Environment
To get a local development environment going, we will first need to download the command and control executable.

For Windows users, paste this link into a browser:

  https://github.com/saddlebackdev/church-management/raw/master/windows-client/cm-control.exe
  
For OS X users, paste this link into a browser (or use wget):

  https://github.com/saddlebackdev/church-management/raw/master/osx-client/cm-control
  
After downloading the command and control application, you'll need to email <a href="mailto:rmeyer@saddleback.com">rmeyer@saddleback.com</a> with your public IP address so we can add it to our whitelist. The IP should be available from the command and control menu.

Once you are whitelisted, you can select 'i' from the menu to install the virtual machine.

If everything goes well, after 10-15 minutes, you should have the API and database running locally inside of a VirtualBox VM.
  

## Architecture
The church management product is a single page application (SPA) that is primarily written in Javascript. The SPA communicates with a RESTful API to read and write data. All data is persisted in a database.

The three layers in more detail:

**Single Page Application**

We use React (http://facebook.github.io/react/) as the primary technology for our application. 

**RESTful API**

The API is written in C#. Specifically we are using .NET 5.0 which is also called "dnx" or "vNext". (https://github.com/aspnet/home)

**Database**

We picked Postgres as our database. (https://en.wikipedia.org/?title=PostgreSQL)

All the layers run in Linux and more specifically on the Debian/Wheezy distribution. Additionally we use Docker to containerize each layer. The API and database both reside in their own containers.

## Front End Development
To contribute to the front end codebase you'll need to get a few things installed first.

1. Node.js (https://nodejs.org/)
2. A good editor/IDE for Javascript development. We recommend Sublime Text (http://www.sublimetext.com/).
3. A git client. We have had good luck with the Github client (https://windows.github.com/, https://mac.github.com/).

After getting the software installed you'll need to do the following to begin to actually write code:

1. Create a Github account if you don't have one and communicate your Github username to the Church Management team.
2. After you've been added to the private repository, you'll need to `fork` the repository.
3. Now you'll need to `clone` your forked repository to your local machine. You can use the Github client for example to do this.
4. Open a command prompt/the console and navigate to the directory where you cloned the repository.
5. Assuming `node -v` returns valid data, type `npm install`. This will install all dependencies.
6. Now type `npm start` to run the application. 

When the above steps are completed, you should be able to go to `http://localhost:8080` to see the application running. If that doesn't work, go to the Troubleshooting section.
