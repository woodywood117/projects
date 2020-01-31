# Password Manager #
This project will consist of the multiple steps it takes to build
a password manager from scratch. This password manager will be usable from both the command-line
as well as from a web interface, while also being adaptable to other interfaces.

## Step One ##
For this step, we're going to create the core building block on which a password manager relies, passwords.
Create a set of functions that can perform the following operations on password objects:
* Create a password object
* Save a password object to some database
* Update a saved password object in some database
* List all password objects in some database
* Return all information about a password object
* Delete a password object from some database

These password objects should have at least (but is not limited to) the following attributes:
* ID
* Name
* URL
* Username
* Password
* Owner
* Description
* A list of users it is shared with

When doing this step, create a command-line interface that allows a user to call each of the functions mentioned above.
It should allow for a user to type in a command that should be named based on the function it will call,
and then the interface should gather any necessary information that it needs for the corresponding function.

One thing to keep in mind for this step is that "some database" can mean any method of storing data.
This can mean saving the information to a file or a more traditional database like Postgres.
Don't couple your program too tightly to the database, it could always change later.

## Step Two ##
In this step, we're going to create a method for grouping password objects together.
Create a set of functions that can perform the following operations on a password group:
* Create a password group
* Add a password to a password group
* Remove a password from a password group
* Save a password group to some database
* List all password groups
* Delete a password group
* Return all information about a password group

These password groups should have at least (but is not limited to) the following attributes:
* ID
* Name
* Description
* A list of password objects
* A list of users it is shared with

All of these operations should use the password objects from step one, rather than using the password strings themselves.

When doing this step extend the command-line interface from step one. Add commands the same was as before,
but for the newly added functions.

## Step Three ## 
In this step we're going to add a new interface to the program.
Create a REST interface for the program. It should have HTTP routes for all of the functionality mentioned in the previous two steps.

Once you've done this, alter your command-line interface to use the REST API that you've just created. You can optionally create a web interface the uses the REST API if you'd like a visual way of managing the program.

## Step Four ##
In this step, we're going to implement configuration files into the application.
Create the ability to have the program read in configuration variables at startup from some text file in any encoding of your choice.
(JSON, YAML, TOML, INI)

Once the program has the ability to read in these values at startup, go through the rest of the program removing any hard-coded values and replace them with configuration variables.
While performing this step, remember that it is better to pass a variable in via parameters than accessing some global program state.
