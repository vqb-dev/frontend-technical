## Visual Quiz builder

[[_TOC_]]

---

:scroll: **START**


### Introduction

Shopping has never been easier with e-commerce.
Consumers use different web applications to search **products** and purchase them anywhere and anytime.

---

### Task description

We are tasked with developing a small web application for managing **products** and **cart** information.

The **product** looks like:
```json
{
  "id": 3,
  "title": "Mens Cotton Jacket",
  "price": 55.99,
  "description": "great outerwear jackets for Spring/Autumn/Winter, suitable for many occasions, such as working, hiking, camping, mountain/rock climbing, cycling, traveling or other outdoors. Good gift choice for you or your family member. A warm hearted love to Father, husband or son in this thanksgiving or Christmas Day.",
  "category": "men's clothing",
  "image": "https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg",
  "rating": {
      "rate": 4.7,
      "count": 500
    }
}

```

The **cart** looks like:
```json
[
    {
      "id": 3,
      "title": "Mens Cotton Jacket",
      "price": 55.99,
      "image": "https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg",
      "quantity": 1
    }
]
```

The **user** has:
- name: user's name
- email: user's email 
- password: user's password 

Create a web application **(front-end only)** in Typescript and React to display and search the product data, and add products to the cart, integrating with the REST API of the provided server (see below how to run the server). 

You can use any react component library or CSS framework you prefer. Please give it a nice and consistent look and feel.

#### How to run the server

Install the server using npm. Node version `14.15` or greater is required

```bash
npm install @vqb/products-server --save-dev
```

Add it to the scripts section of your package.json

```json
{
  "scripts": {
    "server": "products-server"
  }
}
```

If you have added the server in the scripts section, you can run it with `npm run server`. Alternatively, you can run it with `npx products-server`

Check the webpage that opens automatically in your browser for more instructions on how to configure the server (by default http://localhost:3000) and its API documentation.

By default, even though some endpoints require authentication, they can be accessed without it. You can start development without using the authentication. We have some requirements below, where authentication is needed, so to enable authentication on the server, it can be run by adding `--auth` parameter like `products-server --auth`. Also, to simulate async processing, the server can be run with `--async` parameter like `products-server --async`.

Please check carefully the API documentation and request parameters. The documentation is self-explanatory, but could you make sure you check the details? For example:
```bash
GET /products
```
provides you the option to send paging requests. 

For full configuration options of the server, check the webpage that opens automatically.


### Requirements

Make sure you read all of the requirements to get full information on the task's expectations. Even though the list of items seems long, once you read it all, you will notice that they are related and the list just helps you to easily finish the task. Then try to complete the following features one after another in order (recommended but not necessary). 

The features are grouped into different categories. The features marked as **required** are the bare minimum necessary to qualify,
the **nice to have** increase your score and the **specials** will surely demonstrate your talent.

#### Required features

1. Create a web page to display the list of product cards showing `title`, `image`, `category` and `price` of each product.
2. Create an `Add to cart` button attached to each product item.
3. Create a search bar that allows for searching the products and a search page for the results items, and display an empty response message if no products were found.
4. Validate the parameters just added in the URL to match the format accepted by the server for the page (and page size) and redirect to a "Bad request" page in case the parameters are invalid.
5. Create a separate page that displays the product information when a product is clicked.
6. A URL should be changed for each product page e.g. `/products/<product_id>`.
7. Create a cart button in the header toolbar with a bubble indicator to show how many products are in the cart.
8. Create a cart page/popover to display the current products in the cart and give the ability to change product quantity and delete them from the cart.
9. If the user tries to add to their cart a quantity of product that exceeds the product `stock`, display an error.
10. Make sure the page is responsive and looks good on mobile and tablet. 

#### Nice to have features

1. Add a progress bar on indefinite status or loader to this product card when adding to the cart.
2. List the products by categories
3. Add a navigation control that allows to change pages (optionally also to change the number of items per page).
4. If a product's `stock` is 0 then the product should be marked as unavailable
5. When the user types in the search bar wait a few seconds after stopping typing to update the url and send the request to the server.
6. Add a register screen that allows to creation of new users with `name`, `email` and `password` fields.
7. Add a login screen that allows to authenticate the user with `email` and `password`.
8. Enable security on the server and make all your requests authenticated. Do not allow access to the application to users that are not registered.
9. Add a toolbar on top of your authenticated page showing the authenticated user with a menu with an option to log out. Make sure error pages also have this toolbar.
10. Create dark and light modes for your app. You can put the switcher in the toolbar.

#### Special features

1. When the security credentials are expired redirect the user to the login screen.
2. Automatically refresh the tokens when they expire without logging out the user.
3. Create E2E tests for the various features
4. Add one unit test that checks your page with mocked data from the server works.

---
:scroll: **END**
