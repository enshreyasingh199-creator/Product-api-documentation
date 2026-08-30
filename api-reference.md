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


### Example request
```http
GET https://dummyjson.com/products
```

### Example Response

A Successful response returns a list of products.

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
|`500 Internal Server Error`| The server encountered an unexpected error. |


## Get a Product

Retrieves a specific product using its unique product ID.

### Endpoint

```text
GET/products/{id}
```

### Full URL

```text
https://dummyjson.com/products/{id}
```

### Path Parameters

|Parameter|Type|Required|Description
|---|---|---|---|
|`id`| Number| Yes| The unique id of the product to retrieve.|

### Example Request

```JSON
{
  "id": 1,
  "title": "Essence Mascara Lash Princess",
  "description": "The Essence Mascara Lash Princess is a popular mascara known for its volumizing and lengthening effects. Achieve dramatic lashes with this long-lasting and cruelty-free formula.",
  "category": "beauty",
  "price": 9.99,
  "discountPercentage": 10.48,
  "rating": 2.56,
  "stock": 99,
  "brand": "Essence"
}
```

### Response Fields

|Field| Type| Description|
|---|---|---|
|`id`| Number| Unique id of the product to retrieve|
|`title`| String| Name of the Product|
|`description`| String| Description of the product|
|`category`| String| category of the product|
|`price`| Number| Price of the product|
|`discountPercentage`| Number| discount given on the product|
|`rating`| Number| rating of the product|
|`stock`| Number| no. of units in the stock|
|`brand`| String| Brand associated with the product|

### HTTP Status code

|Status Code| Meaning|
|---|---|
|`200 OK`|The product was successfully retrieved.|


## Search Product

Searches for product using a search keyword.

### Endpoint

```text
GET/product/search
```

### Full URL

```text
https://dummyjson.com/products/search
```

### Query Parameters

|Parameter| Type| Required| Description|
|---|---|---|---|
|`q`| String| Yes| Keyword to search for product|

### Example request

```text
GET/products/search
```

### Example response

A successful response returns a list of products matching the keyword.

```JSON
"products": [
    {
      "id": 101,
      "title": "Apple AirPods Max Silver",
      "description": "The Apple AirPods Max in Silver are premium over-ear headphones with high-fidelity audio.",
      "category": "mobile-accessories",
      "price": 549.99
    }
  ],
  "total": 1,
  "skip": 0,
  "limit": 30
}
```

### Response Field

|Field|Type| Description|
|---|---|---|
|Product| array| list of products matching the keyword|
|`id`|Number|Unique id of the product|
|`title`|String|Title of the product|
|`description`|String|Description of the produrct|
|`category`|String| Category the product belongs to|
|`price`| Number| price of the product|
|`total`| Number| total no. of matching products|
|`skip`| Number| Total products skipped|
|`limit`| NUmber| maximum no of products returned|

### HTTP Status Code
|Status Code| Meaning|
|---|---|
|`200 OK`| The search was successful|
