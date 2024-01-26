## Visual Quiz builder

[[_TOC_]]

---

:scroll: **START**


### Introduction

Shopping has never been easier with ecommerce.
Consumers use different web applications in order to search **products** and purchase them anywhere and anytime.

---

### Task description

We are tasked with developing a small web application for managing **products** and **cart** information.

The **product** looks like:
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

The **cart** looks like:
```json
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
```

The **user** has:
- name: user's name
- email: user's email 
- password: user's password 

Create a web application **(front-end only)** in your typescript and react to display and search the products data, and adding products to cart, integrating with the REST API of the provided server (see below how to run the server). 

You can use any component library or css framework you prefer. Give it a nice and consistent look and feel.

#### How to run the server

Install the server using npm. Node version `14.15` or greater is required

```bash
npm install @vqb/products-server --save-dev
```

Add it to the scripts section of your package.json

```json
{
  "scripts": {
    "server": "vqb-products-server"
  }
}
```

If you have added the server in the scripts section, you can run it with `npm run server`. Alternatively you can run it with `npx vqb-products-server`

Check the webpage that opens automatically in your browser for more instructions on how to configure the server (by default http://localhost:3000) and its API documentaion.

By default, even though some of the endpoints requires authentication, they can be accessed without it. You can start development without using the authentication. We have some requirements below, where authentication is needed, so in order to enable authenticaion on server, it can be run with adding `--auth` parameter like `vqb-products-server --auth`. Also, to simulate async processing, the server can be run with `--async` parameter like `vqb-products-server --async`.

Please check carefully the API documentation and request parameters. The documentation is self-explanatory, but make sure you check the details. For example:
```bash
GET /products
```
provides you option to send paging requests. 

For full configuration options of the server, check the webpage that opens automatically.


### Requirements

Make sure you read all of the requirements in order to get full information of the task's expectations. Even though the list of items seams long, once you read it all, you will notice that they are related and the list just helps you to easily finish the task. Then try to complete the following features one after another in order (recommended but not necessary). 

The features are grouped in different categories. The features marked as **required** are the bare minimum necessary to qualify,
the **nice to have** increase your score and the **specials** will surely demonstrate your talent.

#### Required features

1. Create a web page to display the page 1 and 10 items of the list of products showing `title`, `image`, `category` and `price` of each prouduct.
2. Create `Add to cart` button with each product item.
3. List the products by categories
4. Create a search bar that allows for searching the products and a search page for the results items, and display an empty response message if no products were found
5. Add a navigation control that allows to change pages (optionally also to change the number of items per page).
6. Change the navigation element to update the url of the page when clicked and to show the correct page (and page size if implemented) when the browser page is refreshed.
7. Validate the parameters just added in the url to match the format accepted by the server for page (and page size) and redirect to a "Bad request" page in case the parameters are invalid.
8. Create a cart button in the header with a bubble indicator to show how many products are in the cart
9. Create a cart page/popover to display the current products in the cart and give the ability to change products quantity and delete them from the cart
10. If the user tried to add to thier cart a quantity of product that exceeds the product `stock`, display an error.
11. On small screen display your data in cards instead of tabulated, on medium screens show the cards on portrait mode and tabulated data in landscape mode, on large screens show only the tabulated data
12. Create your own custom component for the cards. Use scalable component spacing based on font size 
13. Add one unit test that check your page with mocked data from the server works.

#### Nice to have features

1. Add a progress bar on indefinite status or loader to this product card when adding to the cart.
2. If a product's `stock` is 0 then the product should be marked as unavailable
3. Create your own custom component to display the tabular data with the possibility to render the cells with custom html
4. Add a column with a delete button on it that allows to delete flights by `id` on the server. This column must occupy have minimum width space except for some padding, and you must ask for confirmation before delete.
5. Add a search input on the flight list page that allows filtering by `code`.
6. Update the url as well to persist the user filter and validate it. If the user types an invalid product title show an error on the search input and no results on the table.
7. When the user types in the search bar wait a few seconds after stopped typing to update the url and send the request to the server.
8. Create a seperate page that displays the product information when a product is clicked
9. Add a register screen that allows to create new users with `name`, `email` and `password` fields.
10. Add a login screen that allows to authenticate the user with `email` and `password`.
11. Enable security on the server and make all your request authenticated. Do not allow access to the application to users that are not registered.
12. Add a toolbar on top of your authenticated page showing the authenticated user with a menu with an option to logout. Make sure error pages also has this toolbar.
13. Create dark and light mode of your app. You can put the swithcher in the toolbar.
14. Create E2E tests for the various features


#### Special features

1. When the security credentials are expired redirect the user to the login screen.
2. Automatically refresh the tokens when they expire without login out the user.

---
:scroll: **END**
