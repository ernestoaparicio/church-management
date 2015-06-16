# Church Management

## Requirements
Please install the following to work on church management:

1. VirtualBox https://www.virtualbox.org/
2. Vagrant https://www.vagrantup.com/
3. Node.js https://nodejs.org/

The first two pieces of software allow you to run a local virtual machine (VM). The third piece of software will allow you to build the front end software.

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
5. Assuming `node -v` returns valid data, type `npm install`. (You should see 
6. 
