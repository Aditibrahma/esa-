# CS 474 REST API Assignment

## How to use

1. Clone the repository.
2. Navigate to the directory.
3. Run command : `npm init`
4. Install dependencies : `npm install express body-parser mongoose --save`
5. Install and use nodemon : `npm install --save-dev nodemon`
6. In the package.json file, add `"start": ""nodemon index.js` under `scripts`
```
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "nodemon index.js"
  },
```
7. In `index.js` replace `<PASSWORD>` with the password provided in the submission file
8. Run the file using the command : `npm start`
9. Test the API on http://localhost:3000/rest/v1/

## REST API
***GET Product***

**Request URL**: /rest/v1/products

*Response*:
```
[
    {
        "_id": "607f0c45f870946c5af6e7da",
        "productId": "12445dsd234",
        "category": "Modile",
        "productName": "Samsung",
        "productModel": "GalaxyNote",
        "price": 700,
        "availableQuantity": 10
    },
    {
        "_id": "607f0c60f870946c5af6f998",
        "productId": "123245ds4234",
        "category": "TV",
        "productName": "Sony",
        "productModel": "Bravia",
        "price": 1200,
        "availableQuantity": 6
    }
]
```

***GET User***

**Request URL**: /rest/v1/users

*Response*:
```
[
    {
        "_id": "607f001cf870946c5aeca2a9",
        "user_id": "18xj001",
        "username": "Tony"
    },
    {
        "_id": "607f004bf870946c5aecc78e",
        "user_id": "18xj002",
        "username": "Steve"
    }
]
```
**Request URL**: /rest/v1/users/<user_id>

*Response*:
```
[
    {
        "_id": "607f001cf870946c5aeca2a9",
        "user_id": "18xj001",
        "username": "Tony"
    }
]
```
***PUT CartItem API***

**Request URL**: /rest/v1/users/<user_id>/cart

*Body Parameter*:
```
{
    "productId": "12445dsd234",
    "quantity": "1",
    "amount": "1200"
}
```
*Response*:
```
[
    {
        "_id": "6084dd2df870946c5acdad96",
        "user_id": "18xj001",
        "cartItems": [
            {
                "productId": "12445dsd234",
                "quantity": "1",
                "amount": "1200"
            }
        ]
    }
]
```
***Retrieve UserCart***

**Request URL**: /rest/v1/users/<user_id>/cart

*Response*:
```
[
    {
        "_id": "6084dd2df870946c5acdad96",
        "user_id": "18xj001",
        "cartItems": [
            {
                "productId": "12445dsd234",
                "quantity": "1",
                "amount": "1200"
            }
        ]
    }
]
```
