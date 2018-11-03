# "Item Catalog" - Item Catalog Web Application

This webiste aims to display a catalog containing a list of categories with their related items using Python data structures. A list of categories and latest added items are displayed and by clicking on any of the categories, a list of items for this  category are displayed. Users can log in to this website by using third-party login with either their Google account or Facebook account. Also, A user does not need to be logged in order to view the categories or items in the catalog. However, only authenticated users have the ability to add, edit, and delete their own items. This project was done as a part of the Full Stack Web Developer Nanodegree on [Udacity](https://www.udacity.com/course/full-stack-web-developer-nanodegree--nd004)

## Project Setup

To set up the environment for the project, you must download [Python](https://www.python.org/downloads) and it is recommended to download version 2.7 or above, as any other version may not be compatible with the code. It's supported for Windows, Linux/UNIX, Mac OS X, and other operating systems.

This project uses technologies like Flask, SQLite, OAuth and SQLAlchemy

## To run this project

1. Install [Vagrant](https://www.vagrantup.com/) and [Virtual Box](https://www.virtualbox.org/)
2. Download the project ZIP file or clone it to your local machine by clicking on the green "Clone or download" button on the upper right side of the page
`or`
clone it to your local machine using Git's command line
```
git clone https://github.com/dalia-maher/Item-Catalog
```
3. Put the cloned directory of the repo in vagrant folder inside the Virtual Machine. You can use [Udacity](https://github.com/udacity/fullstack-nanodegree-vm) VM
4. Open the terminal and change directory to vagrant
```
cd /vagrant
```
5. Launch the Vagrant VM by typing this command
```
vagrant up
```
6. Access the Shell by typing:
```
vagrant ssh
``` 
7. change directory to the catalog folder
```
cd Item-Catalog
``` 
8. Run the application
```
python application.py
``` 
9. After the last command, you will be able to browse the application at this URL: http://localhost:5000/


## Project Functionalities

1. You can find a list of different categories and latest items added to all categories.
2. Clicking on the category should display the items inside this category.
3. Clicking on the "Login" button in the upper right in the navigation bar should display login page with two login options (Google and Facebook).
4. After logging in to the website, you can find "New" button beside categories to add new category.
5. You can also find "Add Item" button beside items to add a new catalog item.
6. Logged in users can only edit and delete the categories and items which they created.
7. Edit and Delete buttons should appear beside the user's own categories.
8. Clicking on any item should display this item's info and if the user is allowed to edit or delete this item, two buttons will be shown on the bottom left for editing or deleting this item.
9. Deleting an item or category should display a confirmation page to the user to confirm their deletion.
10. Users can add items to other categories which they don't really own.
11. JSON endpoints can be used to display the catalog info in JSON format as follows:
- JSON API for Catalog information
```
http://localhost:5000/catalog.json
```
- JSON API for Category information
```
http://localhost:5000/categories/JSON
```
- JSON API for Catalog Item information
```
http://localhost:5000/categories/<int:category_id>/item/<int:catalog_item_id>/JSON
```

## Project Contents

### database-setup.py:
Python module that sets up the database classes and relations of User, Category and CatalogItem. It uses SqLite DB.

### application.py:
Python module containing the business login of the whole project including login, connection to database, JSON APIs, and the main functionalities of each endpoint in the application.

### templates:
Contains HTML Pages used in this application.

### static:
Contains the required css, js and other assets for design.
