# API Reference

This page provides detailed explanation about the Product API endpoints.
The API allows you to retrieve, search, update, create and delete product information.


## Base URL

```text
https://dummyjson.com
```


## Endpoints

| Method| Endpoint | Description |
|---|---|---|
| GET |`/Products` | Retrieve a list of products |
| GET |`/Product/{id}`| Retrieve a specific product |
| GET |`/Products/search`| Search for products |
| POST |`/Products/add`| Create a new product |
| PUT |`/Products/{id}`| Update a product |
| DELETE |`/Products/{id}`| Delete a product |


## Get All Products

Retrieves a list of products from the API.

### Endpoint

```text
GET /products
```

### Full URL
```text
https://dummyjson.com/products
```

### Requests

No parameters are required for this request.

### Example Request
```JSON
{
  "products": [
    {
      "id": 1,
      "title": "Essence Mascara Lash Princess",
      "description": "The Essence Mascara Lash Princess is a popular mascara known for its volumizing and lengthening effects.",
      "category": "beauty",
      "price": 9.99
    }
  ],
  "total": 194,
  "skip": 0,
  "limit": 30
}
```

### Response Fields

| Field| Type| Description|
|---|---|---|
|`products`| Array|List of products returned by the API|
|`id`| Number| Unique identifier for the product|
|`title`| String| Name of the Product|
|`description`| String| Description of the product|
|`category`| String| Category of Product|
|`price`| Number| Price of the product|
|`total`| Number| Price of the product|
|`skip`| Number| Number of products skipped|
|`limit`| Number| Maximum number of products returned|

### Status Code

|Status Code| Meaning|
|---|---|
|`200 OK`| The request was successfull|



