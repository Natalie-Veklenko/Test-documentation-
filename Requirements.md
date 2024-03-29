# ACS_beauty

The API is available at `https://`

## Endpoints
- [User](#User)
  - [Register user](#Register-user)
  - [Activate from email link](#Activate-from-email-link)
  - [Update token](#Update-token)
  - [Log in user](#Log-in-user)
  - [Get my account info](#Get-my-account-info)
  - [Get users](#Get-users)
  - [PATCH my account with avatar](#PATCH-my-account-with-avatar)
  - [PATCH user](#Patch-user)
  - [Log out user](#Log-out-user)
  - [Delete users](#Delete-users)
 
- [Category](#Category)
  - [Get all orders](#Get-all-orders)
  - [Get a single order](#Get-a-single-order)
  - [Create a new order](#Create-a-new-order)
  - [Update an order](#Update-an-order)
  - [Delete an order](#Delete-an-order)
- [Subcategory](#Subcategory)
  - [Get all orders](#Get-all-orders)
  - [Get a single order](#Get-a-single-order)
  - [Create a new order](#Create-a-new-order)
  - [Update an order](#Update-an-order)
  - [Delete an order](#Delete-an-order)
- [Product] (#Product)
  - [Get all orders](#Get-all-orders)
  - [Get a single order](#Get-a-single-order)
  - [Create a new order](#Create-a-new-order)
  - [Update an order](#Update-an-order)
  - [Delete an order](#Delete-an-order)
- [Order](#Order)
  - [Get all orders](#Get-all-orders)
  - [Get a single order](#Get-a-single-order)
  - [Create a new order](#Create-a-new-order)
  - [Update an order](#Update-an-order)
  - [Delete an order](#Delete-an-order)
- [API Authentication](#API-Authentication)
  - [Register a new API client](#Register-a-new-API-client)


### USER
 ### Register-user

 
GET (http://13.48.46.250:5000/api/user/me)
## Get my account info
**Parameters**

| Name        | Type    | In    | Required | Description                                                                                                                                          |
| ----------- | ------- | ----- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| `category`  | string  | query | No       | Specifies the category of products you want to be returned. It can be one of: meat-seafood, fresh-produce, candy, bread-bakery, dairy, eggs, coffee. |
| `results`   | integer | query | No       | Specifies the number of results you want. Must be number between 1 and 20. By default, only 20 products will be displayed.                           |
| `available` | boolean | query | No       | Specifies the availability of the products. By default, all products will be displayed.                                                              |

**Status code**
| Status code | Description |
| ----------- | ----------- |
| 200 | to get my own account info |
| 403 | Bad request |


### Title of unit
**`GET /url`**
The request body need to be in JSON format.

**Parameters**

| Name        | Type   | Required | Description |                                                             
| ----------- | ------ | -----| ------------------------------------------------------------ |
| `category`  | string  | No       | Specifies the category of products you want to be returned. It can be one of: meat-seafood, fresh-produce, candy, bread-bakery, dairy, eggs, coffee. |
| `results`   | integer | No       | Specifies the number of results you want. Must be number between 1 and 20. By default, only 20 products will be displayed.                           |
| `available` | boolean | No       | Specifies the availability of the products. By default, all products will be displayed.      |

**request body**

**Responce**
The responce body need to be in JSON format.

**Status codes**
| Status code | Description |
|-----------------|-----------------------------------------------------|
| 200 OK | Indicates a successful response. |
| 400 Bad Request | Indicates that the parameters provided are invalid. |

Example response:

```
[
    {
        "id": 4643,
        "category": "coffee",

```

| Name            | Type   | In     | Required | Description                                   |
| --------------- | ------ | ------ | -------- | --------------------------------------------- |
| `Authorization` | string | header | Yes      | Specifies the bearer token of the API client. |

| Name            | Type   | In     | Required | Description                          |
| --------------- | ------ | ------ | -------- | ------------------------------------ |
| `Authorization` | string | header | Yes      | The bearer token of the API client.  |
