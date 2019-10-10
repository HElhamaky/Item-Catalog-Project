# Item Catalog Project

This is the secon project for the Udacity Full Stack Nanodegree. The Item Catalog project is about developing an application that provides a list of items within a variety of categories, as well as provide a user registration and authentication system. This project uses persistent data storage to create a RESTful web application that allows users to perform Create, Read, Update, and Delete operations.

A user does not need to be logged in in order to read the categories or items uploaded. However, users who created an item are the only users allowed to update or delete the item that they created.

This program uses third-party auth with Google. Some of the technologies used to build this application include Flask, Bootsrap, Jinja2, and SQLAlchemy.

## Features

- Proper authentication and authorisation check.
- Full CRUD support using SQLAlchemy and Flask.
- JSON endpoints.
- Implements oAuth using Google Sign-in API.

## Steps to run this project

1. Download and install [Vagrant](https://www.vagrantup.com/downloads.html).

2. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

3. Clone or download the Vagrant VM configuration file from [here](https://github.com/udacity/fullstack-nanodegree-vm).

4. Open the above directory and navigate to the `vagrant/` sub-directory.

5. Open terminal, and type ```vagrant up```, this will cause Vagrant to download the Ubuntu operating system and install it. This may take quite a while depending on how fast your Internet connection is.

6. After the above command succeeds, type ```vagrant ssh``` to connect to the newly created VM.
7. Type `cd /vagrant/` to navigate to the shared repository.

8. Download or clone  and extract this repository to ```vagrant/catalog``` directory (which will automatically be synced to ```/vagrant/catalog``` within the VM).

9. Set up the database using ```python database_setup.py```
10. ```python /vagrant/catalog/ItemCatalog.py``` to run this application.
11. Open `http://localhost:8000/` in your browser, and enjoy.

## Files and Folders

- ItemCatalog.py - this file runs the program, implements the CRUD functionality and
user authentication/registration
- database_setup.py - this file sets up the database structure
- items_catalog.db - contains the data
- static - contains the CSS files for the application
- templates - contains the HTML files and the layout for the application
- client_secrets.json - the dictionary for client id and secrets
- the Vagrant files
- this README.md file

## DataBase Tables

The database contains the following tables with the following columns:
- user: id(PK), name, email, picture
- category: id(PK), name, user_id(FK)
- item: id(PK), name, description, price, category_id(FK), user_id(FK)


## Citation and Attribution

In order to complete this project I have looked at some repositories, listed below.
* [item-catalog](https://github.com/ddavignon/item-catalog) by @ddavignon
* [Item-Catalog](https://github.com/SruthiV/Item-Catalog) by @SruthiV
* [Udacity-Item-Catalog-Project](https://github.com/SDey96/Udacity-Item-Catalog-Project) by @SDey96
* [Udacity-Full-Stack-Item-Catalog](https://github.com/anikolengyel/Udacity-Full-Stack-Item-Catalog) by @anikolengyel
