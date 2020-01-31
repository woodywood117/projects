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
* Delete a password object from some database

These password objects should have at least (but is not limited to) the following attributes:
* ID
* Name
* URL
* Username
* Password
* Owner
* Description

## Step Two ##
Create a method for grouping password objects.
