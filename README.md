# SCUTICOMMERCE - Shopping Cart with MEAN STACK (eCommerce web application)
A single page Shopping Cart web applications with many necessary features of an ecommerce application.


# Requirements
Install the following 2 softwares

1.    Node http://nodejs.org/ (Server)
2.    MongoDB https://www.mongodb.org/ (Database)

# Install
Run the following commands and the application will start automatically

1.    npm install yo -g (Install yeoman for scaffolding web application)
2.    npm install grunt-cli -g (This creates and runs javascript repetative tasks )
3.    npm install bower -g ( A frontend package manager for web applications)
4.    npm install (Install all nodejs dependencies, also automatically installs bower components)
5.    grunt serve

# Features
### Store Front features
*  Single page web app (SPA) created using AngularJS, NodeJS, Express, MongoDB (MEAN)
*  Fastest shop experience
*  Fast Product Search, Filter with AJAX
*  Price slider and multiple brand selector
*  Faster Add to Cart and Product Details
*  Checkout with Paypal Integration
*  Minimal User Registration process
*  Order history and Password Management
*  Facility for Multi level Category
*  Mobile optimized with Bootstrap
*  Instant updates for any changes made across all clients with SocketIO implementation
*  Loads more products on scroll (No paging required)

### Store Back Office
*  Products, Categories, Brand, Order Management from admin panel with easy directives
*  Manage Order and Change Status from admin panel
*  Facility for Multiple product variants (size, color, price, image)
*  User roles - Administrator, User, Guest
*  SEO friendly URLs for each page
*  Secure and quality code - Takes care all single page web app standards




/Users/kapilkataria/scuti_products/mongodb/bin/mongoexport --db scuti-dev --collection products --out products.json
/Users/kapilkataria/scuti_products/mongodb/bin/mongoexport --db scuti-dev --collection categories --out categories.json
/Users/kapilkataria/scuti_products/mongodb/bin/mongoexport --db scuti-dev --collection brands --out brands.json
/Users/kapilkataria/scuti_products/mongodb/bin/mongoexport --db scuti-dev --collection orders --out orders.json


/Users/kapilkataria/scuti_products/mongodb/bin/mongoimport --db scuti-dev --collection products --file /Users/kapilkataria/scuti_products/scuticommerce-ecommerce/sample_data/products.json
/Users/kapilkataria/scuti_products/mongodb/bin/mongoimport --db scuti-dev --collection categories --file /Users/kapilkataria/scuti_products/scuticommerce-ecommerce/sample_data/categories.json
/Users/kapilkataria/scuti_products/mongodb/bin/mongoimport --db scuti-dev --collection brands --file /Users/kapilkataria/scuti_products/scuticommerce-ecommerce/sample_data/brands.json
/Users/kapilkataria/scuti_products/mongodb/bin/mongoimport --db scuti-dev --collection orders --file /Users/kapilkataria/scuti_products/scuticommerce-ecommerce/sample_data/orders.json

db.brands.find().forEach(function(d){ db.getSiblingDB('scuti')['brands'].insert(d); });
db.categories.find().forEach(function(d){ db.getSiblingDB('scuti')['categories'].insert(d); });
db.products.find().forEach(function(d){ db.getSiblingDB('scuti')['products'].insert(d); });
db.orders.find().forEach(function(d){ db.getSiblingDB('scuti')['orders'].insert(d); });
# scuticommerce-ecommerce
