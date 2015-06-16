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
