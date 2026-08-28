# Getting Started

This guide explains how to make your first request to the Product API.
The product API is a sample REST API that allows you to retrieve, search, create, update and delete product information.
You can test the API using tools such as Postman.


## API Base URL

All API requests are sent to the following url:

```text
https://dummyjson.com
```


## Before You Begin

Before using the API, make sure you have:

- An internet connection
- A tool for sending HTTP requests, such as Postman
- A basic understanding of HTTP methods such as GET, POST, PUT and DELETE


## Make your first API request

The easiest way to test the API is to test the list of products.
Use the following request:

```text
GET https://dummyjson.com/products
```
In Postman:

1. Create a new request.
2. Select ```GET``` as the HTTP method.
3. Enter the following URL:
```text
https://dummyjson.com/products
```
4. Click **Send**.
5. The API returns a list of products in JSON format.


## Example response

A successful request returns a response similar to:

```JSON
{
  "products": [
    {
      "id": 1,
      "title": "Essence Mascara Lash Princess",
      "description": "The Essence Mascara Lash Princess is a popular mascara...",
      "category": "beauty",
      "price": 9.99
    }
  ]
}
```

The response contains information about the products returned by the API.


## Understanding the response

The response is formatted as JSON.
Some commonly used fields include:

|Field| Description|
|---|---|
|id| unique identifier for the product|
| Title| Name of the product|
| Description| Description of the product|
| Category| Product category|
| Price| Product price|


## What's next?

Now that you've made the first API request, you can explore the other endpoints. 

You can:

- Retrieve a specific product.
- Search for products.
- Create a product.
- Update a product.
- Delete a product.

See the API Reference for detailed information about each endpoint.






